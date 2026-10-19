# Generadores de sitios estáticos (SSG)

## 1. ¿Qué es un SSG?

Un **SSG** (*Static Site Generator* o generador de sitios estáticos) es una herramienta que crea páginas web estáticas automáticamente a partir de archivos de contenido y plantillas.

Se utiliza para crear blogs, documentación, portafolios y otras webs sin tener que escribir manualmente cada página HTML.

## 2. ¿Qué archivos utiliza?

Como punto de partida puede utilizar archivos como:

- Markdown (`.md`)
- YAML (`.yml` o `.yaml`)
- JSON (`.json`)
- Plantillas y componentes
- Imágenes, hojas de estilo CSS y archivos JavaScript

Markdown resulta útil porque permite escribir contenido con una sintaxis sencilla y legible.

## 3. ¿Cómo funciona?

El generador combina el contenido con las plantillas, procesa la información y produce los archivos finales de la web.

1. Se escribe o modifica el contenido.
2. El SSG lee los archivos y la configuración.
3. Combina el contenido con las plantillas o componentes.
4. Genera HTML, CSS, JavaScript, imágenes u otros recursos necesarios.
5. Se publica el resultado en un servidor web o una plataforma de alojamiento.

```text
Markdown + datos + plantillas
              ↓
       SSG / proceso build
              ↓
     HTML + CSS + JavaScript
              ↓
       Publicación de la web
              ↓
          Navegador
```

El HTML se genera **antes de que el visitante solicite la página**, durante el proceso de desarrollo, compilación o publicación. Por eso el servidor puede entregar archivos ya preparados.

## 4. Ventajas e inconvenientes

### Ventajas

- **Rendimiento:** se sirven archivos previamente generados.
- **Mantenimiento:** las plantillas evitan repetir código en muchas páginas.
- **Seguridad:** una web puramente estática puede prescindir de una base de datos y de un CMS ejecutándose en el servidor público.
- **Versionado:** el contenido puede mantenerse en archivos y controlarse con Git.
- **Alojamiento sencillo:** puede publicarse en un servidor web estático o una CDN.

### Inconvenientes

- Para publicar cambios normalmente hay que volver a generar el sitio.
- Es necesario aprender el funcionamiento del generador y sus plantillas o componentes.
- La configuración inicial puede ser más compleja que crear una página HTML sencilla.
- Las funciones que requieren datos personalizados en tiempo real pueden necesitar APIs o servicios adicionales.

## 5. Comparación de Jekyll, Hugo y Astro

| Característica | Jekyll | Hugo | Astro |
|---|---|---|---|
| Lenguaje principal | Ruby | Go | JavaScript / TypeScript |
| Contenido habitual | Markdown + Front Matter | Markdown + Front Matter | Markdown, MDX y componentes |
| Herramientas de plantillas | Liquid | Plantillas de Hugo | Componentes de Astro y compatibilidad con otros frameworks |
| Instalación o entorno | Ruby y RubyGems | Binario de Hugo | Node.js y un gestor de paquetes |
| Velocidad de generación | Media | Muy alta | Alta |
| Curva de aprendizaje (orientativa) | Baja-media | Media | Media |
| Usos típicos | Blogs, documentación y páginas personales | Sitios grandes y documentación | Webs modernas y portafolios |

*La velocidad y la dificultad son orientativas: pueden variar según el proyecto, la configuración y la experiencia de quien lo desarrolla.*

### Jekyll

[Jekyll](https://jekyllrb.com/) está escrito en Ruby y utiliza Markdown y plantillas Liquid. Es una opción conocida para blogs y páginas personales; también se puede utilizar con GitHub Pages.

### Hugo

[Hugo](https://gohugo.io/) está escrito en Go. Destaca por generar sitios muy rápidamente y puede ser adecuado para proyectos grandes o con mucha documentación.

### Astro

[Astro](https://astro.build/) utiliza JavaScript/TypeScript y permite combinar contenido con componentes. Está orientado a webs modernas y puede integrar componentes de diferentes frameworks.

## 6. CMS dinámico y SSG: resumen

- Un CMS dinámico suele permitir modificar contenido desde un panel y generar páginas cuando se solicitan.
- Un SSG genera las páginas durante el *build* a partir de archivos y plantillas.
- Un CMS suele facilitar la edición a usuarios no técnicos.
- Un SSG suele ofrecer una entrega sencilla y rápida de páginas estáticas, aunque publicar cambios requiere generar de nuevo el sitio.

**Conclusión:** Jekyll, Hugo y Astro resuelven una necesidad parecida, pero se diferencian en sus herramientas, velocidad, ecosistema y forma de construir la web.

## 7. Vídeo explicativo

[Ver “What is a Static Site Generator?” de Fazt en YouTube](https://www.youtube.com/watch?v=osWfEtbP_sk)

*Comprueba la duración del vídeo antes de entregarlo y utiliza uno de cinco minutos como máximo, tal como pide la actividad.*

## 8. Fuentes y documentación oficial

- [Jekyll: documentación oficial](https://jekyllrb.com/docs/)
- [Hugo: documentación oficial](https://gohugo.io/documentation/)
- [Astro: documentación oficial](https://docs.astro.build/)

---

## Ejemplo adicional de Markdown

### Lista de tareas

- [x] Escribir el contenido de la actividad.
- [x] Comparar tres generadores estáticos.
- [ ] Comprobar la duración del vídeo elegido.

### Imagen de ejemplo

![Logotipo de Markdown](https://upload.wikimedia.org/wikipedia/commons/4/48/Markdown-mark.svg)

### Cita

> Un SSG combina contenido y plantillas para generar archivos web antes de que el visitante acceda a ellos.

### Código

```html
<h1>Mi sitio estático</h1>
<p>Esta página se genera previamente.</p>
```

### Formato de texto

Este texto está en **negrita**, este en *cursiva* y este ~~tachado~~.

---

*Documento elaborado en Markdown para la actividad de CMS y SSG.*
