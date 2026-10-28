# Gestores de contenido (CMS)

## Índice

1. [¿Qué es un CMS?](#1-qué-es-un-cms)
2. [¿Cómo funciona?](#2-cómo-funciona)
3. [Tipos de CMS](#3-tipos-de-cms)
4. [Top 5 de CMS y estadísticas de uso](#4-top-5-de-cms-y-estadísticas-de-uso)
5. [Ventajas e inconvenientes](#5-ventajas-e-inconvenientes)
6. [CMS dinámico frente a generador de sitios estáticos](#6-cms-dinámico-frente-a-generador-de-sitios-estáticos)
7. [Vídeo explicativo](#7-vídeo-explicativo)
8. [Fuentes y documentación](#8-fuentes-y-documentación)
9. [Documento relacionado](#9-documento-relacionado)

## 1. ¿Qué es un CMS?

Un **CMS** (*Content Management System* o sistema de gestión de contenidos) es una aplicación que permite **crear, modificar, organizar y publicar contenido web** sin tener que desarrollar una página desde cero. Normalmente se utiliza desde un panel de administración.

Por ejemplo, una persona puede redactar una entrada de blog, añadir imágenes, asignarle una categoría y publicarla sin escribir directamente todo el HTML.

## 2. ¿Cómo funciona?

El proceso habitual es el siguiente:

1. El usuario entra en el **panel de administración**.
2. Crea contenido o modifica el que ya existe.
3. Lo organiza mediante etiquetas, categorías, menús y secciones.
4. El CMS guarda el contenido, normalmente en una base de datos.
5. Cuando alguien visita la web, el sistema utiliza el contenido y las plantillas para mostrar la página.

```text
Administrador → Panel del CMS → Contenido y base de datos
                                      ↓
Visitante ← Página web generada ← Plantillas
```

## 3. Tipos de CMS

Los CMS se pueden clasificar según distintos criterios. Es importante no mezclar el propósito del sistema con la forma en que se aloja.

### Según su propósito

- **Generalistas:** permiten crear diferentes tipos de sitios web. Ejemplo: [WordPress](https://wordpress.org/).
- **Comercio electrónico:** están orientados a tiendas en línea. Ejemplo: [Shopify](https://www.shopify.com/).
- **Blogs y publicaciones:** facilitan la publicación de artículos. Ejemplo: [Ghost](https://ghost.org/).
- **Educativos:** permiten gestionar cursos y materiales formativos. Ejemplo: [Canvas LMS](https://www.instructure.com/canvas).
- **Corporativos:** ayudan a organizar la información de una empresa. Ejemplo: [Drupal](https://www.drupal.org/).
- **Foros y comunidades:** permiten organizar conversaciones entre usuarios. Ejemplo: [Discourse](https://www.discourse.org/).

### Según su arquitectura

- **Tradicional o acoplado:** la gestión del contenido y la presentación forman parte de un mismo sistema. Ejemplo: WordPress en una instalación tradicional.
- **Desacoplado:** el sistema de gestión y la parte visual están separados, aunque pueden estar conectados. Ejemplo: Drupal utilizado con un frontend independiente.
- **Headless:** administra el contenido y lo distribuye mediante una API; la presentación se desarrolla por separado. Ejemplo: [Strapi](https://strapi.io/).

### Según el modelo de alojamiento

- **Alojado o SaaS:** el proveedor ofrece la plataforma y se encarga de buena parte de la infraestructura. Ejemplos: [Wix](https://www.wix.com/) y [Squarespace](https://www.squarespace.com/).
- **Autoalojado:** la organización instala y mantiene el CMS en su propio servidor o alojamiento contratado. Ejemplo: WordPress descargado desde WordPress.org.

El alojamiento es un criterio distinto de la arquitectura: un CMS puede ser tradicional y autoalojado, o funcionar como servicio alojado.

## 4. Top 5 de CMS y estadísticas de uso

Según [W3Techs, estadísticas de uso de sistemas de gestión de contenidos](https://w3techs.com/technologies/overview/content_management), consultadas el **28 de octubre de 2026**, estos son los cinco CMS principales según su cuota entre los sitios web cuyo CMS ha podido identificar W3Techs.

| Puesto | CMS | Cuota entre sitios con CMS identificado | Porcentaje de todos los sitios web |
|:---:|---|---:|---:|
| 1 | [WordPress](https://wordpress.org/) | 58,3 % | 39,6 % |
| 2 | [Shopify](https://www.shopify.com/) | 7,9 % | 5,3 % |
| 3 | [Wix](https://www.wix.com/) | 6,2 % | 4,2 % |
| 4 | [Squarespace](https://www.squarespace.com/) | 3,6 % | 2,4 % |
| 5 | [Joomla](https://www.joomla.org/) | 1,6 % | 1,1 % |

![Gráfico de barras con la cuota de mercado de los cinco CMS principales](img/cuota_cms.png)

**Cómo interpretar los datos:** la columna «Cuota entre sitios con CMS identificado» compara los CMS entre sí. La última columna representa la proporción sobre todos los sitios web observados, incluidos aquellos cuyo CMS no se ha identificado. Por eso las dos cifras de cada plataforma son distintas.

WordPress destaca claramente en ambas medidas. Shopify y Wix aparecen a continuación, mientras que Squarespace y Joomla tienen cuotas menores. Estas cifras describen el uso detectado por W3Techs y no significan que un CMS sea necesariamente mejor que otro para cualquier proyecto.

## 5. Ventajas e inconvenientes

**Ventajas**

- Es fácil crear y mantener contenido desde un panel.
- Permite publicar con rapidez.
- Los temas y *plugins* añaden funciones.
- Facilita organizar grandes cantidades de contenido.

**Inconvenientes**

- Los *plugins* de terceros pueden introducir vulnerabilidades.
- Puede haber menos control sobre algunas partes del sistema.
- La web puede depender de extensiones concretas.
- La instalación y el mantenimiento requieren actualizaciones y medidas de seguridad.

> **Importante:** instalar muchos *plugins* no convierte automáticamente una web en mejor. Cada extensión debe ser necesaria y mantenerse actualizada.

## 6. CMS dinámico frente a generador de sitios estáticos

| Aspecto | CMS dinámico | Generador estático (SSG) |
|---|---|---|
| Edición habitual | Panel de administración | Archivos Markdown/MDX y otros archivos |
| Base de datos | Normalmente sí | No suele necesitar una base de datos para servir las páginas |
| Cuándo se genera el HTML | Dinámicamente cuando se solicita la página | Durante la compilación o *build*, antes de publicarla |
| Servidor | Necesita un entorno capaz de ejecutar el CMS y, normalmente, una base de datos | Puede servirse desde un servidor web sencillo o una CDN |
| Cambios de contenido | Se pueden publicar desde el panel | Se modifica el contenido y se vuelve a ejecutar el *build* |
| Seguridad | Mayor superficie de ataque en una instalación típica | Menor superficie de ataque en la parte pública, si solo se sirven archivos estáticos |
| Ejemplos | WordPress, Drupal y Joomla | Jekyll, Hugo y Astro |

### ¿Cuál elegir?

- Elige un **CMS dinámico** si necesitas que personas no técnicas actualicen contenido con frecuencia desde un panel.
- Elige un **SSG** si priorizas páginas rápidas, contenido versionado en archivos y una publicación sencilla.

No existe una opción universalmente mejor: depende del tipo de web, de quién la mantenga y de cómo se actualice.

## 7. Vídeo explicativo

[Ver «Qué es un CMS y para qué sirve (explicado en 2 minutos)», de David Zamora](https://www.youtube.com/watch?v=sSh5AAmItN0)

**Duración:** aproximadamente 2 minutos y 23 segundos, según la información disponible del vídeo. Cumple el límite de cinco minutos de la actividad.

## 8. Fuentes y documentación

- [W3Techs: estadísticas de uso de CMS](https://w3techs.com/technologies/overview/content_management). Consultado el 28 de octubre de 2026.
- [Documentación oficial de WordPress](https://wordpress.org/documentation/).
- [Shopify](https://www.shopify.com/).
- [Joomla](https://www.joomla.org/).

## 9. Documento relacionado

Continúa con la explicación de los generadores de sitios estáticos en **[ssg.md](ssg.md)**.

---

*Documento elaborado en Markdown para la actividad de CMS y SSG.*
