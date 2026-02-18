# Translation Audit Report

Audit of untranslated English terms found in `fr/`, `it/`, `es/` documentation files.

Use this report to:
1. Decide which terms should be **translated** vs. kept in English (UI labels, product features)
2. Populate the **glossary files** (`_glossary.md`) for each language
3. Fix untranslated content in the documentation

---

## Decision needed: Translate or Keep in English?

Before fixing files, decide on each category below. Terms marked with **UI** are labels that appear in the Alfred platform interface — keeping them in English may help users match docs to the actual UI.

### Category 1: Platform Concepts (appear everywhere)

| English term | Suggested FR | Suggested IT | Suggested ES | Decision needed |
|---|---|---|---|---|
| library / libraries | bibliothèque(s) | biblioteca/biblioteche | biblioteca(s) | Translate or keep? |
| property / properties | propriété(s) | proprietà | propiedad(es) | Translate or keep? |
| subscription(s) | abonnement(s) | abbonamento/i | suscripción(es) | Translate or keep? |
| billing cycle | cycle de facturation | ciclo di fatturazione | ciclo de facturación | Translate or keep? |
| plan | plan / forfait | piano | plan | Translate or keep? |
| custom item(s) | élément(s) personnalisé(s) | elemento/i personalizzato/i | elemento(s) personalizado(s) | Translate or keep? |
| item(s) (standard) | élément(s) | elemento/i | elemento(s) | Translate or keep? |
| policy / policies | règle(s) interne(s) | regola/e interna/e | política(s) interna(s) | Translate or keep? |
| monthly / yearly | mensuel / annuel | mensile / annuale | mensual / anual | Translate or keep? |

### Category 2: Feature Names

| English term | Suggested FR | Suggested IT | Suggested ES | Decision needed |
|---|---|---|---|---|
| Hands off | Transfert humain | Passaggio umano | Transferencia humana | Translate or keep? |
| Hands off number | Numéro de transfert | Numero di passaggio | Número de transferencia | Translate or keep? |
| Phone number | Numéro de téléphone | Numero di telefono | Número de teléfono | Translate or keep? |
| Guest contact number | Numéro de contact voyageur | Numero di contatto ospite | Número de contacto huésped | Translate or keep? |
| Go live | Mise en ligne | Messa online | Puesta en línea | Translate or keep? |
| Quick launch | Lancement rapide | Avvio rapido | Lanzamiento rápido | Translate or keep? |
| Full control | Contrôle total | Controllo completo | Control total | Translate or keep? |
| Test assistant | Tester l'assistant | Testare l'assistente | Probar el asistente | Translate or keep? |
| Quickstart | Démarrage rapide | Avvio rapido | Inicio rápido | Translate or keep? |
| Hospitality AI | IA hôtelière | IA per l'ospitalità | IA de hospitalidad | Translate or keep? |

### Category 3: UI Labels (bold in docs, match platform interface)

| English term | Context | Translate or keep as-is? |
|---|---|---|
| **My Properties** | Navigation menu | |
| **My subscriptions** | Navigation menu | |
| **My Host Profile** | Navigation menu | |
| **My saved card** | Navigation menu | |
| **Manage my properties** | Navigation menu | |
| **Add a property** | Button | |
| **Go live** (toggle) | Toggle switch in My Properties | |
| **Save** | Button | |
| **Delete** | Button | |
| **Add custom info** | Button | |
| **Info type** | Form field label | |
| **friendly label** | Form field label | |
| **short description** | Form field label | |
| **Item Category** | Navigation label | |
| **Item Categories** | Navigation label | |
| **Subcategory** | Navigation label | |

### Category 4: Library Item Category Names (bold section headings)

| English term | Context | Translate or keep? |
|---|---|---|
| **Check-in information** | Item category in library setup | |
| **Policies** | Item category in library setup | |
| **Accommodation information** | Item category in library setup | |
| **Devices and appliances** | Item category in library setup | |
| **Household systems** | Item category in library setup | |
| **Local tips** | Item category in library setup | |
| **Custom items** | Item category in library setup | |

### Category 5: Property Identifier Terms

| English term | Context | Translate or keep? |
|---|---|---|
| Property Internal name | Dashboard identifier | |
| Property guest name | Guest-facing identifier | |
| Guest access PIN | Authentication code | |
| Guest-facing identifiers | Heading/concept | |
| Internal identifier | Heading/concept | |
| case sensitive | Description of name matching | |

### Category 6: Policy Structure Terms

| English term | Context | Translate or keep? |
|---|---|---|
| **Trigger** | Policy component | |
| **Action** | Policy component | |
| **Message** | Policy component | |

### Category 7: Library Table Content

