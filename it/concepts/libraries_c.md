<div data-toc-depth="3"></div>

# Libraries

Nella piattaforma Alfred Co.Host, una **library** è l’insieme strutturato di informazioni che Alfred usa per rispondere alle domande degli ospiti per una specifica proprietà.

Ogni proprietà ha la sua library. Questa library contiene tutte le informazioni rilevanti sull’unità — da come accendere il riscaldamento a dove mangiare nei dintorni. Quando costruisci una library, raccogli e organizzi:

- **Informazioni sull’alloggio**: descrizioni generali (posizione, caratteristiche, zona, stile).
- **Dispositivi ed elettrodomestici**: istruzioni e troubleshooting (Wi-Fi, TV, elettrodomestici, ecc.).
- **Sistemi domestici e troubleshooting**: guida e troubleshooting (elettricità, acqua, riscaldamento, A/C).
- **Consigli locali**: suggerimenti per cibo, trasporti, visite e altre informazioni locali.
- **Policy e procedure**: regole della casa e istruzioni relative al soggiorno e al rapporto con l’host.
- **Info solo staff**: note interne per manutenzione o dettagli sugli ospiti. Visibili solo allo staff — mai mostrate agli ospiti.

> **NOTE** Più la library è ricca e chiara, più Alfred è utile.

## Come funziona

La library di ogni proprietà è composta da **unità di informazione**. Alcune sono predefinite, altre sono personalizzabili.

Quando Alfred identifica la proprietà dell’ospite, usa la library collegata per rispondere — che l’ospite chieda aiuto pratico, dettagli descrittivi o voglia raggiungere un host umano.

Le unità di informazione sono di due tipi: **Standard** (campi predefiniti) e **custom** (definibili da te).

L’informazione può essere **testuale** o **media**:

- [Standard textual information](#standard-textual-information)
- [Custom textual information](#custom-textual-information)
- [Standard media information](#standard-media-information)
- [Custom media information](#custom-media-information)

Alfred usa queste informazioni **così come sono** o le combina a seconda della complessità della richiesta.

### Standard textual information

Campi predefiniti in cui inserisci un valore testuale.  
Esempio:

| Information unit | Description | Custom value |
| --- | --- | --- |
| Property address | Indirizzo per localizzare la proprietà | `123 Oxford Street, London` |

Compila solo ciò che ti serve — lascia il resto vuoto.

### Custom textual information

Campi personalizzati in cui definisci sia l’etichetta sia il valore testuale.  
Esempio:

| Custom information unit | Custom description | Custom value |
| --- | --- | --- |
| `Parking instructions` | `Procedura per aprire il cancello del parcheggio` | `Use the garage remote stored in the kitchen cupboard` |

### Standard media information

Campi predefiniti in cui puoi aggiungere media (foto o video).  
Esempio:

| Information unit | Description | Value |
| --- | --- | --- |
| How to launch the washing machine | Tutorial per avviare il ciclo | `washing_machine_tutorial.mp4` |
| Fridge shelves detail | Dettaglio ripiani assegnati | `roomA_fridge_shelf.png` |

Formati supportati:
- image: JPG, JPEG, PNG fino a 25 Mb
- video: MP4, 3GP fino a 25 Mb

### Custom media information

Campi personalizzati in cui definisci etichetta, descrizione opzionale e file media.  
Esempio:

| Custom information unit | Custom description | Custom value |
| --- | --- | --- |
| `How to unlock the backyard door` | `Procedura per sbloccare la porta del giardino` | `backyard_door_opening_demo.mp4` |
| `How to open/close the terrace curtain` | `Dettaglio del meccanismo della tenda` | `curtain_lock.png` |

Formati supportati:
- image: JPG, JPEG, PNG fino a 25 Mb
- video: MP4, 3GP fino a 25 Mb
