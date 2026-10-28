# Generadores de sitios estáticos (SSG)

## Índice

1. [¿Qué es un SSG?](#1-qué-es-un-ssg)
2. [¿Qué archivos utiliza?](#2-qué-archivos-utiliza)
3. [¿Cómo funciona?](#3-cómo-funciona)
4. [SSG frente a HTML manual](#4-ssg-frente-a-html-manual)
5. [Ventajas e inconvenientes](#5-ventajas-e-inconvenientes)
6. [Comparación de Jekyll, Hugo y Astro](#6-comparación-de-jekyll-hugo-y-astro)
7. [CMS dinámico y SSG: resumen](#7-cms-dinámico-y-ssg-resumen)
8. [Vídeo explicativo](#8-vídeo-explicativo)
9. [Fuentes y documentación oficial](#9-fuentes-y-documentación-oficial)

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

## 4. SSG frente a HTML manual

En una web HTML manual, cada página se escribe y mantiene como un archivo propio. Esto funciona bien para una web muy pequeña, pero los cambios repetidos pueden resultar laboriosos cuando hay muchas páginas.

Imaginemos una web con **50 páginas HTML** que comparten el mismo menú y el mismo pie de página:

- **HTML manual:** si el menú cambia, hay que modificar los 50 archivos y comprobar que el cambio se ha aplicado correctamente en todos.
- **Con un SSG:** el menú puede estar definido en una plantilla común. Se modifica esa plantilla y se vuelve a generar el sitio para aplicar el cambio a todas las páginas que la utilizan.

| Aspecto | HTML manual | SSG |
|---|---|---|
| Creación de páginas | Se escribe cada archivo HTML | El generador crea las páginas a partir del contenido y las plantillas |
| Cambio de diseño común | Puede requerir editar muchos archivos | Normalmente basta con modificar la plantilla compartida |
| Sitio muy pequeño | Puede ser la opción más sencilla | La configuración inicial puede ser innecesaria |
| Sitio con muchas páginas | Aumenta el trabajo repetitivo | Facilita mantener una estructura coherente |
| Publicación | Se suben los archivos HTML editados | Se ejecuta el *build* y se publica el resultado generado |

Por tanto, un SSG no es siempre mejor. Para una única página sencilla, escribir HTML directamente puede ser suficiente. Cuando muchas páginas comparten una estructura y se actualizan con frecuencia, las plantillas y la generación automática reducen el trabajo repetitivo.

## 5. Ventajas e inconvenientes

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

## 6. Comparación de Jekyll, Hugo y Astro

| Característica | Jekyll | Hugo | Astro |
|---|---|---|---|
| Lenguaje principal | Ruby | Go | JavaScript / TypeScript |
| Contenido habitual | Markdown + Front Matter | Markdown + Front Matter | Markdown, MDX y componentes |
| Herramientas de plantillas | Liquid | Plantillas de Hugo | Componentes de Astro y compatibilidad con otros frameworks |
| Instalación o entorno | Ruby y RubyGems | Binario de Hugo | Node.js y un gestor de paquetes |
| Velocidad de generación | Media | Muy alta | Alta |
| Curva de aprendizaje (orientativa) | Baja-media | Media | Media |
| Usos típicos | Blogs, documentación y páginas personales | Sitios grandes y documentación | Webs modernas y portafolios |
| GitHub Pages | Compatible de forma directa con la configuración admitida por GitHub Pages | Normalmente requiere generar el sitio antes y publicar los archivos resultantes | Requiere generar y publicar los archivos de salida con una configuración adecuada |

*La velocidad y la dificultad son orientativas: pueden variar según el proyecto, la configuración y la experiencia de quien lo desarrolla.*

### Jekyll

[Jekyll](https://jekyllrb.com/) está escrito en Ruby y utiliza Markdown y plantillas Liquid. Es una opción conocida para blogs y páginas personales; también se puede utilizar con GitHub Pages.

**Ventajas:** integración directa con GitHub Pages y un flujo de trabajo conocido para sitios basados en Markdown.

**Inconvenientes:** requiere un entorno Ruby y aprender Liquid; puede ser menos cómodo si el proyecto necesita componentes modernos complejos.

### Hugo

[Hugo](https://gohugo.io/) está escrito en Go. Destaca por generar sitios muy rápidamente y puede ser adecuado para proyectos grandes o con mucha documentación.

**Ventajas:** generación rápida y distribución mediante un ejecutable, sin necesidad de instalar Ruby para usar el generador.

**Inconvenientes:** hay que aprender su sistema propio de plantillas y su configuración; la integración con el alojamiento debe prepararse según el proyecto.

### Astro

[Astro](https://astro.build/) utiliza JavaScript/TypeScript y permite combinar contenido con componentes. Está orientado a webs modernas y puede integrar componentes de diferentes frameworks.

**Ventajas:** arquitectura basada en componentes, integración con herramientas modernas y posibilidad de generar páginas estáticas.

**Inconvenientes:** requiere Node.js y un gestor de paquetes, y puede tener una curva de aprendizaje mayor si no se conoce JavaScript. También admite renderizado bajo demanda, por lo que no todos los proyectos Astro son necesariamente estáticos.

## 7. CMS dinámico y SSG: resumen

- Un CMS dinámico suele permitir modificar contenido desde un panel y generar páginas cuando se solicitan.
- Un SSG genera las páginas durante el *build* a partir de archivos y plantillas.
- Un CMS suele facilitar la edición a usuarios no técnicos.
- Un SSG suele ofrecer una entrega sencilla y rápida de páginas estáticas, aunque publicar cambios requiere generar de nuevo el sitio.

**Conclusión:** Jekyll, Hugo y Astro resuelven una necesidad parecida, pero se diferencian en sus herramientas, velocidad, ecosistema y forma de construir la web.

## 8. Vídeo explicativo

[Ver «Hugo in 100 Seconds», de Fireship](https://www.youtube.com/watch?v=0RKpf3rK57I)

El vídeo presenta Hugo de forma breve y se titula «in 100 Seconds» (100 segundos), por lo que está dentro del límite de cinco minutos de la actividad.

## 9. Fuentes y documentación oficial

- [Jekyll: documentación oficial](https://jekyllrb.com/docs/)
- [Hugo: documentación oficial](https://gohugo.io/documentation/)
- [Astro: documentación oficial](https://docs.astro.build/)

---

---

*Documento elaborado en Markdown para la actividad de CMS y SSG.*