| English term | Context | Translate or keep? |
|---|---|---|
| Information unit / Description / Custom value | Table headers in libraries_c.md | |
| Standard textual information | Section heading | |
| Custom textual information | Section heading | |
| Standard media information | Section heading | |
| Custom media information | Section heading | |
| Property address | Table example | |
| Parking instructions | Table example | |
| How to launch the washing machine | Table example | |
| Fridge shelves detail | Table example | |
| How to unlock the backyard door | Table example | |
| How to open/close the terrace curtain | Table example | |

### Category 8: Writing Guide Example Labels

| English term | Context | Translate or keep? |
|---|---|---|
| Garbage collection times | Example item name | |
| Hot water information | Example item name | |
| Hot water system location | Example item name | |
| Hot water ON/OFF button location | Example item name | |
| Main water valve location | Example item name | |
| Keybox instructions | Example item name | |

### Category 9: Document Titles & Link Text

| English term | Context | Translate or keep? |
|---|---|---|
| Writing custom items | Page title and link text | |
| Writing internal policies | Page title and link text | |
| Test assistant | Page title and link text | |
| Work on Alfred setup | Section heading and link text | |
| Setup & Library | Section heading | |

### Category 10: Other English Terms

| English term | Context | Translate or keep? |
|---|---|---|
| check-in / check-out | Hospitality terms | |
| staff | Library visibility label | |
| host | Role description | |
| dashboard | Platform UI area | |
| touchpoints | Channels where Alfred appears | |
| troubleshooting | Description of support type | |
| handoff | Alternative for "hands off" | |
| placeholders | Custom item concept | |
| guesthouse | Accommodation type example | |
| **Example** | Admonition label in blockquotes | |
| **photo** / **video** / **instructions** | Form field labels | |

---

## Special Issue: Italian words in French docs

The French (`fr/`) files contain Italian words **"voci"** (plural) and **"voce"** (singular) instead of French equivalents. These appear in:
- `fr/library_faqs.md` (~15 occurrences)
- `fr/procedures/writing_tips.md` (~3 occurrences)
- `fr/procedures/writing_custom_items.md` (~2 occurrences)
- `fr/procedures/writing_policies.md` (~2 occurrences)
- `fr/procedures/libraries_p.md` (~2 occurrences)
- `fr/concepts/what-alfred-can-do_c.md` (~1 occurrence)
- `fr/procedures/test_assistant.md` (~1 occurrence)

Suggested French replacement: **"entrées"**, **"éléments"**, or **"fiches"** (depending on context).

---

## Files Affected per Language

### French (fr/) — All content files affected
| File | Severity |
|---|---|
| fr/library_faqs.md | HIGH — many untranslated terms + Italian words |
| fr/concepts/plans_billing_cycles_c.md | HIGH — billing/subscription terms throughout |
| fr/concepts/libraries_c.md | HIGH — table content entirely in English |
| fr/concepts/property-identifiers_c.md | HIGH — identifier terms throughout |
| fr/procedures/setup_library_p.md | HIGH — category names in English |
| fr/procedures/subscriptions_p.md | HIGH — subscription/billing terms |
| fr/procedures/libraries_p.md | HIGH — UI labels in English |
| fr/concepts/hands_off_c.md | MEDIUM |
| fr/get-started.md | MEDIUM |
| fr/procedures/writing_custom_items.md | MEDIUM |
| fr/procedures/writing_tips.md | MEDIUM |
| fr/procedures/writing_policies.md | MEDIUM |
| fr/procedures/properties_p.md | MEDIUM |
| fr/procedures/change_payment_card_p.md | LOW |
| fr/procedures/test_assistant.md | LOW |
| fr/home.md / fr/README.md | LOW — card titles only |
| fr/concepts/intro.md | LOW |
| fr/concepts/what-alfred-can-do_c.md | MEDIUM |
| fr/concepts/properties_c.md | LOW |
| fr/procedures/intro.md | MEDIUM |

### Italian (it/) — All content files affected
Same files, same severity distribution as French (without the Italian-words-in-French issue).

### Spanish (es/) — All content files affected
Same files, same severity distribution as French.

---

## Glossary Population Guide

Once you've decided which terms to translate, add them to each language's `_glossary.md`:

```markdown
## Library
Bibliothèque — L'ensemble structuré d'informations de chaque propriété.

## Property
Propriété — Chaque logement géré sur la plateforme Alfred.

## Subscription
Abonnement — Accord actif liant une propriété à un plan.
```

Terms you decide to **keep in English** should also go in the glossary with an explanation:

```markdown
## Hands off
Hands off — Fonction de transfert vers le support humain quand Alfred ne peut pas résoudre une demande.
```
