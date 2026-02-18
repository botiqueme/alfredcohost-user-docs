# FAQ Biblioteca

Preguntas frecuentes sobre redacción y gestión del contenido de la library para tus propiedades.

## Preguntas generales

<details>
<summary><strong>¿Tengo que rellenar todos los items estándar?</strong></summary>

No. Rellena solo lo que sea relevante para tu propiedad. Deja en blanco los items que no apliquen. Alfred solo usará la información que proporciones.

Más información: [Sobre las libraries](/es/concepts/libraries_c.md)

</details>

<details>
<summary><strong>¿Quick launch o full control?</strong></summary>

Puedes elegir según tu calendario. El **Quick launch (15 minutos)** te pone en línea rápido con lo esencial: check-in, políticas, datos básicos del alojamiento. El **Full control** te permite construir una library completa a tu ritmo. Ambos enfoques funcionan.

Más información: [Configurar tu biblioteca](/es/procedures/setup_library_p.md)

</details>

<details>
<summary><strong>¿Puedo editar las voces después de crearlas?</strong></summary>

Sí. Puedes editar cualquier voz en cualquier momento. Los cambios tienen efecto de inmediato.

Más información: [Añadir contenido a las bibliotecas](/es/procedures/libraries_p.md)

</details>

<details>
<summary><strong>¿Cómo sé si mi redacción es suficiente?</strong></summary>

Alfred entiende muy bien lo que escribes. Para mejores resultados sigue nuestros [consejos de escritura](/es/procedures/writing_tips.md). Lo importante es ser claro y concreto — piensa en lo que el huésped necesita para resolver su problema o encontrar lo que busca.

</details>

<details>
<summary><strong>¿Puedo copiar voces entre propiedades?</strong></summary>

Actualmente cada propiedad tiene su propia library. Debes añadir las voces a cada propiedad por separado. Así la información se mantiene precisa y específica de cada unidad.

Más información: [Sobre las libraries](/es/concepts/libraries_c.md)

</details>

## Redacción

<details>
<summary><strong>¿Qué longitud deben tener las voces?</strong></summary>

Mantén las voces cortas y centradas. Cada voz debe cubrir **una sola información clara**. Para items simples (contraseña Wi-Fi) bastan unas palabras. Para procedimientos (abrir keybox, reiniciar caldera) usa pasos numerados cortos y en orden lógico.

Más información: [Writing custom items](/es/procedures/writing_custom_items.md)

</details>

<details>
<summary><strong>¿Puedo usar abreviaturas o términos técnicos?</strong></summary>

Evita abreviaturas y jerga interna. Escribe como si le explicaras algo a un huésped en persona. Usa un lenguaje claro y cotidiano.

Más información: [Consejos de escritura](/es/procedures/writing_tips.md)

</details>

<details>
<summary><strong>Mi propiedad tiene características no cubiertas por los items estándar</strong></summary>

Usa custom items para cualquier información no cubierta por los campos estándar. Ver [writing custom items](/es/procedures/writing_custom_items.md).

</details>

<details>
<summary><strong>¿Debo incluir fotos o vídeos?</strong></summary>

Solo si facilitan la explicación. Imágenes y vídeos son útiles **solo en ese caso** — evita saturar. Usa los campos **photo**, **video**, **instructions**. No pegues enlaces en la descripción.

Más información: [Escribir buenos contenidos](/es/procedures/writing_tips.md)

</details>

<details>
<summary><strong>¿Qué tan específico debo ser con las ubicaciones?</strong></summary>

Sé lo más preciso posible. Escribe **ubicaciones claras y detalladas**. En lugar de "en la cocina", escribe "dentro del mueble bajo el fregadero de la cocina".

Más información: [Escribir buenos contenidos](/es/procedures/writing_tips.md)

</details>

<details>
<summary><strong>No estoy seguro de cómo redactar algo</strong></summary>

Parte del punto de vista del huésped: ¿qué está intentando hacer? ¿Cuándo necesitará esta información? ¿La voz debe instruir, informar, tranquilizar o guiar? Luego escribe una respuesta clara y directa. Si dudas, consulta nuestra [guía de escritura](/es/procedures/writing_tips.md).

</details>

## Custom items

<details>
<summary><strong>¿Cuándo crear un custom item?</strong></summary>

Crea custom items cuando necesites añadir información no cubierta por los campos estándar (ej. instrucciones de aparcamiento, horarios de basura, características únicas de la propiedad).

Más información: [Writing custom items](/es/procedures/writing_custom_items.md)

</details>

<details>
<summary><strong>¿Cómo funcionan los placeholders en custom items?</strong></summary>

Piensa en placeholders: escribe las voces para que encajen bien en los mensajes. Ej. un item "Garbage collection times" con valor "de 18:30 a 22:30" puede insertarse en un mensaje tipo: "Recuerda que la basura se puede sacar {garbage_collection_times}."

Más información: [Writing custom items](/es/procedures/writing_custom_items.md)

</details>

<details>
<summary><strong>¿Puedo poner varias informaciones en un solo custom item?</strong></summary>

No. Cada voz debe centrarse en **una sola información clara**. Si tienes varios detalles relacionados, crea una voz por cada uno. Alfred encontrará y usará la información correcta.

Más información: [Writing custom items](/es/procedures/writing_custom_items.md)

</details>

<details>
<summary><strong>¿Cuál es la diferencia entre items estándar y custom?</strong></summary>

Los items estándar son campos predefinidos (contraseña Wi-Fi, hora de check-in, etc.). Los custom items permiten añadir cualquier otra información específica de tu propiedad. Ambos funcionan igual para Alfred.

Más información: [Sobre las libraries](/es/concepts/libraries_c.md), [Writing custom items](/es/procedures/writing_custom_items.md)

</details>

## Políticas

<details>
<summary><strong>¿Qué son las políticas y en qué se diferencian de las voces normales?</strong></summary>

Las políticas son voces especiales que controlan el comportamiento de Alfred en situaciones concretas. Nunca se muestran directamente a los huéspedes. Indican a Alfred qué hacer o decir cuando se cumplen ciertas condiciones.

Más información: [Writing internal policies](/es/procedures/writing_policies.md)

</details>

<details>
<summary><strong>¿Necesito crear políticas personalizadas?</strong></summary>

Ya hemos definido las políticas base. Solo necesitas crear políticas personalizadas para situaciones que requieran un tratamiento especial. Estructura: **Trigger**, **Action**, **Message** (si hace falta). Ver [writing policies](/es/procedures/writing_policies.md).

</details>

## Resolución de problemas

<details>
<summary><strong>Alfred no usa correctamente mis voces</strong></summary>

Comprueba que las voces sean: claras y concretas; centradas en una sola información; redactadas desde el punto de vista del huésped; sin palabras vagas ("disponible", "presente"). Comprueba también que los custom items tengan etiquetas claras.

Más información: [Escribir buenos contenidos](/es/procedures/writing_tips.md), [Writing custom items](/es/procedures/writing_custom_items.md)

</details>

<details>
<summary><strong>¿Puedo probar cómo Alfred usará mi library?</strong></summary>

Sí. Usa la función test assistant para ver cómo Alfred responde a las preguntas. Así compruebas el comportamiento antes de publicar.

Más información: [Test assistant](/es/procedures/test_assistant.md)

</details>

<details>
<summary><strong>¿Qué pasa si dejo un item en blanco?</strong></summary>

Nada. Alfred simplemente no usará esa información. Los huéspedes no verán campos vacíos ni mensajes de error.

Más información: [Sobre las libraries](/es/concepts/libraries_c.md)

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
