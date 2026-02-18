# Property identifiers

Chaque propriété dans Alfred Co.Host est définie par trois identifiants qui la rendent reconnaissable en interne et pour vos voyageurs.  
**Ces identifiants sont essentiels au bon fonctionnement d’Alfred** : ils permettent à la plateforme d’associer le bon chatbot au bon appartement et d’assurer une expérience fluide.

Sur cette page vous découvrirez les trois identifiants qui permettent l’automatisation et les échanges avec les voyageurs :  
- L’[Internal identifier](#internal-identifier), utilisé uniquement dans votre dashboard pour la gestion des propriétés.  
- Les **Guest-facing identifiers** — le [Property guest name](#property-guest-name) et le [Guest access PIN](#guest-access-pin) — qui connectent chaque voyageur de façon sécurisée au bon assistant.

Vous pouvez définir ou modifier ces identifiants dans **My Properties** > _sélectionner une propriété_ > <img src="../media/modify-property-icon.png" alt="pencil icon" style="height: 1em; vertical-align: middle;">.

## Internal identifier

Le **Property Internal name** est utilisé uniquement par votre équipe dans le dashboard. Il vous permet de reconnaître et désigner la propriété de façon cohérente.

- Non visible par les voyageurs  
- Peut suivre toute convention de nommage (ex. `WILLOWST77-1A` pour Willow Street 77, Appartement 1A)  
- Doit être unique sur la plateforme  
- Utile pour éviter les confusions quand vous gérez plusieurs unités similaires  

> **TIP** Utilisez des noms internes clairs et cohérents pour identifier les propriétés en un coup d’œil.

## Guest-facing identifiers

> **IMPORTANT**  
> **Lisez cette section attentivement !** Elle explique des concepts clés qui influencent directement l’expérience des voyageurs avec Alfred.

### Property guest name

Lorsqu’un voyageur contacte le numéro d’Alfred, Alfred lui demande dans quel appartement il séjourne et attend le **Property guest name**.

Le **Property guest name** est affiché aux voyageurs dans le chat Alfred et sur les autres touchpoints (Booking.com, Airbnb, communications de l’hôte, etc.).

- Visible par les voyageurs  
- Doit être unique sur la plateforme  
- Utilisé par Alfred pour associer le voyageur au bon chatbot  
- Vous pouvez le modifier à tout moment dans **My Properties**

> **WARNING**
> - Utilisez exactement le même nom que les voyageurs voient sur Booking.com ou Airbnb pour garder les communications cohérentes.  
> - Partagez toujours le Property guest name avec le **Guest access PIN**, sinon le voyageur ne pourra pas accéder à Alfred.

## Guest access PIN

Le **Guest access PIN** est un code numérique court (ex. *4739*) utilisé pour vérifier que le voyageur est bien votre client.  
Il évite que des utilisateurs non autorisés accèdent à Alfred et garantit que seuls les vrais voyageurs peuvent interagir avec l’assistant de la propriété.

- Doit être unique pour chaque appartement  
- Partagé manuellement avec les voyageurs par l’hôte  
- Sert de contrôle de sécurité léger avant l’accès au chat  
- Vous pouvez le modifier à tout moment dans **My Properties**

> **WARNING**
> - Partagez toujours le PIN avec le **Property guest name**, sinon le voyageur ne pourra pas accéder à Alfred.  
> - Si vous changez le **Property guest name** ou le **Guest access PIN**, mettez à jour vos supports (emails, messages OTA, documents imprimés) pour éviter toute confusion.

## Comment fonctionne l’authentification des voyageurs

Lorsqu’un voyageur contacte le numéro d’Alfred, il doit s’authentifier avec les deux identifiants :

1. **Property guest name** — Alfred demande dans quel appartement il séjourne. Le voyageur doit donner exactement le Property guest name.
2. **Guest access PIN** — Alfred demande ensuite le PIN pour vérifier son identité.

> **IMPORTANT** Le Property guest name est **sensible à la casse**. Les voyageurs doivent le saisir exactement comme vous l’avez défini (majuscules et minuscules). Par exemple, si le nom est "Apartment 2B", saisir "apartment 2b" ou "APARTMENT 2B" ne fonctionnera pas.

En cas de PIN incorrect, le voyageur peut réessayer. Pensez à partager clairement le Property guest name et le PIN pour éviter les problèmes d’authentification.
