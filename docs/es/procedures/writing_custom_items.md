# Writing custom items

Ya hemos definido la información principal que tus huéspedes pueden necesitar. Puedes añadir custom items a tus [libraries](/es/concepts/libraries_c.md) para cubrir detalles adicionales. Sigue estos consejos para que Alfred tenga la información más precisa sobre tu propiedad y políticas.

## 💡 Piensa en placeholders

Escribe los items para que encajen bien en los mensajes a los huéspedes.

> **Example**
> - **Garbage collection times**: “de 18:30 a 22:30”
> - **Mensaje al huésped**: “Recuerda que la basura se puede sacar {garbage_collection_times}.”

## 🥵 No sobrecargues un solo item

Cada contenido de library debe centrarse en **una sola información clara**. Los items estándar contienen un solo contenido. Al crear custom items, separa tipos de información en entradas distintas.

> **Example** ❌ **Hot water information**: “Caldera encima del bidé. Botón debajo. Si no hay agua caliente, abre la llave bajo el fregadero de la cocina.”  
> ✅ Dividido en varios items:  
> - **Hot water system location**: “Encima del bidé en el baño”  
> - **Hot water ON/OFF button location**: “Debajo de la caldera en el baño”  
> - **Main water valve location**: “Bajo el fregadero de la cocina”

## ✍️ Instrucciones paso a paso cuando hagan falta

Para procedimientos como abrir una keybox o reiniciar la caldera, usa pasos cortos y numerados en orden lógico.

> **Example** ✅ **Keybox instructions**:  
> 1. Gira los diales para poner el código.  
> 2. Baja la palanca negra.  
> 3. Después de usar, mezcla el código para mantenerlo privado.

---

### También te puede interesar

- [Cómo escribir buenos contenidos de biblioteca](/es/procedures/writing_tips.md) — Principios y tono para contenido eficaz
- [Writing internal policies](/es/procedures/writing_policies.md) — Controlar cuándo Alfred pasa conversaciones o toma acciones
