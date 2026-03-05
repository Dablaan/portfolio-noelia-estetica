# Guía Maestra del Proyecto: Portfolio Estética (Astro + IA)

## 1. Conceptos Fundamentales
- **Framework (Astro):** La estructura prefabricada que nos ahorra picar código desde cero y garantiza que la web cargue rápido.
- **Tailwind CSS v4:** El motor de estilos que permite diseñar inyectando clases directamente en el HTML (ej. `aspect-square`, `rounded-lg`).
- **Control Bot (Reglas, Skills y Workflows):** La metodología para dirigir a la IA. En lugar de pedirle todo a la vez (lo que genera errores), dividimos su "cerebro" en reglas estrictas (`reglas_globales.md`), habilidades específicas (`skills_prompts.md` con `@AstroUI` y `@GitMaster`) y un mapa de ruta paso a paso (`workflow_plan.md`).
- **Git:** Nuestra máquina del tiempo local para hacer "fotografías" (`commits`) del código en cada fase superada.

## 2. Estrategias de Ahorro de Cuota (Tokens)
- **Archivos `.md` sobre PDF:** La IA lee texto plano (Markdown) mil veces más rápido y barato que los archivos binarios (PDFs). Siempre debemos transcribir los requisitos.
- **Prompting Agrupado:** Pedir múltiples tareas relacionadas en un solo prompt estructurado (indicándole qué archivos exactos leer) gasta menos tokens que una conversación fragmentada.
- **Acciones Manuales:** Las tareas de interfaz web (como conectar GitHub con Vercel) se hacen a mano. La IA no tiene "manos" para navegar, y pedirle que lo haga consume cuota intentando generar largos tutoriales innecesarios.

## 3. Optimización y Buenas Prácticas (El Estándar Profesional)
- **SEO de Imágenes:** Las fotos locales siempre se renombran a minúsculas, sin espacios, sin tildes y con guiones (ej. `unas-acrilicas-blancas.jpg`).
- **Astro Assets:** Usar el componente nativo `<Image />` para que el framework comprima las fotos a formato WebP automáticamente al publicar la web.
- **Filtros CSS (Honestidad Visual):** No alterar las fotos originales de los trabajos de estética. Se unifica la galería visualmente usando CSS (`brightness-105 contrast-105 object-cover`).
- **i18n (Internacionalización):** Preparar la estructura base (`Layout.astro`) para soportar varios idiomas (ES/EN) desde el inicio es más fácil que intentar meterlo con calzador al final.
- **Cero Mantenimiento (RRSS):** Sustituir integraciones complejas y costosas (como la API Graph de Meta) por widgets ligeros (iframes gratuitos) para el feed de Instagram.

## 4. Historial de Prompts (El Workflow Ejecutado)
* **Fase 1 (Setup):** `Lee el archivo workflow_plan.md y sitúate en la Fase 1. Inicia un nuevo proyecto de Astro... limpia el index, inicializa Git y haz un commit.`
* **Fase 2 (Arquitectura):** `Crea Layout.astro con soporte i18n, configura colores Tailwind basándote estrictamente en el PRD. Llama a @GitMaster.`
* **Fase 3 (Componentes):** `Actúa bajo @AstroUI y crea Hero, Services y WhatsAppButton. Llama a @GitMaster...`
* **Fase 4 (Multimedia):** `Importa imágenes locales usando <Image />, aplica filtros CSS (aspect-square, object-cover) y prepara contenedor para Instagram. Llama a @GitMaster.`