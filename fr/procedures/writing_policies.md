# 📜 Writing internal policies

Les policies sont un type particulier de voce de library utilisé pour contrôler le comportement d’Alfred dans des situations données. Elles ne sont **jamais montrées directement aux voyageurs**. Elles définissent ce qu’Alfred doit faire ou dire lorsque certaines conditions sont remplies — par exemple quand un voyageur signale un problème, demande un service supplémentaire ou tente un check-in hors horaires.

Nous avons déjà défini les policies de base pour Alfred. Si vous devez en créer des personnalisées, ces conseils vous aideront.

## 🧠 Ce qu’il faut pour une bonne policy

Une policy bien rédigée doit :
- Être **précise** sur le scénario concerné
- Définir clairement **ce qu’Alfred doit faire** (transférer à un humain ? envoyer un message ? ne rien faire ?)
- Inclure **ce qu’Alfred doit dire** si un message au voyageur est nécessaire
- Être rédigée en **langage naturel** (pas de placeholders, pas de jargon technique)

## ✅ Structure à suivre

Avant d’écrire une policy, délimitez bien le périmètre : Quelle situation ? Quand commence-t-elle ? Quand se termine-t-elle ?

Ensuite utilisez cette structure :

1. **Trigger**  
   Décrivez la condition qui active la policy.  
   _Exemple : « Si le voyageur signale avoir perdu les clés… »_

2. **Action**  
   Décrivez ce qu’Alfred doit faire.  
   _Exemple : « Transférer la conversation à un agent humain. »_

3. **Message (si besoin)**  
   Donnez le message exact qu’Alfred doit envoyer.  
   _Exemple : « Pas d’inquiétude, nous vous recontactons rapidement ! »_

---

### Voir aussi

- [Comment rédiger de bonnes voci de bibliothèque](/fr/procedures/writing_tips.md) — Principes et ton
- [Writing custom items](/fr/procedures/writing_custom_items.md) — Ajouter des informations spécifiques à la propriété
