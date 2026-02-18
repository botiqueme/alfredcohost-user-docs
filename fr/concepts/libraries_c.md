<div data-toc-depth="3"></div>

# Libraries

Sur la plateforme Alfred Co.Host, une **library** est l’ensemble structuré d’informations qu’Alfred utilise pour répondre aux questions des voyageurs pour une propriété donnée.

Chaque propriété a sa propre library. Cette library contient toutes les informations pertinentes sur l’unité — du réglage du chauffage aux bonnes adresses à proximité. Lorsque vous construisez une library, vous rassemblez et organisez :

- **Informations sur le logement** : description générale (emplacement, caractéristiques, surface, style).
- **Appareils et équipements** : instructions et dépannage (Wi-Fi, TV, électroménager, etc.).
- **Systèmes domestiques et dépannage** : conseils et dépannage (électricité, eau, chauffage, climatisation).
- **Conseils locaux** : suggestions (restaurants, transports, visites).
- **Politiques et procédures** : règles de la maison et instructions liées au séjour et à la relation avec l’hôte.
- **Infos réservées au staff** : notes internes (maintenance, détails voyageurs). Visible uniquement par le staff — jamais montré aux voyageurs.

> **NOTE** Plus votre library est riche et claire, plus Alfred est utile.

## Comment ça marche

La library de chaque propriété est constituée d’**unités d’information**. Certaines sont prédéfinies, d’autres sont entièrement personnalisables.

Quand Alfred identifie la propriété du voyageur, il utilise la library associée pour répondre — que le voyageur demande de l’aide pratique, des détails descriptifs ou souhaite joindre un humain.

Les unités d’information sont de deux types : **Standard** (champs prédéfinis) et **custom** (que vous définissez).

L’information peut être **textuelle** ou **média** :

- [Standard textual information](#standard-textual-information)
- [Custom textual information](#custom-textual-information)
- [Standard media information](#standard-media-information)
- [Custom media information](#custom-media-information)

Alfred utilise cette information **telle quelle** ou la combine selon la complexité de la demande.

### Standard textual information

Champs prédéfinis où vous saisissez une valeur texte.  
Exemple :

| Information unit | Description | Custom value |
| --- | --- | --- |
| Property address | Adresse pour localiser la propriété | `123 Oxford Street, London` |

Remplissez uniquement ce dont vous avez besoin — laissez le reste vide.

### Custom textual information

Champs personnalisés où vous définissez le libellé et la valeur texte.  
Exemple :

| Custom information unit | Custom description | Custom value |
| --- | --- | --- |
| `Parking instructions` | `Procédure pour ouvrir le portail` | `Use the garage remote stored in the kitchen cupboard` |

### Standard media information

Champs prédéfinis où vous pouvez ajouter un média (photo ou vidéo).  
Exemple :

| Information unit | Description | Value |
| --- | --- | --- |
| How to launch the washing machine | Tutoriel pour lancer un cycle | `washing_machine_tutorial.mp4` |
| Fridge shelves detail | Détail des étagères attribuées | `roomA_fridge_shelf.png` |

Formats supportés :
- image : JPG, JPEG, PNG jusqu’à 25 Mo
- video : MP4, 3GP jusqu’à 25 Mo

### Custom media information

Champs personnalisés où vous définissez le libellé, une description optionnelle et le fichier média.  
Exemple :

| Custom information unit | Custom description | Custom value |
| --- | --- | --- |
| `How to unlock the backyard door` | `Procédure pour déverrouiller la porte du jardin` | `backyard_door_opening_demo.mp4` |
| `How to open/close the terrace curtain` | `Détail du mécanisme du rideau` | `curtain_lock.png` |

Formats supportés :
- image : JPG, JPEG, PNG jusqu’à 25 Mo
- video : MP4, 3GP jusqu’à 25 Mo
