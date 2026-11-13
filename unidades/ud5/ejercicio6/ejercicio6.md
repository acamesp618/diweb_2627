# Ejercicio 6

Crea una plantilla HTML sencilla para darle una estructura a una página web. Llámala `plantilla.html` y utilízala para crear 3 páginas: `index.html`, `contactos.html` y `noticias.html`.  
Añade en la parte principal un `iframe` con un contenido a tu elección.

---

## ¿Qué diferencia existe entre un frame y un iframe?

* **Frame:** Dividía la pantalla completa en regiones independientes. Requería un documento contenedor con la etiqueta `<frameset>` que sustituía por completo al elemento `<body>`. No podía colocarse libremente dentro del flujo de texto o diseño de una página web.
* **iFrame:** Es un elemento de nivel de bloque que se comporta como cualquier otro componente HTML (similar a `<img>` o `<div>`). Se inserta directamente dentro del `<body>` de un documento HTML estándar, lo que permite dimensionarlo, alinearlo mediante CSS y combinarlo libremente con el contenido circundante.

---

## ¿Por qué los frames tradicionales dejaron de utilizarse?

Los *frames* cayeron en desuso y fueron descartados formalmente en la especificación **HTML5** por severos problemas técnicos y de usabilidad:

* **Accesibilidad:** Los lectores de pantalla y tecnologías asistivas tenían dificultades para interpretar la navegación interconectada entre marcos y anunciar correctamente los cambios de contenido.
* **SEO (Posicionamiento en buscadores):** Los motores de búsqueda indexaban las páginas individuales del frame sin su contexto (`<frameset>`), haciendo que los usuarios llegaran a marcos aislados sin cabecera ni navegación general.
* **Problemas con marcadores y URLs:** La barra de direcciones del navegador mostraba siempre la URL del conjunto de frames principal. Si el usuario navegaba internamente dentro de un marco, la URL no cambiaba, impidiendo guardar en favoritos o compartir una subpágina específica.
* **Experiencia de usuario e impresión:** El botón de "Atrás" del navegador a menudo producía comportamientos impredecibles al gestionar el historial de marcos individuales. Además, enviar a imprimir la ventana completa generaba problemas de renderizado de los scrolls independientes.

---

## ¿Qué ventajas ofrece una plantilla?

Frente a la inclusión estática de documentos completos mediante marcos, la arquitectura basada en plantillas (ya sea en servidor o mediante sintaxis `<template>` en cliente) aporta:

* **Modularidad y Reutilización:** Permite mantener componentes comunes (como cabeceras, menús de navegación y pie de página) en archivos únicos y reutilizables en toda la aplicación sin duplicación de código (principio **DRY** - *Don't Repeat Yourself*).
* **Mantenibilidad:** Si se requiere un cambio en la navegación o en la identidad visual, basta con editar la plantilla correspondiente para que el cambio se refleje automáticamente en todo el sitio web.
* **Separación de Responsabilidades:** Separa claramente la capa de presentación (HTML/CSS) de la lógica de negocio o de los datos dinámicos.
* **Carga eficiente e indexabilidad:** Genera un único árbol de DOM limpio por página, facilitando el trabajo de indexación a los motores de búsqueda y mejorando el rendimiento de carga sin gestionar contextos de navegación paralelos.

---

## ¿Qué problemas de seguridad pueden aparecer al utilizar iframes?

Al incrustar documentos externos en un `<iframe>`, se abren diferentes vectores de ataque si no se configuran correctamente las protecciones de aislamiento:

* **Clickjacking (UI Redress Attack):** Un sitio malicioso incrusta una página legítima mediante un iframe transparente o superpuesto sobre botones atractivos. El usuario cree hacer clic en un elemento inofensivo, pero en realidad está interactuando con la página incrustada (por ejemplo, ejecutando una transferencia bancaria o dando un "Me gusta").
  * **Mitigación:** Cabeceras HTTP `X-Frame-Options: DENY` / `SAMEORIGIN` o directivas *Content Security Policy* (CSP) como `frame-ancestors`.
* **Inyección de Scripts y Cross-Site Scripting (XSS):** Si el contenido dentro del iframe proviene de una fuente no confiable, puede ejecutar código JavaScript en el contexto del navegador.
  * **Mitigación:** Utilizar el atributo `sandbox` en el elemento iframe (ej. `<iframe sandbox="allow-scripts allow-same-origin">`) para restringir permisos como envío de formularios, ejecución de scripts o apertura de popups.
* **Acceso no autorizado a API del navegador:** Un iframe incrustado podría solicitar acceso a la cámara, micrófono, geolocalización o almacenamiento sin consentimiento.
  * **Mitigación:** Definir políticas explícitas de permisos mediante el atributo `allow` (*Permissions Policy*).

---

## ¿Qué alternativas modernas existen para reutilizar componentes de una interfaz?

La arquitectura web moderna dispone de estándares nativos y metodologías basadas en componentes que evitan recurrir a iframes salvo para integrar servicios de terceros (como pasarelas de pago, reproductor de vídeo o mapas):

* **Web Components (Nativos en navegador):** Conjunto de tecnologías estándar (*Custom Elements*, *Shadow DOM* y elementos `<template>`) que permiten crear etiquetas HTML personalizadas y totalmente encapsuladas sin librerías externas.
* **Frameworks y librerías SPA (React, Angular, Vue, Svelte):** Crean la interfaz mediante componentes reactivos modulares que se componen y renderizan dinámicamente en el cliente.
* **Renderizado en servidor y Partial Layouts (PHP, Next.js, Blade, Twig):** Uso de motores de plantillas o componentes de servidor (*Server Components*) que componen la página HTML completa antes de enviarla al navegador.
* **Fetch API / AJAX / Server-Driven UI (HTMX):** Carga dinámica de fragmentos HTML o datos JSON mediante peticiones asíncronas para actualizar secciones del DOM en tiempo real sin recargar la página ni aislar el contexto de navegación.