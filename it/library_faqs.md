# FAQ Biblioteca

Domande comuni su scrittura e gestione del contenuto della library per le tue proprietà.

## Domande generali

<details>
<summary><strong>Devo compilare tutti gli item standard?</strong></summary>

No. Compila solo ciò che è rilevante per la tua proprietà. Lascia vuoti gli item che non si applicano. Alfred userà solo le informazioni che fornisci.

Per saperne di più: [Le libraries](/it/concepts/libraries_c.md)

</details>

<details>
<summary><strong>Quick launch o full control?</strong></summary>

Puoi scegliere in base ai tuoi tempi. Il **Quick launch (15 minuti)** ti porta online velocemente con l’essenziale: check-in, policy, dettagli base dell’alloggio. Il **Full control** ti permette di costruire una library completa con calma. Entrambi gli approcci funzionano.

Per saperne di più: [Configurare la biblioteca](/it/procedures/setup_library_p.md)

</details>

<details>
<summary><strong>Posso modificare le voci dopo averle create?</strong></summary>

Sì. Puoi modificare qualsiasi voce in qualsiasi momento. Le modifiche hanno effetto immediato.

Per saperne di più: [Aggiungere contenuti alle libraries](/it/procedures/libraries_p.md)

</details>

<details>
<summary><strong>Come faccio a sapere se la mia scrittura è sufficiente?</strong></summary>

Alfred capisce molto bene ciò che scrivi. Per risultati migliori segui i nostri [consigli di scrittura](/it/procedures/writing_tips.md). L’importante è essere chiari e specifici — pensa a cosa serve all’ospite per risolvere il problema o trovare ciò che cerca.

</details>

<details>
<summary><strong>Posso copiare voci tra proprietà?</strong></summary>

Attualmente ogni proprietà ha la propria library. Devi aggiungere le voci a ogni proprietà separatamente. Così le informazioni restano accurate e specifiche per ogni unità.

Per saperne di più: [Le libraries](/it/concepts/libraries_c.md)

</details>

## Scrittura

<details>
<summary><strong>Quanto devono essere lunghe le voci?</strong></summary>

Mantieni le voci brevi e focalizzate. Ogni voce deve coprire **un’unica informazione chiara**. Per item semplici (password Wi-Fi) bastano poche parole. Per procedure (aprire keybox, resettare caldaia) usa passi numerati brevi e logici.

Per saperne di più: [Writing custom items](/it/procedures/writing_custom_items.md)

</details>

<details>
<summary><strong>Posso usare abbreviazioni o termini tecnici?</strong></summary>

Evita abbreviazioni e gergo interno. Scrivi come se stessi spiegando a un ospite di persona. Usa un linguaggio chiaro e quotidiano.

Per saperne di più: [Consigli di scrittura](/it/procedures/writing_tips.md)

</details>

<details>
<summary><strong>La mia proprietà ha caratteristiche non coperte dagli item standard</strong></summary>

Usa custom items per qualsiasi informazione non coperta dai campi standard. Vedi [writing custom items](/it/procedures/writing_custom_items.md).

</details>

<details>
<summary><strong>Devo includere foto o video?</strong></summary>

Solo se rendono più chiara la spiegazione. Immagini e video sono utili **solo in quel caso** — evita di sovraccaricare. Usa i campi **photo**, **video**, **instructions**. Non incollare link nella descrizione.

Per saperne di più: [Scrivere ottime voci](/it/procedures/writing_tips.md)

</details>

<details>
<summary><strong>Quanto essere specifici sulle posizioni?</strong></summary>

Sii il più preciso possibile. Scrivi **posizioni chiare e dettagliate**. Invece di "in cucina", scrivi "nello sportello sotto il lavello in cucina".

Per saperne di più: [Scrivere ottime voci](/it/procedures/writing_tips.md)

</details>

<details>
<summary><strong>Non sono sicuro di come scrivere qualcosa</strong></summary>

Parti dal punto di vista dell’ospite: cosa sta cercando di fare? Quando avrà bisogno di questa informazione? La voce deve istruire, informare, rassicurare o guidare? Poi scrivi una risposta chiara e diretta. In caso di dubbio consulta la nostra [guida alla scrittura](/it/procedures/writing_tips.md).

</details>

## Custom items

<details>
<summary><strong>Quando creare un custom item?</strong></summary>

Crea custom items quando devi aggiungere informazioni non coperte dai campi standard (es. istruzioni parcheggio, orari rifiuti, caratteristiche uniche della proprietà).

