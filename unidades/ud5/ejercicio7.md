# Ejercicio 7

## ¿Qué son los CMS?

Un **CMS** (*Content Management System* o Sistema de Gestión de Contenidos) es una aplicación software que permite a los usuarios crear, administrar, editar y publicar contenidos digitales en un sitio web sin necesidad de escribir código fuente ni programar la interfaz desde cero.

Separa la capa de presentación (plantillas o diseño visual) de la capa de datos y lógica del sitio, proporcionando un panel de administración visual (*Back-office*) intuitivo para gestionar entradas, páginas, multimedia y usuarios.

## Casos de uso: ¿Cuándo utilizar un CMS y cuándo no?

* **Cuándo SÍ usar un CMS:** En un blog corporativo, web de noticias o portal de contenidos dinámicos con publicaciones continuas, ya que permite a perfiles no técnicos redactar, programar y publicar contenidos rápidamente. Incluye gestión de roles de usuario, flujo editorial, taxonomías (categorías/etiquetas) y optimización SEO nativa o mediante plugins.

* **Cuándo NO usar un CMS:** En una aplicación web interactiva de alta complejidad (ej. plataforma SaaS con lógica personalizada o algoritmos a medida). Los CMS tradicionales añaden sobrecarga (*overhead*) de base de datos, capas innecesarias de complejidad, limitaciones de arquitectura y posibles brechas de seguridad al intentar forzarlos a actuar como software a medida.
  * **Alternativa:** Un desarrollo a medida utilizando Frameworks Web (ej. Angular, React, Laravel o Vanilla PHP/Node.js) junto con una API REST o arquitectura de microservicios.

## Comparativa de CMS en el mercado

### WordPress
* **Tipo:** Open Source (*Self-hosted*).
* **Enfoque principal:** Gestión de contenidos general, blogs, páginas corporativas y comercio electrónico (vía WooCommerce).
* **Puntos fuertes:** Gran comunidad, ecosistema masivo de temas/plugins y alta flexibilidad.

### Shopify
* **Tipo:** SaaS (*Software as a Service* - Privativo).
* **Enfoque principal:** E-commerce exclusivo.
* **Puntos fuertes:** Plataforma llave en mano con alojamiento, pasarelas de pago y seguridad gestionadas al 100% por el proveedor.

### Strapi / Sanity
* **Tipo:** Headless CMS.
* **Enfoque principal:** Gestión de contenidos desacoplada expuesta mediante API (REST/GraphQL).
* **Puntos fuertes:** Ideal para consumir contenidos desde múltiples clientes (*frontends* en React/Angular, aplicaciones móviles, IoT).

### Joomla / Drupal
* **Tipo:** Open Source (*Self-hosted*).
* **Enfoque principal:** Sitios complejos con estructuras de permisos avanzados e integración institucional.
* **Puntos fuertes:** Control granular de seguridad y arquitecturas de datos complejas fuera de la caja.

## Elección para diseñar una tienda online rápida y funcional

Si el objetivo principal es desplegar una tienda online de manera rápida, funcional y sin complicaciones de infraestructura, la mejor opción depende del modelo de despliegue preferido:

1. **Shopify (Opción SaaS más rápida):** Es la alternativa ideal para lanzar una tienda en cuestión de horas sin preocuparse por servidores, certificados SSL, mantenimiento de base de datos ni configuración de pasarelas de pago. La plataforma ofrece plantillas listas para producción y optimizadas para conversión.
2. **WooCommerce sobre WordPress (Opción Open Source):** Si se busca independencia total del hosting, control de datos y menores costes fijos mensuales a largo plazo, WordPress junto a la extensión WooCommerce permite montar un comercio electrónico completamente operativo mediante un instalador en pocos pasos.