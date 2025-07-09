## ¿Qué es [[CURSO DEFINITIVO DE HTML Y CSS|HTML]]?
 El Lenguaje de Marcado de Hipertexto o HTML por sus siglas en inglés _(HyperText Markup Language)_ es el código para construir la **estructura** de una página web.
##  ¿Qué es [[CURSO DEFINITIVO DE HTML Y CSS||CSS]]?
El lenguaje de Hojas de Estilos en Cascada o CSS por sus siglas en inglés _(Cascade Style Sheets)_ es el código para **describir la presentación** de los elementos de la página web, los que definimos con HTML.

Para qué sirven las herramientas del navegador

**Las herramientas del navegador** son importantes para visualizar lo que ocurre con el código generado. Entre una de la opciones está identificar los elementos que están estructurados en la página web con sus respectivos estilos.
Las herramientas de desarrollador se despliegan con la combinación de teclas `F12` / `Ctrl + Shift + I` / `Cmd + Opt + I` o clic derecho e “Inspeccionar” en tu navegador preferido (se recomienda Google Chrome).

## Motores de Renderizado en Navegadores: Funcionamiento y Etapas
Los motores de renderizado son programas que **traducen nuestro código en un lenguaje que entienda el navegador**, de esta manera el programa sabrá que es lo que tiene que mostrar por pantalla al usuario.

## ¿Cuáles son los motores del navegador?

Los navegadores tienen sus propios motores: Chrome - Blink, Edge - Edge HTML, Safari - Webkit y Firefox - Gecko. **Todos realizan esta compilación de manera diferente, pero con el mismo resultado**, es decir, convierten los archivos a píxeles.
## Proceso de renderizado del motor del navegador

**El motor del navegador realiza 5 pasos o procesos para compilar nuestro código hasta el renderizado por pantalla.** Estos pasos son los siguientes:

1. Transforma los **archivos a un árbol de objetos** HTML o CSS, estos se denominan DOM (Document Object Model) y CSSDOM (Cascade Style Sheet Object Model), respectivamente. Cada nodo en el árbol es una representación de los elementos que contiene el archivo HTML o CSS.
2. **Calcula el estilo** correspondiente a cada nodo del DOM relacionado al CSSDOM.
3. **Calcula las dimensiones** de cada nodo y dónde va en la pantalla.
4. Pinta o renderiza los diferentes elementos como **cajas o contenedores**.
5. Agrupa todas las cajas en diferentes capas para **convertirlas en una imagen que se renderiza en pantalla**.

