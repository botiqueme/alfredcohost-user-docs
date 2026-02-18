# Guida integrazione backend – Robin (chat docs)

Documento per lo sviluppatore backend: stato attuale dell'integrazione e cosa resta da fare.

---

## Contesto

- **Frontend**: chat in iframe (`docs/chatbot/index.html`) caricata da un widget nella documentazione Docsify (bottone 💬 in basso a destra).
- **Flusso**: l'utente apre la chat → vede il messaggio di benvenuto (nella sua lingua) → invia messaggi → il backend risponde.
- **Multi-lingua**: la documentazione supporta 4 lingue (`en`, `fr`, `it`, `es`). Il chatbot adatta la UI alla lingua scelta dall'utente e la comunica al backend ad ogni richiesta.

---

## Endpoint attuali

Il frontend chiama **due** endpoint, già configurati e funzionanti:

| Endpoint | URL |
|----------|-----|
| **Invia messaggio** | `POST https://chatbot.alfredco.host/api/v1/docs_chatbot` |
| **Restart conversazione** | `POST https://chatbot.alfredco.host/api/v1/docs_chatbot_restart` |

### 1. Invia messaggio

**Quando**: ogni volta che l'utente clicca "Send" / "Invia" / "Envoyer" / "Enviar".

**Payload inviato dal frontend**:

```json
{
  "message": "come aggiungo una proprietà?",
  "thread_id": "abc123",
  "preferred_language": "it",
  "current_page_url": "#/it/procedures/properties_p.md"
}
```

| Campo | Tipo | Note |
|-------|------|------|
| `message` | string | Testo dell'utente. Sempre presente. |
| `thread_id` | string \| null | ID conversazione restituito dal backend alla prima risposta. `null` al primo messaggio. |
| `preferred_language` | string | Codice lingua scelto dall'utente: `en`, `fr`, `it`, `es`. **Nuovo campo.** |
| `current_page_url` | string | Hash della pagina docs che l'utente sta visualizzando, es. `#/it/procedures/properties_p.md`. **Nuovo campo.** |

**Risposta attesa dal backend**:

```json
{
  "status": "success",
  "data": {
    "thread_id": "abc123",
    "response": "Per aggiungere una proprietà, vai su..."
  }
}
```

**Nota su `preferred_language`**: attualmente l'AI del chatbot deduce già la lingua dal testo del messaggio utente. Il campo `preferred_language` serve come rinforzo esplicito, utile soprattutto:
- Al primo messaggio, quando non c'è ancora contesto
- Se l'utente scrive in una lingua diversa da quella dell'interfaccia
- Per istruire il modello a rispondere sempre nella lingua della documentazione scelta

**Nota su `current_page_url`**: permette al backend di contestualizzare la risposta. Se l'utente sta leggendo la pagina "Gestire le proprietà" e chiede "come faccio?", il backend può usare questa informazione per dare una risposta più pertinente.

---

### 2. Restart conversazione

**Quando**: l'utente clicca "Restart" / "Riavvia" / "Redémarrer" / "Reiniciar".

**Payload**:

```json
{
  "thread_id": "abc123"
}
```

**Risposta**: qualsiasi 200 OK. Il frontend azzera comunque `thread_id` e messaggi in locale.

---

## Cosa gestisce il frontend (già implementato)

| Funzionalità | Stato |
|---|---|
| UI chat completa (messaggi, input, loading, typing indicator) | ✅ |
| Gestione `thread_id` (salvataggio in memoria, reset) | ✅ |
| Rendering Markdown nelle risposte (via `marked.js`) | ✅ |
| Interfaccia tradotta in 4 lingue (welcome, placeholder, bottoni, errori) | ✅ |
| Aggiornamento lingua in tempo reale (cambio lingua senza ricaricare) | ✅ |
| Invio `preferred_language` e `current_page_url` nel payload | ✅ |
| Apertura/chiusura panel, minimize, persistenza in `sessionStorage` | ✅ |

---

## Cosa deve fare il backend (TODO)

### Priorità 1: Usare `preferred_language`

Il campo è già inviato dal frontend. Il backend deve:
1. Leggere `preferred_language` dal body della richiesta
2. Usarlo nel prompt del modello AI (es. "Rispondi sempre in {preferred_language}")

Se il backend non lo gestisce, non si rompe nulla: il campo viene semplicemente ignorato e l'AI continua a dedurre la lingua dal testo.

### Priorità 2: Usare `current_page_url`

Il campo è già inviato dal frontend. Il backend può:
1. Estrarre il percorso del file .md dall'hash (es. `#/it/procedures/properties_p.md` → `procedures/properties_p`)
2. Usarlo come contesto aggiuntivo nel prompt (es. "L'utente sta leggendo la pagina: Gestire le proprietà")

### Priorità 3: Link nelle risposte (STANDBY)

Attualmente il frontend ha un handler che tenta di convertire i link nelle risposte del bot in link navigabili nella documentazione. Questo handler è **pre-esistente** e **non è stato aggiornato** per il multi-lingua.

**Stato attuale**: se il backend restituisce link come `/procedures/properties_p.md`, l'handler li converte in `#/procedures/properties_p.md` (senza prefisso lingua).

**Da fare in futuro**: aggiornare l'handler per anteporre la lingua corretta ai link, oppure far restituire al backend link già con il prefisso lingua (es. `#/it/procedures/properties_p.md`). Vedere i commenti `TODO: LINK LANGUAGE PREFIX` nel codice di `chatbot/index.html`.

---

## CORS

Le chiamate dal frontend al backend sono **cross-origin** (il sito docs è su Netlify, il backend su `chatbot.alfredco.host`). Il backend deve rispondere con gli header CORS appropriati:

```
Access-Control-Allow-Origin: <origine del sito docs>
Access-Control-Allow-Methods: POST, OPTIONS
Access-Control-Allow-Headers: Content-Type
```

---

## Architettura lingua

```
┌─────────────────────────────────────┐
│  Docsify (index.html)               │
│                                     │
│  localStorage: preferredLanguage=it │
│                                     │
│  ┌───────────────────────────────┐  │
│  │  chatbot/index.html (iframe)  │  │
│  │                               │  │
│  │  1. Legge lingua dal parent   │  │
│  │     localStorage              │  │
│  │  2. Traduce UI (i18n)        │  │
│  │  3. Invia preferred_language  │  │
│  │     nel payload API           │  │
│  │  4. Ascolta postMessage per   │  │
│  │     aggiornamenti lingua      │  │
│  └───────────────────────────────┘  │
│                                     │
│  Quando il panel si apre, il parent │
│  invia postMessage con la lingua    │
│  corrente → il chatbot si aggiorna  │
└─────────────────────────────────────┘
         │
         ▼ POST /api/v1/docs_chatbot
┌─────────────────────────────────────┐
│  Backend (chatbot.alfredco.host)    │
│                                     │
│  Riceve: message, thread_id,        │
│          preferred_language,         │
│          current_page_url            │
│                                     │
│  TODO: usare preferred_language e   │
│        current_page_url nel prompt  │
└─────────────────────────────────────┘
```

---

## File di riferimento

| File | Cosa contiene |
|------|---------------|
| `docs/chatbot/index.html` | Frontend completo del chatbot (UI + logica + i18n) |
| `docs/index.html` | Pagina Docsify principale (widget chatbot + language switcher) |
| `docs/chatbot/BACKEND-INTEGRATION.md` | Questo documento |
