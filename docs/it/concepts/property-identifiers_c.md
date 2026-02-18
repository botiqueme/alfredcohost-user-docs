# Property identifiers

Ogni proprietà in Alfred Co.Host è definita da tre identificatori che la rendono riconoscibile sia internamente sia ai tuoi ospiti.  
**Questi identificatori sono essenziali per il corretto funzionamento di Alfred**: consentono alla piattaforma di collegare il chatbot giusto all’appartamento giusto e garantire un’esperienza fluida.

In questa pagina trovi i tre identificatori che abilitano l’automazione e le interazioni con gli ospiti:  
- L’[Internal identifier](#internal-identifier), usato solo nella tua dashboard per la gestione delle proprietà.  
- Gli **Guest-facing identifiers** — il [Property guest name](#property-guest-name) e il [Guest access PIN](#guest-access-pin) — che collegano ogni ospite in modo sicuro all’assistente della proprietà corretta.

Puoi impostare o aggiornare questi identificatori da **My Properties** > _seleziona una proprietà_ > <img src="../media/modify-property-icon.png" alt="pencil icon" style="height: 1em; vertical-align: middle;">.

## Internal identifier

Il **Property Internal name** è usato solo dal tuo team nella dashboard. Aiuta te e lo staff a riconoscere e riferirsi alla proprietà in modo coerente.

- Non visibile agli ospiti  
- Può seguire qualsiasi convenzione di naming (es. `WILLOWST77-1A` per Willow Street 77, Appartamento 1A)  
- Deve essere univoco sulla piattaforma  
- Utile per evitare confusione quando gestisci più unità simili  

> **TIP** Usa nomi interni chiari e coerenti per identificare le proprietà a colpo d’occhio.

## Guest-facing identifiers

> **IMPORTANT**  
> **Leggi questa sezione con attenzione!** Spiega concetti chiave che influenzano direttamente l’esperienza degli ospiti con Alfred.

### Property guest name

Quando un ospite contatta il numero di Alfred, Alfred chiede in quale appartamento soggiorna e si aspetta il **Property guest name**.

Il **Property guest name** è mostrato agli ospiti nella chat di Alfred e negli altri touchpoint (Booking.com, Airbnb, comunicazioni dell’host, ecc.).

- Visibile agli ospiti  
- Deve essere univoco sulla piattaforma  
- Usato da Alfred per collegare l’ospite al chatbot corretto  
- Puoi modificarlo in qualsiasi momento da **My Properties**

> **WARNING**
> - Usa lo stesso identico nome che gli ospiti vedono su Booking.com o Airbnb per mantenere le comunicazioni coerenti.  
> - Condividi sempre il Property guest name insieme al **Guest access PIN**, altrimenti l’ospite non potrà accedere ad Alfred.

## Guest access PIN

Il **Guest access PIN** è un codice numerico breve (es. *4739*) usato per verificare che l’ospite sia tuo cliente.  
Impedisce a utenti non autorizzati di accedere ad Alfred e assicura che solo i veri ospiti possano interagire con l’assistente della proprietà.

- Deve essere univoco per ogni appartamento  
- Condiviso manualmente con gli ospiti dall’host  
- Funge da controllo di sicurezza prima dell’accesso alla chat  
- Puoi modificarlo in qualsiasi momento da **My Properties**

> **WARNING**
> - Condividi sempre il PIN insieme al **Property guest name**, altrimenti l’ospite non potrà accedere ad Alfred.  
> - Se modifichi il **Property guest name** o il **Guest access PIN**, aggiorna le tue comunicazioni (email, messaggi OTA, materiali stampati) per evitare confusione.

## Come funziona l’autenticazione degli ospiti

Quando un ospite contatta il numero di Alfred, deve autenticarsi con entrambi gli identificatori:

1. **Property guest name** — Alfred chiede in quale appartamento soggiorna. L’ospite deve fornire esattamente il Property guest name.
2. **Guest access PIN** — Alfred chiede poi il PIN per verificare l’identità.

> **IMPORTANT** Il Property guest name è **case sensitive**. Gli ospiti devono inserirlo esattamente come l’hai impostato, incluse maiuscole e minuscole. Ad esempio, se il nome è "Apartment 2B", inserire "apartment 2b" o "APARTMENT 2B" non funzionerà.

Se un ospite inserisce il PIN sbagliato, può riprovare. Assicurati di condividere chiaramente Property guest name e PIN per evitare problemi di autenticazione.
