# 🔍 Informe de Auditoría UI/UX & Copywriting

## 1. Análisis del Componente `Hero.astro`

Actualmente, el Hero es funcional y cumple con la base, pero visualmente puede resultar un poco plano y su texto es demasiado genérico ("como en casa"). Un centro de belleza no solo vende un servicio, vende **autoestima, bienestar y desconexión**.

### 🎨 Mejoras Visuales y de Interfaz (Tailwind)
*   **Fondo más profundo y premium:** En lugar de un color sólido plano (`bg-nude-50`), podemos usar un leve degradado lineal o radial que aporte luz desde el centro superior de la pantalla. Ejemplo: `bg-[radial-gradient(ellipse_at_top,_var(--tw-gradient-stops))] from-white via-nude-50 to-nude-100`.
*   **Animaciones sutiles (Fade-in-up):** El texto principal y el botón deberían aparecer al cargar la página en lugar de cargarse de golpe. Se puede configurar una utilidad simple en Tailwind (ej. `animate-fade-in-up`) para darle un "efecto wow" inicial sin perder elegancia.
*   **Tipografía más sofisticada:** Añadir `tracking-tight` (letter-spacing negativo) a los títulos grandes de Tailwind suele dar un aspecto editorial mucho más moderno y pulido.
*   **El Botón de Acción (Call to Action - CTA):** El botón debe invitar a hacer clic. Para hacerlo más "premium":
    *   Añadir una transición de elevación al pasar el ratón: `transition-all duration-300 hover:-translate-y-1`.
    *   Mejorar la sombra para emitir un suave "glow" usando el color corporativo: `shadow-lg hover:shadow-pink-200/60`.

### ✍️ Propuestas de Copywriting (Beneficios > Características)
*   **Título (H1):**
    *   *Actual:* "Tu espacio digital como en casa"
    *   *Propuesta 1:* "Despierta tu mejor versión en un ambiente diseñado para ti"
    *   *Propuesta 2:* "El momento de desconexión y belleza que mereces"
    *   *Propuesta 3:* "Eleva tu belleza natural. Nosotras nos encargamos del resto."
*   **Subtítulo (P):**
    *   *Actual:* "Ambiente tranquilo, trato súper personalizado. Nos encanta cuidar y mimar a cada cliente."
    *   *Propuesta:* "Olvídate del estrés diario en nuestro refugio de estética. Déjate mimar por especialistas y luce unas manos, mirada y piel impecables durante semanas."
*   **Llamada a la acción (CTA):**
    *   *Actual:* "Reserva tu cita"
    *   *Propuesta 1:* "Reserva tu momento"
    *   *Propuesta 2:* "Empezar a mimarme"

---

## 2. Análisis del Componente `Services.astro`

La estructura en grid dividida en tarjeta destacada y menú secundario es un buen recurso para organizar la jerarquía, pero los colores sólidos de fondo (`bg-pastel-pink`, `bg-pastel-green`) pueden verse muy "infantiles" si no se tratan adecuadamente. En estética buscamos un minimalismo *nude* y elegante.

### 🎨 Mejoras Visuales y de Interfaz (Tailwind)
*   **Fondos de tarjetas tipo "Soft Glass" o Gradiente Suave:** Para evitar que las tarjetas se vean como bloques duros de color, sugerimos usar colores más cercanos al blanco con un destello del color pastel y bordes semitransparentes. Por ejemplo: `bg-white/80 backdrop-blur-sm border-white/50` apoyado sobre un fondo general muy sutil, o gradientes muy difuminados `bg-gradient-to-br from-pink-50/40 to-white`.
*   **Paddings más holgados (Efecto "Aire"):** En móvil el padding de 8 (`p-8`) está bien, pero en desktop las tarjetas agradecerían más respiro, subiéndolo a `lg:p-10`. El espacio en blanco es clave en el lujo.
*   **Sombra de Tarjetas (Glow elegante):** Sustituir el `shadow-sm` base por una sombra suave custom que envuelva la tarjeta sin que parezca pesada: `shadow-[0_8px_30px_rgb(0,0,0,0.04)]`.
*   **Efecto Hover de interacción:** Al igual que en el Hero, queremos que la web se sienta "viva". Que al pasar por encima (`group-hover:`) la tarjeta ascienda ligeramente (`hover:-translate-y-2`) y que la imagen haga un ligerísimo zoom interior suave (`group-hover:scale-105 transition-transform duration-500` con `overflow-hidden` en su contenedor).
*   **Badge "Destacado":** Hacerlo menos ruidoso, quizás un borde muy fino con texto en un tono rosa empolvado más profundo, en lugar del sólido actual.

### ✍️ Propuestas de Copywriting (Beneficios > Características)
*   **Título de Sección:**
    *   *Actual:* "Nuestros Servicios Estrella"
    *   *Propuesta:* "Experiencias de Belleza que Transforman" o "Tus Rituales de Cuidado"

*   **Servicio Destacado (Microblading):**
    *   *Actual:* "Microblading & Micropigmentación: Diseño experto de mirada y labios. Resultados naturales que realzan tu belleza."
    *   *Propuesta:* "**Microblading & Micropigmentación:** Despierta cada mañana con una mirada perfecta. Diseñamos tus cejas y labios con precisión milimétrica para un resultado tan natural que será tu secreto mejor guardado. Olvídate del maquillaje diario."

*   **Servicios Secundarios (Uñas y Pedicura):**
    *   *Título Actual:* "Estética Completa" -> *Propuesta:* "Mimos de Pies a Cabeza" o "Manos y Pies Impecables"
    *   *Actual Uñas Acrílicas:* "extensiones, esculpidas y diseños únicos" -> *Propuesta Uñas Acrílicas:* "Uñas largas, ultrarresistentes y con el diseño que siempre has soñado."
    *   *Actual Semipermanente:* "color duradero y brillo impecable" -> *Propuesta Semipermanente:* "Brillo cristalino y color intacto durante semanas. Adiós a los retoques diarios."
    *   *Actual Pedicura:* "relajación y cuidado para tus pies" -> *Propuesta Pedicura:* "Un ritual de relajación profunda que renueva tus pies, dejándolos suaves y preciosos para cualquier ocasión."
