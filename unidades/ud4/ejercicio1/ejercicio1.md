# Análisis UI y Solución mediante Guía de Estilo

1. **Objetivo:** Encontrar al menos 4 errores visuales en 5 minutos y anotar en el Portfolio cómo una guía de estilo habría evitado el caos.

---

## Errores Visuales Identificados

### 2. Problemas graves de legibilidad y contraste (Inaccesibilidad Web)
- **Subtítulo del header:** El texto *"LOS MEJORES PRECIOS DEL MERCADO..."* en verde/azul sobre fondo rosa magenta es casi invisible por la falta de contraste.
- **Sección "OFERTA 2":** El texto *"Reloj Inteligente 2026."* en verde sobre fondo negro, sumado al enlace *"Ver más datos del producto"* en azul oscuro sobre negro, resulta prácticamente ilegible.

### 3. Tipografía inconsistente y no corporativa
- Se mezclan sin criterio tipografías dispares: fuentes *display*/fantasía muy pesadas en el encabezado (*"TIENDA DE OFERTAS DÉCADA 2020"*), fuentes informales tipo *Comic Sans* en los productos (*"Producto Estrella #1"*, descripción y pie de página), y tipografías *sans-serif* estándar en botones. Esto rompe la coherencia y profesionalidad.

### 4. Incoherencia cromática y paleta estridente
- Uso de colores primarios y neón en saturaciones máximas (magenta, amarillo chillón, cian, rojo puro, violeta, negro) sin una paleta armónica definida ni jerarquía visual.

### 5. Falta de alineación, espaciado e inconsistencia en componentes (UI Layout)
- Los contenedores de productos no siguen un sistema de retícula (*grid*): mientras que la *"Oferta #1"* es un rectángulo gigante con borde punteado rojo y cian, la *"Oferta 2"* es un bloque negro con bordes muy redondeados (*border-radius* desproporcionado).
- La cabecera está descompensada a la derecha y los márgenes/paddings interiores son irregulares.

---

## ¿Cómo una Guía de Estilo (Style Guide) habría evitado este caos?

La implementación previa de una Guía de Estilo habría garantizado la calidad visual del proyecto mediante las siguientes pautas:

- **Paleta de Colores Definida:** Estableciendo colores primarios, secundarios, neutros y de acento con ratios de contraste probados para garantizar accesibilidad (WCAG AA/AAA).
- **Sistema Tipográfico (Scale & Hierarchy):** Definiendo una o máximo dos familias tipográficas con reglas claras de escala (`h1`, `h2`, `body`, `caption`), pesos y alturas de línea (`line-height`).
- **Biblioteca de Componentes (UI Kit):** Normalizando los estados y estilos de botones, tarjetas de producto (*cards*), bordes y sombras para asegurar coherencia visual en todo el sitio.
- **Grid y Espaciado (Layout System):** Aplicando una retícula estándar (por ejemplo, base de 8px) para mantener márgenes, alineaciones y *paddings* proporcionados y limpios.
