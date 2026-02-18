# Property identifiers

Cada propiedad en Alfred Co.Host se define por tres identificadores que la hacen reconocible tanto internamente como para tus huéspedes.  
**Estos identificadores son esenciales para que Alfred funcione correctamente**: permiten a la plataforma vincular el chatbot correcto al apartamento correcto y garantizar una experiencia fluida.

En esta página conocerás los tres identificadores que permiten la automatización y la interacción con los huéspedes:  
- El [Internal identifier](#internal-identifier), usado solo en tu dashboard para la gestión de propiedades.  
- Los **Guest-facing identifiers** — el [Property guest name](#property-guest-name) y el [Guest access PIN](#guest-access-pin) — que conectan a cada huésped de forma segura con el asistente de la propiedad correcta.

Puedes configurar o actualizar estos identificadores en **My Properties** > _selecciona una propiedad_ > <img src="../media/modify-property-icon.png" alt="pencil icon" style="height: 1em; vertical-align: middle;">.

## Internal identifier

El **Property Internal name** se usa solo por tu equipo en el dashboard. Ayuda a ti y a tu equipo a reconocer y referirse a la propiedad de forma coherente.

- No visible para los huéspedes  
- Puede seguir cualquier convención de nombres (ej. `WILLOWST77-1A` para Willow Street 77, Apartamento 1A)  
- Debe ser único en la plataforma  
- Útil para evitar confusiones al gestionar varias unidades similares  

> **TIP** Usa nombres internos claros y coherentes para identificar las propiedades de un vistazo.

## Guest-facing identifiers

> **IMPORTANT**  
> **¡Lee esta sección con atención!** Explica conceptos clave que afectan directamente a la experiencia de los huéspedes con Alfred.

### Property guest name

Cuando un huésped contacta el número de Alfred, Alfred pregunta en qué apartamento se aloja y espera el **Property guest name**.

El **Property guest name** se muestra a los huéspedes en el chat de Alfred y en otros touchpoints (Booking.com, Airbnb, comunicaciones del host, etc.).

- Visible para los huéspedes  
- Debe ser único en la plataforma  
- Lo usa Alfred para conectar al huésped con el chatbot correcto  
- Puedes modificarlo en cualquier momento en **My Properties**

> **WARNING**
> - Usa exactamente el mismo nombre que los huéspedes ven en Booking.com o Airbnb para mantener las comunicaciones coherentes.  
> - Comparte siempre el Property guest name junto con el **Guest access PIN**, de lo contrario el huésped no podrá acceder a Alfred.

## Guest access PIN

El **Guest access PIN** es un código numérico corto (ej. *4739*) usado para verificar que el huésped es tu cliente.  
Evita que usuarios no autorizados accedan a Alfred y asegura que solo los huéspedes reales puedan interactuar con el asistente de la propiedad.

- Debe ser único para cada apartamento  
- Se comparte manualmente con los huéspedes por el host  
- Actúa como comprobación de seguridad antes de dar acceso al chat  
- Puedes modificarlo en cualquier momento en **My Properties**

> **WARNING**
> - Comparte siempre el PIN junto con el **Property guest name**, de lo contrario el huésped no podrá acceder a Alfred.  
> - Si cambias el **Property guest name** o el **Guest access PIN**, actualiza tus comunicaciones (emails, mensajes OTA, materiales impresos) para evitar confusión.

## Cómo funciona la autenticación de huéspedes

Cuando un huésped contacta el número de Alfred, debe autenticarse con ambos identificadores:

1. **Property guest name** — Alfred pregunta en qué apartamento se aloja. El huésped debe indicar exactamente el Property guest name.
2. **Guest access PIN** — Alfred pide luego el PIN para verificar su identidad.

> **IMPORTANT** El Property guest name es **sensible a mayúsculas**. Los huéspedes deben escribirlo exactamente como lo has configurado, incluidas mayúsculas y minúsculas. Por ejemplo, si el nombre es "Apartment 2B", escribir "apartment 2b" o "APARTMENT 2B" no funcionará.

Si un huésped introduce el PIN incorrecto, puede intentarlo de nuevo. Asegúrate de compartir con claridad el Property guest name y el PIN para evitar problemas de autenticación.
