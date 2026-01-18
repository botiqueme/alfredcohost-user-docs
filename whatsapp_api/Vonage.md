43FS3dyqWoeJSLG5 vonage API KEY
Ecco la guida aggiornata e strutturata con i dati definitivi per il **2026**. Questa pagina riflette il nuovo modello di Meta (passaggio al costo "per messaggio" per i template) e le tariffe specifiche di Vonage per l'Italia.

---

# GUIDA COSTI WHATSAPP API: IL MODELLO VONAGE (2026)

L'utilizzo di WhatsApp tramite Vonage si basa sulla somma di due componenti: la **tariffa Meta** (proprietaria di WhatsApp) e la **Platform Fee di Vonage**.

## 1. Concetti Chiave: VONAGE

Vonage funge da gateway tecnico e applica un modello di costo "Pay-per-Message" estremamente vantaggioso per chi riceve molti messaggi.

* **Inbound Messages (Ricevuti) GRATUITI:** Vonage non addebita costi per i messaggi che i guest inviano al tuo bot. Questo ti protegge dai costi se un cliente è particolarmente loquace.
* **Outbound Messages (Inviati):** Paghi una tariffa fissa per ogni messaggio inviato dal tuo bot. Per l'Italia, questa tariffa è inclusa nel prezzo finale che vedi in tabella.
* **Virtual Number:** Un costo fisso mensile (circa **$1.00 - $1.50**) per il mantenimento del numero di telefono.
* **Documentazione ufficiale:** [Vonage Messages API Pricing](https://www.vonage.com/communications-apis/messages/pricing/)

## 2. Concetti Chiave: META (WhatsApp)

Dal 2026, Meta ha consolidato il passaggio dal costo "per conversazione" al costo **"per messaggio consegnato"** per i messaggi basati su template.

* **Le 1.000 Sessioni "Service" GRATIS:** Ogni mese, le prime 1.000 conversazioni avviate dai guest (Service) sono **gratuite lato Meta**. Pagherai solo la piccola quota di Vonage per le risposte del bot.
* **Costo per Messaggio (Utility/Marketing):** I messaggi di notifica (es. alert al manager o codici check-in) non pagano più una "finestra di 24h", ma si pagano **singolarmente** ogni volta che vengono consegnati.
* **Categorie di Messaggio:** * **Utility:** Notifiche transazionali (le più economiche).
* **Service:** Risposte libere del bot a domande dei guest.
* **Marketing:** Promozioni (le più costose).



---

## 3. Tariffe per l'ITALIA (Dati Rate Card 2026)

*Valori medi espressi in USD per singolo messaggio consegnato.*

| Categoria | Costo per Messaggio (Meta + Vonage) |
| --- | --- |
| **Service (Risposta Bot)** | **$0.00819** |
| **Utility (Alert/Check-in)** | **$0.00910** |
| **Marketing (Promo)** | **$0.02098** |

---

## 4. Esempio Pratico (Simulazione su 100 Guest)

Immaginiamo un mese tipo con **100 Guest** che arrivano nelle tue strutture.
*Ogni guest manda 5 messaggi e il bot risponde con 5 messaggi. Inoltre, il bot invia 1 alert "Utility" al Manager per ogni guest.*

### A. Interazione Guest-Bot (Service)

Meta non addebita la sessione (sei sotto i 1.000). Paghi solo i messaggi che il bot invia tramite Vonage.

* Messaggi ricevuti (500): **$0.00**
* Risposte del bot (500): 500 x $0.00819 = **$4.09**

### B. Alert al Property Manager (Utility)

Invio di un template pre-approvato per ogni nuovo guest.

* Alert inviati (100): 100 x $0.00910 = **$0.91**

### C. Costi Fissi

* Canone mensile numero: **$1.00**

### **TOTALE MENSILE ESTIMATO: $6.00**

---
