# Tabla de Análisis de Color y Elementos UI

| Sitio web | 60% Dominante (Base/Fondo) | 30% Secundario (Estructura/Texto) | 10% Acento (Conversión/CTA) | Un texto | Un botón CTA | Un mensaje de error o éxito |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **notion.com** | Blanco (`#FFFFFF`) | Gris (`#37352F`) | Azul (`#2383E2`) | Gris (`#37352F`) | Azul (`#2383E2`) | Texto explicativo en formulario |

---

# Respuestas a las Preguntas de Accesibilidad (WCAG)

* **¿Cumple el texto normal el ratio de 4.5:1?**
  * **Sí.** El texto en `#37352F` sobre fondo blanco `#FFFFFF` da un ratio de contraste de **12.26:1**, superando holgadamente el mínimo de 4.5:1 exigido para texto normal.

* **¿El botón cumple el ratio de 3:1?**
  * **Sí.** El texto blanco `#FFFFFF` sobre el fondo azul `#2383E2` alcanza un ratio de contraste de **3.88:1**, por lo que cumple con el criterio de 3:1.

* **¿Si la web muestra un error, utiliza un icono o texto descriptivo además del color rojo?**
  * **Sí.** Al cometer un error en los campos de entrada, Notion añade un texto explicativo explícito (ej. *"Dirección de correo electrónico no válida"*) junto al formulario.
