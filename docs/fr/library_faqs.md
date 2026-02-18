# FAQ Bibliothèque

Questions fréquentes sur la rédaction et la gestion du contenu de la library pour vos propriétés.

## Questions générales

<details>
<summary><strong>Dois-je remplir tous les items standard ?</strong></summary>

Non. Remplissez uniquement ce qui est pertinent pour votre propriété. Laissez vides les items qui ne s’appliquent pas. Alfred n’utilise que les informations que vous fournissez.

En savoir plus : [À propos des libraries](/fr/concepts/libraries_c.md)

</details>

<details>
<summary><strong>Quick launch ou full control ?</strong></summary>

Vous pouvez choisir selon votre calendrier. Le **Quick launch (15 minutes)** vous met en ligne rapidement avec l’essentiel : check-in, policies, détails de base du logement. Le **Full control** vous permet de construire une library complète à votre rythme (appareils, systèmes, conseils locaux, custom items). Les deux approches fonctionnent.

En savoir plus : [Configurer votre bibliothèque](/fr/procedures/setup_library_p.md)

</details>

<details>
<summary><strong>Puis-je modifier les voci après les avoir créées ?</strong></summary>

Oui. Vous pouvez modifier toute voce à tout moment. Les changements sont pris en compte immédiatement.

En savoir plus : [Ajouter du contenu aux bibliothèques](/fr/procedures/libraries_p.md)

</details>

<details>
<summary><strong>Comment savoir si ma rédaction est suffisante ?</strong></summary>

Alfred comprend très bien ce que vous écrivez, même si ce n’est pas parfait. Pour de bons résultats, suivez nos [conseils d’écriture](/fr/procedures/writing_tips.md). L’important est d’être clair et précis — pensez à ce dont le voyageur a besoin pour résoudre son problème ou trouver ce qu’il cherche.

</details>

<details>
<summary><strong>Puis-je copier des voci entre propriétés ?</strong></summary>

Actuellement, chaque propriété a sa propre library. Vous devez ajouter les voci à chaque propriété séparément. Ainsi les informations restent exactes et spécifiques à chaque unité.

En savoir plus : [À propos des libraries](/fr/concepts/libraries_c.md)

</details>

## Rédaction

<details>
<summary><strong>Quelle longueur pour les voci ?</strong></summary>

Gardez les voci courtes et ciblées. Chaque voce doit couvrir **une seule information claire**. Pour des items simples (mot de passe Wi-Fi), quelques mots suffisent. Pour des procédures (ouvrir une keybox, réinitialiser la chaudière), utilisez des étapes numérotées courtes et logiques.

En savoir plus : [Writing custom items](/fr/procedures/writing_custom_items.md)

</details>

<details>
<summary><strong>Puis-je utiliser des abréviations ou du jargon technique ?</strong></summary>

Évitez les abréviations et le jargon interne. Écrivez comme si vous expliquiez à un voyageur en personne. Utilisez un langage clair et courant.

En savoir plus : [Conseils d’écriture](/fr/procedures/writing_tips.md)

</details>

<details>
<summary><strong>Ma propriété a des particularités non couvertes par les items standard</strong></summary>

Utilisez des custom items pour toute information non couverte par les champs standard. Voir [writing custom items](/fr/procedures/writing_custom_items.md).

</details>

<details>
<summary><strong>Faut-il inclure des photos ou vidéos ?</strong></summary>

Seulement si cela facilite l’explication. Les images et vidéos sont utiles **uniquement dans ce cas** — évitez de surcharger. Utilisez les champs **photo**, **video**, **instructions**. Ne collez pas de liens dans la description.

En savoir plus : [Rédiger de bonnes voci](/fr/procedures/writing_tips.md)

</details>

<details>
<summary><strong>À quel point être précis sur les emplacements ?</strong></summary>

Soyez aussi précis que possible. Donnez des **emplacements clairs et détaillés**. Au lieu de « dans la cuisine », écrivez « dans le placard sous l’évier de la cuisine ».

En savoir plus : [Rédiger de bonnes voci](/fr/procedures/writing_tips.md)

</details>

