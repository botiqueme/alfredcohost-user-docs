# 📜 Writing internal policies

Las políticas son un tipo especial de contenido de library que sirve para controlar el comportamiento de Alfred en situaciones concretas. **Nunca se muestran directamente a los huéspedes**. Definen qué debe hacer o decir Alfred cuando se cumplen ciertas condiciones — por ejemplo cuando un huésped reporta un problema, pide servicios extra o intenta hacer check-in fuera de horario.

Ya hemos definido las políticas base para Alfred. Si necesitas crear otras personalizadas, estos consejos te ayudan.

## 🧠 Qué debe tener una buena política

Una política bien redactada debe:
- Ser **concreta** sobre el escenario al que se aplica
- Definir claramente **qué debe hacer Alfred** (¿pasar a un humano? ¿enviar un mensaje? ¿no hacer nada?)
- Incluir **qué debe decir Alfred** si hace falta un mensaje al huésped
- Estar redactada en **lenguaje natural** (sin placeholders, sin jerga técnica)

## ✅ Estructura a seguir

Antes de escribir una política, delimita bien el alcance: ¿Qué situación cubre? ¿Cuándo empieza? ¿Cuándo termina?

Luego usa esta estructura:

1. **Trigger**  
   Describe la condición que activa la política.  
   _Ejemplo: “Si el huésped indica que ha perdido las llaves…”_

2. **Action**  
   Describe qué debe hacer Alfred.  
   _Ejemplo: “Pasar el chat a un agente humano.”_

3. **Message (si hace falta)**  
   Indica el mensaje exacto que Alfred debe enviar.  
   _Ejemplo: “No te preocupes, te contestamos en breve.”_

---

### También te puede interesar

- [Cómo escribir buenos contenidos de biblioteca](/es/procedures/writing_tips.md) — Principios y tono
- [Writing custom items](/es/procedures/writing_custom_items.md) — Añadir información específica de la propiedad
