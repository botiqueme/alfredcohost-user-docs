# Guida integrazione backend – Robin (chat docs)

Documento per lo sviluppatore backend: cosa deve implementare e **dove** collegarsi nel frontend.

---

## Contesto

- **Frontend**: chat in iframe (`docs/chatbot/index.html`) aperta da un widget nella doc (bottone in basso a destra).
- **Flusso**: l’utente apre la chat → vede il messaggio di benvenuto → invia messaggi → il backend risponde. Il frontend gestisce già UI, stato `thread_id`, loading, Restart e minimize.
- **File da modificare**: un solo file lato frontend, **`docs/chatbot/index.html`**, nella sezione `<script>` in fondo alla pagina.

---

## Endpoint richiesti

Il backend deve esporre **tre** endpoint (base URL da configurare nel frontend, es. variabile o config).

### 1. Crea thread (nuova conversazione)

**Quando si chiama**: alla **prima** invio messaggio dell’utente (quando il frontend non ha ancora un `thread_id`), oppure dopo un “Restart” al primo messaggio successivo.

| | Dettaglio |
|---|-----------|
| **Metodo** | `POST` |
| **URL suggerito** | `POST /api/chat/thread` (o simile) |
| **Body** | Opzionale: `{}` o `{ "source": "docs" }` |
| **Risposta attesa** | `{ "thread_id": "uuid-o-stringa-univoca" }` |
| **Errori** | 4xx/5xx gestiti dal frontend come “errore generico” (messaggio + retry opzionale). |

Il frontend salverà `thread_id` in memoria e lo userà per tutti i messaggi successivi fino a Restart.

---

### 2. Invia messaggio e ricevi risposta

**Quando si chiama**: ogni volta che l’utente clicca “Send” (o Invio), dopo aver eventualmente ottenuto un `thread_id` dal punto 1.

| | Dettaglio |
|---|-----------|
| **Metodo** | `POST` |
| **URL suggerito** | `POST /api/chat/message` (o simile) |
| **Body** | `{ "thread_id": "<id>", "message": "<testo utente>" }` |
| **Risposta attesa** | `{ "reply": "<testo risposta assistente>" }` |
| **Errori** | 4xx/5xx: frontend può mostrare messaggio di errore e tenere il messaggio utente visibile (retry “later”). |

Se il backend restituisce un nuovo `thread_id` (es. dopo reset lato server), il frontend può aggiornare la variabile `threadId` con il valore ricevuto (opzionale, da concordare).

---

### 3. Reset thread (chiudi conversazione)

**Quando si chiama**: quando l’utente clicca **“Restart”** nella chat.

| | Dettaglio |
|---|-----------|
| **Metodo** | `POST` o `DELETE` |
| **URL suggerito** | `POST /api/chat/thread/reset` oppure `DELETE /api/chat/thread/:thread_id` |
| **Body / URL** | `{ "thread_id": "<id>" }` nel body, oppure `thread_id` nell’URL. |
| **Risposta attesa** | 200 OK (body irrilevante, es. `{ "ok": true }`). |
| **Errori** | 4xx/5xx: il frontend può comunque azzerare `thread_id` e messaggi in locale (conversazione resettata lato UI). |

Dopo la chiamata (o in caso di errore), il frontend azzera `thread_id` e svuota i messaggi; al prossimo invio si richiederà un nuovo thread (endpoint 1).

---

## Dove collegare il backend nel frontend

**File**: `docs/chatbot/index.html`  
**Sezione**: lo script in fondo alla pagina (circa righe 229–337).

### 1. Base URL dell’API

In cima allo script, aggiungere una variabile per l’URL base del backend (es. da sostituire in build o da configurare in un solo punto):

```javascript
var API_BASE = 'https://your-backend.example.com';  // TODO: configurare
```

---

### 2. Ottenere un nuovo `thread_id`

**Dove**: la prima volta che l’utente invia un messaggio **senza** avere ancora `thread_id`, il frontend deve chiamare l’endpoint “crea thread” e poi usare l’id ricevuto per “invia messaggio”.

**Codice attuale da sostituire**: dentro `sendMessage()`, il blocco che oggi fa:

- `setLoading(true)`
- `setTimeout(...)` con risposta placeholder e `if (!threadId) threadId = 'placeholder-thread-' + Date.now();`
- `setLoading(false)`

**Cosa fare**:

1. Se `threadId === null`, chiamare prima `POST /api/chat/thread`, leggere `thread_id` dalla risposta e assegnare `threadId = data.thread_id`.
2. Poi chiamare `POST /api/chat/message` con `{ thread_id: threadId, message: text }`.
3. In risposta: mostrare `data.reply` come messaggio del bot (e togliere la risposta placeholder).
4. Gestire errori di rete o HTTP: `setLoading(false)`, eventualmente mostrare un messaggio tipo “Errore di connessione. Riprova.” (dettagli in “Error handling” sotto).

