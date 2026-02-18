<div data-toc-depth="3"></div>

# Libraries

En la plataforma Alfred Co.Host, una **library** es el conjunto estructurado de información que Alfred usa para responder a las preguntas de los huéspedes de una propiedad concreta.

Cada propiedad tiene su propia library. Esa library contiene toda la información relevante sobre la unidad — desde cómo poner la calefacción hasta dónde comer cerca. Cuando construyes una library, recopilas y organizas:

- **Información del alojamiento**: descripciones generales (ubicación, características, zona, estilo).
- **Dispositivos y electrodomésticos**: instrucciones y resolución de problemas (Wi-Fi, TV, electrodomésticos, etc.).
- **Sistemas de la casa y resolución de problemas**: guía y troubleshooting (electricidad, agua, calefacción, A/C).
- **Consejos locales**: sugerencias de comida, transporte, visitas y otra información local.
- **Políticas y procedimientos**: normas de la casa e instrucciones relacionadas con la estancia y la relación con el host.
- **Info solo para staff**: notas internas de mantenimiento o detalles de huéspedes. Solo visible para el staff — nunca se muestra a los huéspedes.

> **NOTE** Cuanto más rica y clara sea tu library, más útil será Alfred.

## Cómo funciona

La library de cada propiedad está formada por **unidades de información**. Algunas están predefinidas, otras son personalizables.

Cuando Alfred identifica la propiedad del huésped, usa la library asociada para responder — tanto si el huésped pide ayuda práctica, detalles descriptivos o quiere contactar con un humano.

Las unidades de información son de dos tipos: **Standard** (campos predefinidos) y **custom** (que tú defines).

La información puede ser **textual** o **media**:

- [Standard textual information](#standard-textual-information)
- [Custom textual information](#custom-textual-information)
- [Standard media information](#standard-media-information)
- [Custom media information](#custom-media-information)

Alfred usa esta información **tal cual** o la combina según la complejidad de la petición.

### Standard textual information

Campos predefinidos donde puedes introducir un valor de texto.  
Ejemplo:

| Information unit | Description | Custom value |
| --- | --- | --- |
| Property address | Dirección para localizar la propiedad | `123 Oxford Street, London` |

Rellena solo lo que necesites — deja el resto en blanco.

### Custom textual information

Campos personalizados donde defines tanto la etiqueta como el valor de texto.  
Ejemplo:

| Custom information unit | Custom description | Custom value |
| --- | --- | --- |
| `Parking instructions` | `Procedimiento para abrir la barrera del parking` | `Use the garage remote stored in the kitchen cupboard` |

### Standard media information

Campos predefinidos donde puedes añadir medios (fotos o vídeos).  
Ejemplo:

| Information unit | Description | Value |
| --- | --- | --- |
| How to launch the washing machine | Tutorial para poner la lavadora | `washing_machine_tutorial.mp4` |
| Fridge shelves detail | Detalle de baldas asignadas | `roomA_fridge_shelf.png` |

Formatos soportados:
- image: JPG, JPEG, PNG hasta 25 Mb
- video: MP4, 3GP hasta 25 Mb

### Custom media information

Campos personalizados donde defines la etiqueta, una descripción opcional y el archivo de medio.  
Ejemplo:

| Custom information unit | Custom description | Custom value |
| --- | --- | --- |
| `How to unlock the backyard door` | `Procedimiento para desbloquear la puerta del jardín` | `backyard_door_opening_demo.mp4` |
| `How to open/close the terrace curtain` | `Detalle del mecanismo de la cortina` | `curtain_lock.png` |

Formatos soportados:
- image: JPG, JPEG, PNG hasta 25 Mb
- video: MP4, 3GP hasta 25 Mb
