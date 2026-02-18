# Writing custom items

Nous avons déjà défini les principales informations dont vos voyageurs peuvent avoir besoin. Vous pouvez ajouter des custom items à vos [libraries](/fr/concepts/libraries_c.md) pour couvrir des détails supplémentaires. Suivez ces conseils pour qu’Alfred dispose des informations les plus précises sur votre propriété et vos policies.

## 💡 Pensez en placeholders

Rédigez vos items pour qu’ils s’intègrent naturellement dans les messages aux voyageurs.

> **Example**
> - **Garbage collection times** : « de 18h30 à 22h30 »
> - **Message au voyageur** : « N’oubliez pas que les poubelles peuvent être sorties {garbage_collection_times}. »

## 🥵 Ne surchargez pas un seul item

Chaque voce de library doit porter sur **une seule information claire**. Les items standard ne contiennent qu’un seul contenu. Pour les custom items, séparez les types d’information dans des entrées distinctes.

> **Example** ❌ **Hot water information** : « Chaudière au-dessus du bidet. Bouton en dessous. Si pas d’eau chaude, ouvrir le robinet sous l’évier. »  
> ✅ À scinder en plusieurs items :  
> - **Hot water system location** : « Au-dessus du bidet dans la salle de bain »  
> - **Hot water ON/OFF button location** : « Sous la chaudière dans la salle de bain »  
> - **Main water valve location** : « Sous l’évier de la cuisine »

## ✍️ Instructions pas à pas si besoin

Pour des procédures (ouvrir un coffre à clé, réinitialiser la chaudière), utilisez des étapes numérotées courtes et logiques.

> **Example** ✅ **Keybox instructions** :  
> 1. Tournez les molettes pour composer le code.  
> 2. Tirez le levier noir vers le bas.  
> 3. Après usage, brouillez le code pour le garder confidentiel.

---

### Voir aussi

- [Comment rédiger de bonnes voci de bibliothèque](/fr/procedures/writing_tips.md) — Principes et ton pour un contenu efficace
- [Writing internal policies](/fr/procedures/writing_policies.md) — Contrôler quand Alfred transfère les conversations ou prend des actions
