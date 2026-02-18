# Writing custom items

Abbiamo già mappato le informazioni principali di cui i tuoi ospiti possono aver bisogno. Puoi aggiungere custom items alle tue [libraries](/it/concepts/libraries_c.md) per coprire dettagli extra. Segui questi consigli per dare ad Alfred le informazioni più accurate su proprietà e policy.

## 💡 Pensa in placeholders

Scrivi le voci in modo che funzionino bene dentro i messaggi agli ospiti.

> **Example**
> - **Garbage collection times**: “dalle 18:30 alle 22:30”
> - **Messaggio all’ospite**: “Ricorda che i rifiuti possono essere portati fuori {garbage_collection_times}.”

## 🥵 Non sovraccaricare un solo item

Ogni voce di library deve concentrarsi su **un’unica informazione chiara**. Gli item standard contengono un solo contenuto. Quando crei custom items, separa tipi diversi di informazione in voci distinte.

> **Example** ❌ **Hot water information**: “Caldaia sopra il bidet. Pulsante sotto. Se niente acqua calda, apri la valvola sotto il lavello in cucina.”  
> ✅ Suddiviso in più item:  
> - **Hot water system location**: “Sopra il bidet in bagno”  
> - **Hot water ON/OFF button location**: “Sotto la caldaia in bagno”  
> - **Main water valve location**: “Sotto il lavello in cucina”

## ✍️ Istruzioni passo passo quando servono

Per procedure come aprire una keybox o resettare la caldaia, usa passi brevi e numerati in ordine logico.

> **Example** ✅ **Keybox instructions**:  
> 1. Ruota i dischi per impostare il codice.  
> 2. Abbassa la leva nera.  
> 3. Dopo l’uso, mescola il codice per tenerlo privato.

---

### Vedi anche

- [Come scrivere ottime voci di biblioteca](/it/procedures/writing_tips.md) — Principi e tono per contenuti efficaci
- [Writing internal policies](/it/procedures/writing_policies.md) — Controllare quando Alfred trasferisce le conversazioni o compie azioni
