# Auditoría de UX/UI - App Notas

## 1. Tabla de Heurísticas de Nielsen (Problemas y Soluciones)
| Heurística | Problema Encontrado | Solución Aplicada |
| :--- | :--- | :--- |
| **Visibilidad del estado** | Al agregar una nota no había feedback; la nota aparecía sin aviso. | Se implementó un mensaje dinámico de confirmación ("Nota creada"). |
| **Coincidencia con el mundo real** | El botón de eliminación decía "Purge". | Se cambió el texto a "Eliminar nota". |
| **Control y libertad** | Al hacer clic en borrar, la nota se eliminaba de inmediato. | Se agregó un modal de confirmación con la opción de cancelar. |
| **Prevención de errores** | Se podía guardar una nota vacía presionando Enter. | Se deshabilitó el botón si el campo está vacío y se validó en JS. |
| **Reconocer, no recordar** | Las notas no mostraban etiquetas ni categorías claras. | Se añadieron etiquetas fijas por color/categoría. |

## 2. Aplicación de Leyes de Usabilidad
* **Ley de Fitts:** Se agrandó el área táctil de los botones principales (mínimo 44px) para facilitar la interacción.
* **Ley de Hick:** Se redujo el número de opciones visibles directamente en la pantalla de inicio, agrupando acciones complejas en menús desplegables.
* **Ley de Miller:** Se organizó la vista en bloques compactos (3 a 4 secciones máximo) para no sobrecargar la memoria visual.

## 3. Accesibilidad y Estilos
* Variables CSS en `:root` para colores y contraste (mínimo 4.5:1).
* Etiquetas `<label>` vinculadas con `for`/`id`.
* Atributo `alt` en imágenes y foco visible marcado con `:focus-visible`.
* Puntaje en Lighthouse Accesibilidad: >= 90.