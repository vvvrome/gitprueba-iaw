# Coevaluación de CMS y SSG

**Nombre del evaluador:** Jacinto Rodríguez  
**Persona evaluada:** Víctor Moreno  
**Mi repositorio:** [JacintoX/Trabajos_en_Markdown](https://github.com/JacintoX/Trabajos_en_Markdown)  
**Repositorio que evalúo:** [vvvrome/gitprueba-iaw](https://github.com/vvvrome/gitprueba-iaw)

---

## A. Puntuación de la investigación

| Código | Criterio | Máximo | Puntos asignados | Evidencia y justificación concreta |
|---|---|:---:|:---:|---|
| A1 | Concepto y funcionamiento de SSG. | 1 | 1 | `ssg.md`, apartados 1 a 3. Define el SSG, enumera los archivos de partida (Markdown, YAML, JSON, plantillas y recursos), explica el proceso en 5 pasos con diagrama y aclara que el HTML se genera antes de la visita. Completo. |
| A2 | SSG frente a HTML manual. | 0,5 | 0,3 | No hay un apartado propio. La comparación solo aparece de forma indirecta en el apartado 4 («las plantillas evitan repetir código», «la configuración inicial puede ser más compleja que crear una página HTML sencilla»). Falta un ejemplo concreto de qué se gana frente a escribir cada página a mano. |
| A3 | Comparación de Jekyll, Hugo y Astro. | 1 | 0,9 | `ssg.md`, apartado 5. Tabla con 7 aspectos (lenguaje, contenido, plantillas, instalación, velocidad, curva de aprendizaje y usos) y un párrafo de cada generador. Faltan ventajas e inconvenientes concretos de cada uno; la compatibilidad con GitHub Pages solo se menciona para Jekyll. |
| A4 | Concepto y funcionamiento de CMS. | 1 | 1 | `cms.md`, apartados 1 y 2. Definición clara con ejemplo práctico, proceso en 5 pasos y diagrama del flujo administrador → base de datos → plantillas → visitante. Completo. |
| A5 | Clasificación de CMS y ejemplos. | 0,5 | 0,35 | `cms.md`, apartado 3. Clasifica por propósito y por arquitectura, pero varios tipos no tienen ejemplo (blogs, corporativos, foros, desacoplado y headless). Además, «Alojado» describe el modelo de servicio, no la arquitectura, por lo que mezcla criterios. |
| A6 | Top 5 y estadísticas de mercado. | 0,5 | 0,1 | `cms.md`, apartado 4. La tabla recoge cinco CMS que coinciden con el ranking habitual, pero no se presenta como top 5 ni incluye cuotas, fuente, fecha de los datos ni medida utilizada. |
| A7 | Comparativa CMS dinámico–SSG. | 1 | 0,9 | `cms.md`, apartado 6. Tabla con 7 aspectos bien explicados y un apartado «¿Cuál elegir?» muy útil. Faltan aspectos como los conocimientos técnicos necesarios o la forma de publicar (hosting con PHP frente a hosting estático). |
| A8 | Claridad y apoyo visual. | 0,5 | 0,35 | Organización muy clara con apartados numerados. El apoyo visual se limita a diagramas en texto dentro de bloques de código y a un logotipo externo; no hay imágenes ni gráficos propios que expliquen el funcionamiento o las estadísticas. |
| **Subtotal A** | | **6** | **4,9** | |

## B. Puntuación de la actividad Markdown

| Código | Criterio | Máximo | Puntos asignados | Evidencia y justificación concreta |
|---|---|:---:|:---:|---|
| B1 | Organización del proyecto. | 0,75 | 0,6 | `cms.md` y `ssg.md` con nombres correctos y enlazados entre sí. No hay carpeta de recursos (`img/`) porque el proyecto no usa imágenes locales. **Pendiente de comprobar la estructura completa del repositorio.** |
| B2 | Adaptación de la investigación. | 0,75 | 0,6 | Ambos documentos tienen apartados numerados y bien adaptados. Sin embargo, `ssg.md` termina con un «Ejemplo adicional de Markdown» que no está relacionado con el tema, y ninguno de los dos documentos incluye índice. |
| B3 | Sintaxis Markdown. | 0,5 | 0,5 | Uso correcto de títulos, negrita, cursiva, tachado, listas ordenadas y no ordenadas, listas de tareas, tablas, citas, bloques de código con lenguaje (`text`, `html`), enlaces e imágenes. |
| B4 | Imágenes y rutas. | 0,5 | 0,2 | La única imagen es un logotipo de Wikimedia enlazado por URL externa (`ssg.md`). No hay imágenes locales con rutas relativas, por lo que no se puede comprobar su funcionamiento en GitHub ni en el ZIP extraído. |
| B5 | Dos vídeos de hasta 5 minutos. | 0,5 | 0,2 | `cms.md`, apartado 7: el enlace lleva a una **búsqueda de YouTube**, no a un vídeo concreto. `ssg.md`, apartado 7: enlaza un vídeo concreto, pero no indica su duración y el propio documento marca como pendiente comprobarla. |
| B6 | Enlace de cms.md a ssg.md. | 0,5 | 0,5 | `cms.md`, apartado 9: enlace relativo `[ssg.md](ssg.md)`, que funciona porque ambos archivos están en la misma carpeta. |
| B7 | Legibilidad de ambos documentos. | 0,5 | 0,4 | La vista previa es clara y bien espaciada. Restan legibilidad las notas internas que quedan en el texto final («Antes de entregar, comprueba que el vídeo...», «Comprueba la duración del vídeo antes de entregarlo...»). |
| **Subtotal B** | | **4** | **3** | |

---

## C. Nota propuesta y valoración inicial

- **Puntuación real A + B:** 7,9 / 10.

**Justificación de la nota:**  
La investigación es sólida en los conceptos clave: el funcionamiento de CMS y SSG y la comparativa entre ellos están muy bien explicados. La nota baja sobre todo por la ausencia de estadísticas de mercado con fuente (A6), por la falta de una comparación explícita entre SSG y HTML manual (A2) y por los vídeos: el de CMS es un enlace de búsqueda y el de SSG no indica su duración (B5). Los criterios B1 y B4 quedan pendientes de comprobar la estructura completa del repositorio, por lo que la nota no es definitiva en esos dos puntos.

**Dos puntos fuertes:**

- **Comparativa CMS dinámico frente a SSG (`cms.md`, apartado 6).** La tabla se complementa con el apartado «¿Cuál elegir?», que traduce las diferencias técnicas en criterios prácticos de decisión según quién mantenga la web y con qué frecuencia se actualice.
- **Explicación del funcionamiento de un SSG (`ssg.md`, apartado 3).** Los pasos numerados, el diagrama del proceso de *build* y la aclaración de en qué momento se genera el HTML dejan clara la diferencia fundamental con un CMS dinámico.

**Mejoras prioritarias:**

| Propuesta | Archivo y apartado | Observación y mejora propuesta |
|---|---|---|
| P1 | `cms.md`: apartado 4, «Ejemplos de CMS conocidos». | La tabla incluye cinco CMS, pero sin datos de mercado. Propongo convertirla en un **top 5** con la cuota de cada CMS, indicar la fuente (por ejemplo, W3Techs), la fecha de consulta y la medida usada (porcentaje sobre el total de webs o sobre las webs con CMS conocido). Además, un gráfico de barras como imagen local mejoraría también el apoyo visual. |
| P2 | `ssg.md`: nuevo apartado entre el 3 y el 4, «SSG frente a HTML manual». | Falta la comparación explícita con crear la web a mano en HTML. Propongo añadir un apartado breve con un ejemplo, como cambiar el menú o el pie de página en 50 páginas: con HTML manual hay que editar cada archivo y con un SSG basta con modificar la plantilla y volver a generar el sitio. |
| P3 | `cms.md`: apartado 7, «Vídeo explicativo» (y `ssg.md`, apartado 7). | El enlace de `cms.md` lleva a una búsqueda de YouTube en lugar de a un vídeo. Propongo enlazar un vídeo concreto e indicar su duración en ambos documentos, y eliminar las notas internas («Comprueba la duración...») y la tarea pendiente de la lista final de `ssg.md`. |

---

## D. Respuesta y correcciones del propietario del proyecto

**Cumplimenta:** [Nombre del propietario del repositorio].

| Propuesta | Respuesta y decisión razonada | Corrección aplicada y archivo | Commit |
|---|---|---|---|
| P1 | [Aceptada / Aclaración / Alternativa acordada, con explicación]. | [Qué he cambiado en cms.md y dónde]. | [Enlace]. |
| P2 | [Aceptada / Aclaración / Alternativa acordada, con explicación]. | [Qué he cambiado en ssg.md y dónde]. | [Enlace]. |
| P3 | [Aceptada / Aclaración / Alternativa acordada, con explicación]. | [Qué he cambiado y dónde]. | [Enlace]. |

**Qué he aprendido al corregir mi trabajo:** [Explicación breve].
