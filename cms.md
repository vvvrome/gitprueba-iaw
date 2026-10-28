# Gestores de contenido (CMS)

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

### Según su propósito

- **Generalistas:** permiten crear diferentes tipos de sitios web. Ejemplo: [WordPress](https://wordpress.org/).
- **Comercio electrónico:** están orientados a tiendas en línea. Ejemplo: [Shopify](https://www.shopify.com/).
- **Blogs y publicaciones:** facilitan la publicación de artículos.
- **Educativos:** permiten gestionar cursos y materiales formativos. Ejemplo: [Canvas LMS](https://www.instructure.com/canvas).
- **Corporativos:** organizan la información de una empresa.
- **Foros y comunidades:** permiten organizar conversaciones entre usuarios.

### Según su arquitectura

- **Tradicional o acoplado:** la gestión del contenido y la presentación forman parte de un mismo sistema.
- **Desacoplado:** el sistema de gestión y la parte visual están separados, aunque pueden estar conectados.
- **Headless:** administra el contenido y lo distribuye mediante una API; la presentación se desarrolla por separado.
- **Alojado:** el proveedor ofrece el servicio y se encarga de buena parte de la infraestructura. Ejemplos: [Wix](https://www.wix.com/) y [Squarespace](https://www.squarespace.com/).

## 4. Ejemplos de CMS conocidos

| CMS | Uso habitual | Característica |
|---|---|---|
| [WordPress](https://wordpress.org/) | Blogs y webs generales | Gran variedad de temas y extensiones |
| [Shopify](https://www.shopify.com/) | Tiendas en línea | Herramientas centradas en comercio electrónico |
| [Wix](https://www.wix.com/) | Webs de diferentes tipos | Editor visual y alojamiento integrado |
| [Squarespace](https://www.squarespace.com/) | Webs y portafolios | Plantillas y herramientas integradas |
| [Joomla](https://www.joomla.org/) | Webs generales | Gestión de contenidos y usuarios |

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

[Buscar un vídeo breve sobre qué es un CMS (máximo 5 minutos)](https://www.youtube.com/results?search_query=what+is+a+CMS+explained+in+5+minutes)

*Antes de entregar, comprueba que el vídeo que elijas no supera los cinco minutos.*

## 8. Más información

- [Documentación oficial de WordPress](https://wordpress.org/documentation/)
- [Shopify](https://www.shopify.com/)
- [Joomla](https://www.joomla.org/)

## 9. Enlace al documento sobre SSG

Continúa con la explicación de los generadores de sitios estáticos en **[ssg.md](ssg.md)**.

---

*Documento elaborado en Markdown para la actividad de CMS y SSG.*