Pseudocodice da integrare nella `sendMessage()`:

```javascript
function ensureThread(callback) {
  if (threadId) return callback();
  fetch(API_BASE + '/api/chat/thread', { method: 'POST', headers: { 'Content-Type': 'application/json' }, body: '{}' })
    .then(function (r) { return r.json(); })
    .then(function (data) { threadId = data.thread_id; callback(); })
    .catch(function () { callback(true); }); // true = errore
}

function sendMessage() {
  // ... (validazione text, addMessage(text, true), inputEl.value = '', setLoading(true))
  ensureThread(function (err) {
    if (err) { setLoading(false); addMessage('Impossibile avviare la conversazione. Riprova.', false); return; }
    fetch(API_BASE + '/api/chat/message', {
      method: 'POST',
      headers: { 'Content-Type': 'application/json' },
      body: JSON.stringify({ thread_id: threadId, message: text })
    })
      .then(function (r) { return r.json(); })
      .then(function (data) { setLoading(false); addMessage(data.reply, false); })
      .catch(function () { setLoading(false); addMessage('Errore di connessione. Riprova.', false); });
  });
}
```

Adattare nomi endpoint e proprietà (`reply`, `thread_id`) a ciò che il backend espone realmente.

---

### 3. Restart: chiamare l’endpoint di reset

**Dove**: funzione `clearConversation()` (circa riga 289).

**Codice attuale**: azzera `threadId`, svuota i messaggi, mostra di nuovo il welcome. C’è già un commento: “When backend exists: call reset endpoint”.

**Cosa fare**: prima di azzerare `threadId` e svuotare i messaggi, se `threadId` è valorizzato chiamare l’endpoint di reset (es. `POST /api/chat/thread/reset` con body `{ thread_id: threadId }`). Poi eseguire come oggi: `threadId = null`, svuotare la lista messaggi, `showWelcome()`, `setLoading(false)`. In caso di errore HTTP si può comunque procedere con il reset lato UI.

Esempio:

```javascript
function clearConversation() {
  if (threadId) {
    fetch(API_BASE + '/api/chat/thread/reset', {
      method: 'POST',
      headers: { 'Content-Type': 'application/json' },
      body: JSON.stringify({ thread_id: threadId })
    }).catch(function () {});
  }
  threadId = null;
  messagesEl.innerHTML = '';
  showWelcome();
  setLoading(false);
}
```

---

## Riepilogo punti di intervento

| Cosa | File | Dove |
|------|------|------|
| Base URL API | `docs/chatbot/index.html` | In cima allo script (variabile `API_BASE` o simile). |
| Crea thread | `docs/chatbot/index.html` | In `sendMessage()`: prima di inviare il primo messaggio, se `threadId === null` → chiamare endpoint crea thread e salvare `thread_id`. |
| Invia messaggio + mostra risposta | `docs/chatbot/index.html` | In `sendMessage()`: sostituire il `setTimeout` placeholder con la chiamata a “invia messaggio”, poi mostrare `reply` e fare `setLoading(false)`. |
| Reset thread | `docs/chatbot/index.html` | In `clearConversation()`: se c’è `threadId`, chiamare endpoint reset; poi azzerare `threadId` e messaggi come già fatto. |

---

## CORS e ambiente

- La chat viene servita dal sito delle doc (stesso dominio o sotto un path tipo `.../docs/`). Le chiamate al backend saranno **cross-origin** se il backend è su altro dominio.
- Il backend deve rispondere con **CORS** adeguati (es. `Access-Control-Allow-Origin` per l’origine del sito doc, o un pattern concordato) alle richieste `POST` (e eventualmente `OPTIONS`) verso gli endpoint sopra.
- Per sviluppo locale: configurare `API_BASE` con l’URL del backend locale (es. `http://localhost:8080`) e assicurarsi che il backend accetti l’origine del frontend (es. `http://localhost:3000`).

---

## Messaggio di benvenuto

Il testo di benvenuto è **solo lato frontend** (variabile `WELCOME` nello script). Il backend non deve fornirlo; può eventualmente sovrascriverlo in una versione futura se si passa a “welcome dal backend” dopo la creazione del thread.

---

## Riferimenti

- **Spec frontend e stato attuale**: `docs/chatbot/SPEC-RECAP.md`
- **UI e flusso**: il frontend gestisce già persistenza apertura/chiusura, minimize, Restart (UI), loading e typing; il backend deve solo fornire i tre endpoint e il frontend deve sostituire i placeholder con le chiamate reali come sopra.