## Anatomia y Estructura de Documentos HTML
Antes de empezar a escribir código HTML, debemos conocer la [[CURSO DEFINITIVO DE HTML Y CSS#^estructura-html|Anatomia]] de un documento y sus elementos.
¿Cuáles son los elementos HTML?
Los elementos son **cada una de las partes que conforman un archivo HTML**. Su estructura contiene:
- **Etiquetas**: es la **representación de un elemento HTML**. Se dividen en etiquetas de apertura, representadas por `<etiqueta>` y etiquetas de cierre, representadas por `</etiqueta>`.
- **Contenido**: es el **texto o elementos encerrados por la etiqueta**, este valor es opcional en algunas de ellas. 
Qué son atributos HTML
Los atributos HTML son propiedades en la etiqueta de apertura que **manejan el comportamiento del elemento**. Su valor está envuelto en comillas.
Qué son los elementos vacíos
Los elementos vacíos son aquellos que únicamente **se representan en una etiqueta de apertura**. Por ejemplo, la etiqueta de imagen: `<img...>`.
Estas etiquetas pueden cerrarse en la misma etiqueta de apertura, utilizando la barra inclinada “/” al final: `<img.../>`,
Qué es el anidamiento de elementos
El anidamiento de elementos HTML consiste en **envolver varias etiquetas en otras etiquetas**.
**Interpreta a cada elemento HTML como una caja** donde puedes guardar diferentes elementos u otras cajas. Estas cajas tendrán diferentes tamaños y estarán colocadas junto a otras.
Aquellas etiquetas que envuelven a otras se las denomina **“padres”**. Es decir, `<section>` es padre de `<h1>`, `<p>`, `<ul>`, y a su vez `<ul>` es padre de 3 etiquetas `<li>`.
Las etiquetas que son el contenido de otras, se las denomina **“hijos”**. Es decir, las etiquetas `<h1>`, `<p>`, `<ul>` son hijos de `<section>`, y a su vez las etiquetas `<li>` son hijos de `<ul>`.
Estructura básica de un documento HTML
La estructura básica de un documento HTML está configurado por las siguientes etiquetas principales:
Etiqueta Doctype
La etiqueta `<!DOCTYPE html>` especifica que el archivo se maneje con la **versión 5 de HTML**.
Etiqueta html
La etiqueta `<html>` define el **elemento raíz** de un documento HTML. Todos los demás elementos deben estar contenidos dentro de este elemento raíz. En esta etiqueta se especifica el lenguaje de la página web mediante la propiedad `lang`.
Etiqueta head
La etiqueta `<head>` define la **metainformación**, es decir, toda información que no es contenido como tal de la página web. Por ejemplo, los enlaces a archivos CSS y JavaScript, el título y la imagen que aparecen en la pestaña del navegador. Esto es importante para motores de búsqueda como Google.
Etiqueta body
La etiqueta `<body>` define el **contenido de la página web**. Debe ser hijo cercano de `<html>` y padre de todas las etiquetas HTML, excepto por aquellas que definan metainformación.
Comentarios de HTML
**Los comentarios de HTML consiste en señalar algo que se ignorará**. Para establecer un comentario HTML se lo envuelve entre `<!--` y `-->`, independiente de la cantidad de líneas.

## # HTML Semántico: Mejora la Accesibilidad y SEO de tu Web
El HTML semántico consiste en que cada elemento tenga su propia etiqueta que lo **defina correctamente**. Sin utilizar etiquetas muy generales, como `<div>` o `<span>`.

El problema con la etiqueta _div_

La etiqueta `div` define un **bloque genérico de contenido**, que no tiene ningún valor semántico. Se **utiliza para elementos de diseño** como contenedores.
## ¿Cuáles son las [[CURSO TEORICO FRONTEND#^2e0db3|etiquetas semánticas]]?

^259217

Las etiquetas semánticas para definir una interfaz de una página web son:

- `<header>`: define el **encabezado** de la página (no confundir con `<head>`).
- `<nav>`: define una **barra de navegación** que incluye enlaces.
- `<section>`: define una **sección** de la página.
- `<footer>`: define un **pie de página o de sección**.
- `<article>`: define un **artículo**, el cual puede tener su propio encabezado, navegación, sección o pie de página.

Ahora que ya conoces las etiquetas semánticas, evita el uso excesivo de `<div>`.
Ventajas de utilizar HTML semántico

Las ventajas de utilizar un HTML semántico son:

- Ayuda a tu sitio a ser accesible
- Mejora tu posicionamiento (SEO)
- Código más claro, legible y mantenible
- Ayuda a buscadores (como Google) a encontrar tu página

## ¿Cuáles son las etiquetas HTML más utilizadas para el diseño de una página web?

Entender la estructura y el diseño de una página web a través de HTML es esencial para cualquier desarrollador web. Las etiquetas de layout son cruciales ya que definen la estructura básica del documento. Estas incluyen:

- `header`: define la cabecera de la página.
- `navbar`: se utiliza para la navegación.
- `section`: separa secciones del contenido.
- `article`: contiene contenido independiente.
- `aside`: incluye información complementaria.
- `footer`: marca el pie de página.

Estas etiquetas proporcionan un marco sólido para organizar el contenido dentro de una página web.

## ¿Cómo se manejan los enlaces y el texto en HTML?

Los enlaces y el texto son componentes vitales de cualquier página web. Los enlaces se manejan mediante la etiqueta anchor (`<a>`), que permite redirigir a los usuarios a otros sitios web o páginas internas con solo un clic o toque.

Para el manejo del texto, HTML proporciona distintas etiquetas de encabezado (`<h1>` hasta `<h6>`) que indican la jerarquía y la importancia de los títulos. Los párrafos se estructuran con la etiqueta `<p>`. Además, es posible estilizar textos dentro de un párrafo usando la etiqueta `<span>`, aunque no tiene significado semántico.

## ¿Cómo se integran las imágenes, videos y formularios en HTML?

Para incorporar imágenes y videos, las etiquetas `<img>`, `<svg>`, `<iframe>` y `<video>` son fundamentales. La etiqueta `<img>` es especialmente útil para añadir imágenes estáticas, mientras que para videos se puede utilizar `<iframe>` o `<video>`.

Los formularios son otro elemento indispensable en el desarrollo frontend. Con la estructura básica proporcionada por la etiqueta `<form>`, se pueden incluir diferentes tipos de campos como `<input>` (para texto, checkbox, etc.) y `<label>` que ofrece información sobre el input necesario.

Los botones también son esenciales no solo para enviar formularios sino para la funcionalidad de la página en general.

## ¿Cómo se estructuran listas y etiquetas autocerrables?

Las listas son una excelente forma de organizar información en HTML. Se crean usando etiquetas como `<ul>` para listas no ordenadas, `<ol>` para listas ordenadas y `<li>` para elementos individuales dentro de la lista.

En cuanto a las etiquetas autocerrables, como `<img>`, no necesitan una etiqueta de cierre específica. Esto simplifica el código manteniendo la página organizada y fácil de leer.
## Anatomía de una Declaración CSS: Selectores y Sintaxis Básica
## Qué es una declaración de CSS

Una declaración de CSS es un bloque que especifica el conjunto de estilos que se añadirán a un elemento HTML. Su estructura contiene lo siguiente:

- **Selector**: define el elemento o conjunto de elementos a los cuales se añadirán los estilos.
- **Propiedad**: es el nombre del estilo de CSS.
- **Valor**: es el valor que tomará la propiedad.
- ## Qué son comentarios de CSS

Los comentarios de CSS consisten en señalar algo que se ignorará. Para establecer un comentario CSS se lo envuelve entre `/*` y `*/`, independiente de la cantidad de líneas.
## Propiedades iniciales de CSS

Antes de empezar con CSS utilizaremos algunas propiedades de CSS.

- `color`: establece el color del texto de un elemento.
- `background-color`: establece un color de fondo al elemento.
- `font-size`: establece el tamaño de la fuente.
- `width`: establece la anchura de un elemento.
- `height`: establece la altura de un elemento.

## Medidas iniciales

Estas son las medidas iniciales que debes conocer para establecer tamaños de elementos o de tipografía:

- `px`: establece una longitud de píxeles.
- `%`: establece un porcentaje con respecto a una medida base.

##  Selectores CSS: básicos y combinadores
El selector define el elemento o conjunto de elementos HTML a los cuales se añadirán estilos. Existen [nombres de colores propios de CSS](https://htmlcolorcodes.com/es/nombres-de-los-colores/) que puedes explorar. A continuación veamos más sobre selectores.

## Cuáles son los selectores básicos

Un selector básico es la mínima expresión CSS para colocar estilos.

```css
selector {
    /* Estilos */
}
```
### 1. Selector de tipo

Selecciona todos los elementos que coincidan con el **nombre de la etiqueta HTML**.

```css
div {
    /* Todos los div en el documento */
}
```
### 2. Selector de clase

Selecciona todos los elementos que coincidan con las etiquetas HTML que **contengan el atributo `class`**.

```html
<!--archivo HTML-->
<div class="card"> Soy una carta </div>
```

Para seleccionar estos elementos, se empieza por un punto `.` y seguido el **valor exacto** del atributo `class` de la etiqueta. Puede ser cualquier valor que desees colocar.

```css
/* archivo CSS */
.card {
    /* Todas las etiquetas con la clase "card" */
}
```

Puede existir más de un valor dentro del atributo `class` separados por espacios.

```html
<!--archivo HTML-->
<div class="card card1"> Soy una carta </div>
<div class="card card2"> Soy una carta </div>
```

```css
.card {
    /* Todas las etiquetas con la clase "card" */
}

.card1 {
    /* Todas las etiquetas con la clase "card1" */
}

.card2 {
    /* Todas las etiquetas con la clase "card2" */
}
```
### 3. Selector de identificador único (id)

Selecciona el único elemento que coincida con la etiqueta HTML que **contenga el atributo `id`**. Solo puede existir un valor `id` para todo el documento.

```html
<!--archivo HTML-->
<button id="eliminar"> Eliminar  </button>
```

Para seleccionar el elemento, se empieza por el símbolo de _hashtag_ `#` y seguido el **valor exacto** del atributo `id` de la etiqueta. Puede ser cualquier valor que desees colocar.

```css
/* archivo CSS */
#eliminar {
    /* La única etiqueta con el id "eliminar" */
}
```
### 4. Selector de atributo

Selecciona los elementos que coincidan con la etiqueta HTML que **contenga el atributo y valor** especificado.

```html
<!--archivo HTML-->
<a href="https://platzi.com"> Ir a Platzi </a>
```

Para seleccionar los elementos, se empieza por el nombre de la etiqueta, seguido de corchetes `[]` que contiene el atributo y valor especificado.

```css
/* archivo CSS */
a[href=""https://platzi.com"] {
    /* Todas las etiquetas <a> con una propiedad href con valor "https://platzi.com" */
}
```
### 5. Selector universal

Selecciona todos los elementos del documento mediante un asterisco `*`.

```css
* {
    /* Todos los elementos */
}
```
## Cuáles son los selectores combinadores

Un selector combinador es la unión de dos o más selectores básicos.

```css
selector1 selector2 selector3 {
    /* Estilos */
}
```
### 1. Combinador de descendientes

Selecciona todos los elementos del selector de la derecha que son **hijos** del selector de la izquierda, **independientemente de la profundidad**. Estos selectores están separados por un espacio.

```css
padre hijos {
    /* Todos los hijos del padre */
}

div p{
    /* Todos los hijos <p> de <div>*/
}

.container img{
    /* Todos los hijos <img> de la clase "container"*/
}
```
### 2. Combinador de hijo directo

Selecciona todos los elementos del selector de la derecha que son **hijos directos** del selector de la izquierda. Estos selectores están separados por `>`.

```css
padre > hijos_directos {
    /* Todos los hijos directos del padre */
}

div > p{
    /* Todos los hijos directos <p> de <div>*/
}

.container > img{
    /* Todos los hijos directos <img> de la clase "container"*/
}
```
### 3. Combinador de elemento adyacente

Selecciona todos los elementos del selector de la derecha que están **adyacente** al selector de la izquierda. Estos selectores están separados por `+`.

```css
elemento + adyacente {
    /* Elementos adyacentes */
}

div + p{
    /* Todos los <p> adyacentes a <div>*/
}

.container + img{
    /* Todos los <img> adyacentes a la clase "container"*/
}
```

**Adyacente significa que comparten el mismo padre y está situado inmediatamente hacia abajo de otro elemento**. Por ejemplo, en el siguiente código, `<div>` está adyacente a `<h1>` y `<p>` está adyacente a `<div>`. Sin embargo, `<h1`> no está adyacente a `<div>` y `<div>` no está adyacente a `<p>`.

```html
<!--archivo HTML -->
<h1>Soy un título </h1>
<div>Soy un div</div>
<p>Soy un párrafo</p>
```
### 4. Combinador general de hermanos

Selecciona todos los elementos del selector de la derecha que son **hermanos** del selector de la izquierda. Estos selectores están separados por `~`.

```css
elemento ~ hermanos {
    /* Elementos hermanos */
}

div ~ p{
    /* Todos los <p> hermanos de <div>*/
}

.container ~ img{
    /* Todos los <img> hermanos de la clase "container"*/
}
```

**Hermanos significa que comparten el mismo padre y están situados hacia abajo de otro elemento**. Por ejemplo, en el siguiente código, `<div>` y `<p>` son hermanos de `<h1>`, pero `<h1>` no es hermano de `<div>` y `<p>`.

```html
<!--archivo HTML -->
<h1>Soy un título </h1>
<div>Soy un div</div>
<p>Soy un párrafo</p>
```

##  Selectores CSS: Pseudo Clases y Pseudo Elementos
Existen otros tipos de selectores, además de [los selectores básicos y combinadores](https://platzi.com/clases/2467-frontend-developer/40835-tipos-de-selectores-basicos-y-combinadores/), capaces de cambiar un estado o añadir algo más al elemento. Estos son denominados pseudoclases y pseudoelementos.

## Cuáles son las pseudoclases

Una pseudoclase define el estilo de **un estado** especial de un elemento.

- [Índice de pseudo-clases estándar](https://developer.mozilla.org/es/docs/Web/CSS/Pseudo-classes#indice_de_las_pseudo-clases_est%C3%A1ndar).

### Sintaxis

```css
selector : pseudoclase { 
    propiedad: valor;
}
```

### :hover

Representa el estado en el cual **el cursor está encima del elemento**.

- [Ejemplo](https://codi.link/PGRpdj5TZcOxw6FsYW1lPC9kaXY+%7CZGl2IHsNCiAgZm9udC1zaXplOiAzcmVtOw0KICBjdXJzb3I6IHBvaW50ZXI7DQp9DQoNCmRpdjpob3ZlciB7DQogIGNvbG9yOiByZWQ7DQp9%7C)

### :active

Representa el estado de un elemento que **no ha sido visitado**.

- [Ejemplo](https://codi.link/PGEgaHJlZj0iIyI+Q2xpY2tlYW1lPC9hPg==%7CYSB7DQogIGZvbnQtc2l6ZTogM3JlbTsNCn0NCg0KYTpsaW5rIHsNCiAgY29sb3I6IHJlZDsNCn0=%7C)

### :visited

Representa el estado de un elemento que **ya ha sido visitado**.

- [Ejemplo](https://codi.link/PGEgaHJlZj0iIyI+Q2xpY2tlYW1lPC9hPg==%7CYSB7DQogIGZvbnQtc2l6ZTogM3JlbTsNCn0NCg0KYTp2aXNpdGVkIHsNCiAgY29sb3I6IHJlZDsNCn0=%7C)

### :not()

Representa el estado en el cual **no coinciden los selectores que se indiquen**.

- [Ejemplo](https://codi.link/PGRpdj5BenVsPC9kaXY+DQo8ZGl2PkF6dWw8L2Rpdj4NCjxkaXYgY2xhc3M9Im5lZ3JvIj5OZWdybzwvZGl2Pg0KPGRpdj5BenVsPC9kaXY+DQo8ZGl2PkF6dWw8L2Rpdj4=%7CZGl2IHsNCiAgZm9udC1zaXplOiAzcmVtOw0KfQ0KDQpkaXY6bm90KC5uZWdybykgew0KICBjb2xvcjogYmx1ZTsNCn0=%7C)

### :nth-child()

Representa el estado en el cual **coinciden los hijos del elemento según el valor indicado**.

**Valores de palabras clave:**

- **odd:** los elementos hijos en posiciones impares.
- **even:** los elementos hijos en posiciones pares.

**Fórmula matemática:** `An+B` donde A y B son números enteros.

- [Ejemplo](https://codi.link/PGRpdj4xIE5lZ3JvPC9kaXY+DQo8ZGl2PjIgQXp1bDwvZGl2Pg0KPGRpdj4zIE5lZ3JvPC9kaXY+DQo8ZGl2PjQgTmVncm88L2Rpdj4NCjxkaXY+NSBOZWdybzwvZGl2Pg==%7CZGl2IHsNCiAgZm9udC1zaXplOiAzcmVtOw0KfQ0KDQpkaXY6bnRoLWNoaWxkKDIpIHsNCiAgY29sb3I6IGJsdWU7DQp9%7C)

## Cuáles son los pseudoselementos

Un pseudoelemento define el estilo de **una parte específica** de un elemento.

- [Lista de pseudo-elementos](https://developer.mozilla.org/es/docs/web/css/pseudo-elements#lista_de_pseudoelementos).

### Sintaxis

```css
selector :: pseudo-elemento { 
    propiedad: valor;
}
```

### ::before

Sirve para agregar un contenido **antes del elemento**. El contenido es agregado mediante la propiedad `content` de CSS.

- [Ejemplo](https://codi.link/PGgxPlTDrXR1bG88L2gxPg0KPGgyPlN1YnTDrXR1bG9zPC9oMj4NCjxoMj5TdWJ0w610dWxvczwvaDI+DQo8aDI+U3VidMOtdHVsb3M8L2gyPg0KPGgyPlN1YnTDrXR1bG9zPC9oMj4NCjxoMj5TdWJ0w610dWxvczwvaDI+DQo=%7CaDI6YmVmb3JlIHsNCiAgY29udGVudDogIiAqICI7DQogIGNvbG9yOiByZWQ7DQp9%7C)

### ::after

Sirve para agregar un contenido **después del elemento**. El contenido es agregado mediante la propiedad `content` de CSS.

- [Ejemplo](https://codi.link/PCEtLSBOYXZiYXIgaW1wcm92aXNhZGEgLS0+DQo8bmF2Pg0KICA8dWw+DQogICAgPGxpPkhvbWU8L2xpPg0KICAgIDxsaT5EZXN0YWNhZG9zPC9saT4NCiAgICA8bGk+RWxlbWVudG9zPC9saT4NCiAgICA8bGk+Q2xhc2VzPC9saT4NCiAgICA8bGk+TcOhcy4uLjwvbGk+DQogIDwvdWw+DQo8L25hdj4NCg==%7CbmF2IHVsIHsNCiAgbGlzdC1zdHlsZTogbm9uZTsNCiAgZGlzcGxheTogZmxleDsNCiAganVzdGlmeS1jb250ZW50OiBzcGFjZS1hcm91bmQ7DQogIGN1cnNvcjogcG9pbnRlcjsNCn0NCg0KbmF2IHVsIGxpOjphZnRlciB7DQogIGNvbnRlbnQ6ICJ8IjsNCiAgbWFyZ2luOiAxcmVtOw0KICBjb2xvcjogcmVkOw0KfQ==%7C)

### ::first-letter

Sirve para añadir estilos a a la **primera letra del texto** de cualquier elemento.

- [Ejemplo](https://codi.link/PHA+U295IG90cm8gcMOhcnJhZm88L3A+DQo8cD5Tb3kgb3RybyBww6FycmFmbzwvcD4NCjxwPlNveSBvdHJvIHDDoXJyYWZvPC9wPg0KPHA+U295IG90cm8gcMOhcnJhZm88L3A+DQo8cD5Tb3kgb3RybyBww6FycmFmbzwvcD4NCjxwPlNveSBvdHJvIHDDoXJyYWZvPC9wPg0KPHA+U295IG90cm8gcMOhcnJhZm88L3A+DQo8cD5Tb3kgb3RybyBww6FycmFmbzwvcD4NCjxwPlNveSBvdHJvIHDDoXJyYWZvPC9wPg0K%7COjpmaXJzdC1sZXR0ZXJ7DQogIGNvbG9yOiByZWQ7DQp9DQo=%7C)
