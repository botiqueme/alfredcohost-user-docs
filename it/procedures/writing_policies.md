# 📜 Writing internal policies

Le policy sono un tipo speciale di voce di library usato per controllare il comportamento di Alfred in situazioni specifiche. Non vengono **mai mostrate direttamente agli ospiti**. Definiscono cosa deve fare o dire Alfred quando si verificano certe condizioni — ad esempio quando un ospite segnala un problema, chiede servizi extra o prova a fare check-in fuori orario.

Abbiamo già definito le policy di base per Alfred. Se devi crearne di personalizzate, questi consigli ti aiutano.

## 🧠 Cosa serve per una buona policy

Una policy ben scritta deve:
- Essere **specifica** sullo scenario a cui si applica
- Definire chiaramente **cosa deve fare Alfred** (passare a un umano? inviare un messaggio? non fare nulla?)
- Includere **cosa deve dire Alfred** se serve un messaggio all’ospite
- Essere scritta in **linguaggio naturale** (niente placeholders, niente gergo tecnico)

## ✅ Struttura da seguire

Prima di scrivere una policy, delimita bene l’ambito: Quale situazione? Quando inizia? Quando finisce?

Poi usa questa struttura:

1. **Trigger**  
   Descrivi la condizione che attiva la policy.  
   _Esempio: “Se l’ospite segnala di aver perso le chiavi…”_

2. **Action**  
   Descrivi cosa deve fare Alfred.  
   _Esempio: “Passare la chat a un operatore umano.”_

3. **Message (se necessario)**  
   Fornisci il messaggio esatto che Alfred deve inviare.  
   _Esempio: “Nessun problema, ti rispondiamo al più presto!”_

---

### Vedi anche

- [Come scrivere ottime voci di biblioteca](/it/procedures/writing_tips.md) — Principi e tono
- [Writing custom items](/it/procedures/writing_custom_items.md) — Aggiungere informazioni specifiche della proprietà