Per saperne di più: [Writing custom items](/it/procedures/writing_custom_items.md)

</details>

<details>
<summary><strong>Come funzionano i placeholder nei custom items?</strong></summary>

Pensa in placeholders: scrivi le voci in modo che funzionino bene nei messaggi. Es. un item "Garbage collection times" con valore "dalle 18:30 alle 22:30" può essere inserito in un messaggio tipo: "Ricorda che i rifiuti possono essere portati fuori {garbage_collection_times}."

Per saperne di più: [Writing custom items](/it/procedures/writing_custom_items.md)

</details>

<details>
<summary><strong>Posso mettere più informazioni in un solo custom item?</strong></summary>

No. Ogni voce deve concentrarsi su **un’unica informazione chiara**. Se hai più dettagli correlati, crea una voce per ciascuno. Alfred troverà e userà l’informazione giusta.

Per saperne di più: [Writing custom items](/it/procedures/writing_custom_items.md)

</details>

<details>
<summary><strong>Qual è la differenza tra item standard e custom?</strong></summary>

Gli item standard sono campi predefiniti (password Wi-Fi, orario check-in, ecc.). I custom items permettono di aggiungere qualsiasi altra informazione specifica della proprietà. Entrambi funzionano allo stesso modo per Alfred.

Per saperne di più: [Le libraries](/it/concepts/libraries_c.md), [Writing custom items](/it/procedures/writing_custom_items.md)

</details>

## Policy

<details>
<summary><strong>Cosa sono le policy e come differiscono dalle voci normali?</strong></summary>

Le policy sono voci speciali che controllano il comportamento di Alfred in situazioni specifiche. Non vengono mai mostrate direttamente agli ospiti. Indicano ad Alfred cosa fare o dire quando si verificano certe condizioni.

Per saperne di più: [Writing internal policies](/it/procedures/writing_policies.md)

</details>

<details>
<summary><strong>Devo creare policy personalizzate?</strong></summary>

Abbiamo già definito le policy di base. Devi creare policy personalizzate solo per situazioni che richiedono una gestione particolare. Struttura: **Trigger**, **Action**, **Message** (se serve). Vedi [writing policies](/it/procedures/writing_policies.md).

</details>

## Risoluzione problemi

<details>
<summary><strong>Alfred non usa correttamente le mie voci</strong></summary>

Verifica che le voci siano: chiare e specifiche; focalizzate su un’unica informazione; scritte dal punto di vista dell’ospite; senza parole vaghe ("disponibile", "presente"). Verifica anche che i custom items abbiano etichette chiare.

Per saperne di più: [Scrivere ottime voci](/it/procedures/writing_tips.md), [Writing custom items](/it/procedures/writing_custom_items.md)

</details>

<details>
<summary><strong>Posso testare come Alfred userà la mia library?</strong></summary>

Sì. Usa la funzione test assistant per vedere come Alfred risponde alle domande. Così verifichi il comportamento prima di andare online.

Per saperne di più: [Test assistant](/it/procedures/test_assistant.md)

</details>

<details>
<summary><strong>Cosa succede se lascio un item vuoto?</strong></summary>

Niente. Alfred semplicemente non userà quell’informazione. Gli ospiti non vedranno campi vuoti né messaggi di errore.

Per saperne di più: [Le libraries](/it/concepts/libraries_c.md)

</details>

<style>
.markdown-section details { margin-bottom: 0; border-bottom: 1px solid #FF3B3C; padding-bottom: 0.75rem; margin-bottom: 0.75rem; }
.markdown-section details:last-child { border-bottom: none; margin-bottom: 0; }
.markdown-section details summary { font-size: 1.25rem; font-weight: 600; cursor: pointer; list-style: none; padding: 0.75rem 0; position: relative; padding-left: 1.5rem; }
.markdown-section details summary::-webkit-details-marker { display: none; }
.markdown-section details summary::before { content: ''; position: absolute; left: 0; top: 50%; transform: translateY(-50%) rotate(-45deg); width: 8px; height: 8px; border-right: 2px solid #FF3B3C; border-bottom: 2px solid #FF3B3C; transition: transform 0.2s ease; }
.markdown-section details[open] summary::before { transform: translateY(-50%) rotate(45deg); }
.markdown-section details[open] summary { margin-bottom: 1rem; }
.markdown-section details + h2 { margin-top: 2.5rem; }
</style>