<details>
<summary><strong>Je ne sais pas comment rédiger quelque chose</strong></summary>

Partez du point de vue du voyageur : que cherche-t-il à faire ? Quand aura-t-il besoin de cette info ? Cette voce doit-elle instruire, informer, rassurer ou guider ? Puis rédigez une réponse claire et directe. En cas de doute, consultez notre [guide d’écriture](/fr/procedures/writing_tips.md).

</details>

## Custom items

<details>
<summary><strong>Quand créer un custom item ?</strong></summary>

Créez des custom items pour toute information non couverte par les champs standard (ex. instructions de parking, horaires des poubelles, particularités de la propriété).

En savoir plus : [Writing custom items](/fr/procedures/writing_custom_items.md)

</details>

<details>
<summary><strong>Comment fonctionnent les placeholders dans les custom items ?</strong></summary>

Pensez en placeholders : rédigez les items pour qu’ils s’intègrent bien dans les messages. Par exemple, un item « Garbage collection times » avec la valeur « de 18h30 à 22h30 » peut être inséré dans un message du type : « N’oubliez pas que les poubelles peuvent être sorties {garbage_collection_times}. »

En savoir plus : [Writing custom items](/fr/procedures/writing_custom_items.md)

</details>

<details>
<summary><strong>Puis-je mettre plusieurs informations dans un seul custom item ?</strong></summary>

Non. Chaque voce doit porter sur **une seule information claire**. Si vous avez plusieurs détails liés, créez une voce par détail. Alfred trouvera et utilisera ainsi la bonne information.

En savoir plus : [Writing custom items](/fr/procedures/writing_custom_items.md)

</details>

<details>
<summary><strong>Quelle est la différence entre items standard et custom ?</strong></summary>

Les items standard sont des champs prédéfinis (mot de passe Wi-Fi, heure de check-in, etc.). Les custom items permettent d’ajouter toute autre information spécifique à votre propriété. Les deux fonctionnent de la même façon pour Alfred.

En savoir plus : [À propos des libraries](/fr/concepts/libraries_c.md), [Writing custom items](/fr/procedures/writing_custom_items.md)

</details>

## Policies

<details>
<summary><strong>Que sont les policies et en quoi diffèrent-elles des voci classiques ?</strong></summary>

Les policies sont des voci spéciales qui contrôlent le comportement d’Alfred dans des situations données. Elles ne sont jamais montrées directement aux voyageurs. Elles indiquent à Alfred quoi faire ou dire lorsque certaines conditions sont remplies.

En savoir plus : [Writing internal policies](/fr/procedures/writing_policies.md)

</details>

<details>
<summary><strong>Dois-je créer des policies personnalisées ?</strong></summary>

Nous avons déjà défini les policies de base. Vous ne devez créer des policies personnalisées que pour des situations nécessitant un traitement particulier. Structure : **Trigger**, **Action**, **Message** (si besoin). Voir [writing policies](/fr/procedures/writing_policies.md).

</details>

## Dépannage

<details>
<summary><strong>Alfred n’utilise pas correctement mes voci</strong></summary>

Vérifiez que vos voci sont : claires et précises ; centrées sur une seule information ; rédigées du point de vue du voyageur ; sans mots vagues (« disponible », « présent »). Vérifiez aussi que les custom items ont des libellés clairs.

En savoir plus : [Rédiger de bonnes voci](/fr/procedures/writing_tips.md), [Writing custom items](/fr/procedures/writing_custom_items.md)

</details>

<details>
<summary><strong>Puis-je tester comment Alfred utilisera ma library ?</strong></summary>

Oui. Utilisez la fonction test assistant pour voir comment Alfred répond aux questions. Ainsi vous vérifiez le comportement avant la mise en ligne.

En savoir plus : [Test assistant](/fr/procedures/test_assistant.md)

</details>

<details>
<summary><strong>Que se passe-t-il si je laisse un item vide ?</strong></summary>

Rien. Alfred n’utilisera simplement pas cette information. Les voyageurs ne verront pas de champs vides ni de messages d’erreur.

En savoir plus : [À propos des libraries](/fr/concepts/libraries_c.md)

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
