
# 📘 CONCETTI CHIAVE META (WhatsApp Business API) 2026

Meta non fattura per "messaggio inviato" in senso tradizionale (come gli SMS), ma applica tariffe diverse in base a **chi inizia la conversazione** e allo **scopo del messaggio**.

## 1. Le 4 Categorie di Messaggio

Ogni comunicazione su WhatsApp x Alfred deve essere classificata in una di queste categorie:

* **Service (Assistenza):** Messaggi inviati in risposta a una richiesta dell'utente. Si aprono quando il guest scrive per primo.
* **Utility (Notifiche):** Messaggi necessari per completare una transazione o fornire informazioni critiche (es. conferme, codici check-in).

## 2. Il Modello di Fatturazione: Sessioni vs Messaggi

Dal 2026, Meta utilizza due sistemi di calcolo differenti:

### A. Modello "Per Messaggio" (Template)

Si applica a **Utility, Marketing e Authentication**.

* **Fatturazione singola:** Paghi per ogni singolo messaggio template consegnato.
* **Nessuna finestra gratuita:** Se invii 3 notifiche utility diverse, paghi 3 volte la tariffa utility.

### B. Modello "Per Conversazione" (Service)

Si applica solo alla categoria **Service**.

* **La Finestra delle 24 Ore:** Quando il guest invia un messaggio, si apre una finestra di servizio. Tutti i messaggi di testo libero inviati dal bot entro 24 ore rientrano in una singola sessione.
* **Free Tier (1.000 chat/mese):** Le prime **1.000 conversazioni di assistenza** (Service) ogni mese sono **completamente gratuite** lato Meta.

## 3. Link Ufficiali Meta & Documentazione

Per monitorare i prezzi e le regole tecniche aggiornate:

* **Tabella Prezzi Ufficiale Meta:** [WhatsApp Business API Pricing](https://developers.facebook.com/docs/whatsapp/pricing)
* **Documentazione Categorie Template:** [Message Template Categories](https://www.google.com/search?q=https://developers.facebook.com/docs/whatsapp/business-management-api/message-templates/guidelines)
* **Gestione Finestra di Servizio:** [Customer Service Window Rules](https://www.google.com/search?q=https://developers.facebook.com/docs/whatsapp/cloud-api/guides/send-messages%23service-messages)

---

## 4. Riepilogo Tariffe Meta (Esempio Italia)

*Dati indicativi basati sulle rate card correnti per chi usa partner come Vonage o Twilio.*

| Categoria | Tipo di Costo | Costo Meta Stimato |
| --- | --- | --- |
| **Service (Assistenza)** | Per Sessione (24h) | **$0.00** (Sotto le 1.000/mese) |
| **Utility (Notifiche)** | Per Messaggio | **~$0.0034** |


---

### Cosa deve ricordare il tuo sviluppatore:

1. **L'errore 131047:** Se il bot prova a rispondere a un guest dopo che sono passate 24 ore dall'ultimo messaggio del guest, l'invio fallirà. Bisogna usare un **Template Utility** per riaprire la chat.
2. **Ottimizzazione Template:** Poiché ora i messaggi Utility si pagano "a pezzo", conviene accorpare più informazioni in un unico template invece di inviare molti messaggi brevi.

## Next step
Verificare come Meta approva (o rifiuta) i template per evitare il ban
