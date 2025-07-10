# Introducción al desarrollo frontend

## Fundamentos de HTML y CSS
### ¿Qué es [[CURSO DEFINITIVO DE HTML Y CSS|HTML]]?
 El Lenguaje de Marcado de Hipertexto o HTML por sus siglas en inglés _(HyperText Markup Language)_ es el código para construir la **estructura** de una página web.
###  ¿Qué es [[CURSO DEFINITIVO DE HTML Y CSS||CSS]]?
El lenguaje de Hojas de Estilos en Cascada o CSS por sus siglas en inglés _(Cascade Style Sheets)_ es el código para **describir la presentación** de los elementos de la página web, los que definimos con HTML.

### Para qué sirven las herramientas del navegador

**Las herramientas del navegador** son importantes para visualizar lo que ocurre con el código generado. Entre una de la opciones está identificar los elementos que están estructurados en la página web con sus respectivos estilos.
Las herramientas de desarrollador se despliegan con la combinación de teclas `F12` / `Ctrl + Shift + I` / `Cmd + Opt + I` o clic derecho e “Inspeccionar” en tu navegador preferido (se recomienda Google Chrome).

## Motores de Renderizado en Navegadores: Funcionamiento y Etapas
Los motores de renderizado son programas que **traducen nuestro código en un lenguaje que entienda el navegador**, de esta manera el programa sabrá que es lo que tiene que mostrar por pantalla al usuario.

### ¿Cuáles son los motores del navegador?

Los navegadores tienen sus propios motores: Chrome - Blink, Edge - Edge HTML, Safari - Webkit y Firefox - Gecko. **Todos realizan esta compilación de manera diferente, pero con el mismo resultado**, es decir, convierten los archivos a píxeles.
### Proceso de renderizado del motor del navegador

**El motor del navegador realiza 5 pasos o procesos para compilar nuestro código hasta el renderizado por pantalla.** Estos pasos son los siguientes:

1. Transforma los **archivos a un árbol de objetos** HTML o CSS, estos se denominan DOM (Document Object Model) y CSSDOM (Cascade Style Sheet Object Model), respectivamente. Cada nodo en el árbol es una representación de los elementos que contiene el archivo HTML o CSS.
2. **Calcula el estilo** correspondiente a cada nodo del DOM relacionado al CSSDOM.
3. **Calcula las dimensiones** de cada nodo y dónde va en la pantalla.
4. Pinta o renderiza los diferentes elementos como **cajas o contenedores**.
5. Agrupa todas las cajas en diferentes capas para **convertirlas en una imagen que se renderiza en pantalla**.
# Maquetación con HTML
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

##  HTML Semántico: Mejora la Accesibilidad y SEO de tu Web
El HTML semántico consiste en que cada elemento tenga su propia etiqueta que lo **defina correctamente**. Sin utilizar etiquetas muy generales, como `<div>` o `<span>`.

El problema con la etiqueta _div_

La etiqueta `div` define un **bloque genérico de contenido**, que no tiene ningún valor semántico. Se **utiliza para elementos de diseño** como contenedores.
### ¿Cuáles son las [[CURSO TEORICO FRONTEND#^2e0db3|etiquetas semánticas]]?

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

## Etiquetas HTML esenciales para estructurar una página web
### ¿Cuáles son las etiquetas HTML más utilizadas para el diseño de una página web?

Entender la estructura y el diseño de una página web a través de HTML es esencial para cualquier desarrollador web. Las etiquetas de layout son cruciales ya que definen la estructura básica del documento. Estas incluyen:

- `header`: define la cabecera de la página.
- `navbar`: se utiliza para la navegación.
- `section`: separa secciones del contenido.
- `article`: contiene contenido independiente.
- `aside`: incluye información complementaria.
- `footer`: marca el pie de página.

Estas etiquetas proporcionan un marco sólido para organizar el contenido dentro de una página web.

### ¿Cómo se manejan los enlaces y el texto en HTML?

Los enlaces y el texto son componentes vitales de cualquier página web. Los enlaces se manejan mediante la etiqueta anchor (`<a>`), que permite redirigir a los usuarios a otros sitios web o páginas internas con solo un clic o toque.

Para el manejo del texto, HTML proporciona distintas etiquetas de encabezado (`<h1>` hasta `<h6>`) que indican la jerarquía y la importancia de los títulos. Los párrafos se estructuran con la etiqueta `<p>`. Además, es posible estilizar textos dentro de un párrafo usando la etiqueta `<span>`, aunque no tiene significado semántico.

### ¿Cómo se integran las imágenes, videos y formularios en HTML?

Para incorporar imágenes y videos, las etiquetas `<img>`, `<svg>`, `<iframe>` y `<video>` son fundamentales. La etiqueta `<img>` es especialmente útil para añadir imágenes estáticas, mientras que para videos se puede utilizar `<iframe>` o `<video>`.

Los formularios son otro elemento indispensable en el desarrollo frontend. Con la estructura básica proporcionada por la etiqueta `<form>`, se pueden incluir diferentes tipos de campos como `<input>` (para texto, checkbox, etc.) y `<label>` que ofrece información sobre el input necesario.

Los botones también son esenciales no solo para enviar formularios sino para la funcionalidad de la página en general.

## ¿Cómo se estructuran listas y etiquetas autocerrables?

Las listas son una excelente forma de organizar información en HTML. Se crean usando etiquetas como `<ul>` para listas no ordenadas, `<ol>` para listas ordenadas y `<li>` para elementos individuales dentro de la lista.

En cuanto a las etiquetas autocerrables, como `<img>`, no necesitan una etiqueta de cierre específica. Esto simplifica el código manteniendo la página organizada y fácil de leer.

# Maquetación con CSS
## Anatomía de una Declaración CSS: Selectores y Sintaxis Básica
### Qué es una declaración de CSS

Una declaración de CSS es un bloque que especifica el conjunto de estilos que se añadirán a un elemento HTML. Su estructura contiene lo siguiente:

- **Selector**: define el elemento o conjunto de elementos a los cuales se añadirán los estilos.
- **Propiedad**: es el nombre del estilo de CSS.
- **Valor**: es el valor que tomará la propiedad.
### Qué son comentarios de CSS

Los comentarios de CSS consisten en señalar algo que se ignorará. Para establecer un comentario CSS se lo envuelve entre `/*` y `*/`, independiente de la cantidad de líneas.
### Propiedades iniciales de CSS

Antes de empezar con CSS utilizaremos algunas propiedades de CSS.

- `color`: establece el color del texto de un elemento.
- `background-color`: establece un color de fondo al elemento.
- `font-size`: establece el tamaño de la fuente.
- `width`: establece la anchura de un elemento.
- `height`: establece la altura de un elemento.

### Medidas iniciales

Estas son las medidas iniciales que debes conocer para establecer tamaños de elementos o de tipografía:

- `px`: establece una longitud de píxeles.
- `%`: establece un porcentaje con respecto a una medida base.

##  Selectores CSS: básicos y combinadores
El selector define el elemento o conjunto de elementos HTML a los cuales se añadirán estilos. Existen [nombres de colores propios de CSS](https://htmlcolorcodes.com/es/nombres-de-los-colores/) que puedes explorar. A continuación veamos más sobre selectores.

### Cuáles son los selectores básicos

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

### Cuáles son las pseudoclases

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

### Cuáles son los pseudoselementos

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
##  Cascada y Especificidad en CSS: Domina el Orden y Prioridad de Estilos

### Qué es la cascada en CSS

La cascada es el concepto que determina **qué estilos se colocan sobre otros, priorizando a aquellos que se encuentren más abajo del código**. Recordarás que CSS es la abreviación de _Cascade Style Sheets_, que traducido es hojas de estilos en **Cascada**.

![Representación gráfica de la cascada en CSS](https://static.platzi.com/media/articlases/Images/frontend_developer16.png)

Mira el siguiente código e identifica de qué color de letra tendrá la etiqueta `<h1>`.

```css
h1 {
    color: red;
}

h1 {
    color: blue;
}
```

La etiqueta `<h1>` tendrá un color `blue` de letra, esto porque está situado más abajo en el código. Esto ocurre con cada propiedad de CSS que se repita en algún punto más arriba del código.

- [Ejemplo de cascada](https://codi.link/PGgxPkNhc2NhZGE8L2gxPg==%7CaDEgew0KICBjb2xvcjogcmVkOw0KfQ0KDQpoMSB7DQogIGNvbG9yOiBibHVlOw0KfQ==%7C)

Sin embargo, esto ocurre cuando la especificidad de una regla CSS tiene el mismo valor. Pero, ¿qué es especificidad?

### Qué es especificidad en CSS

La especificidad consiste en dar un valor a una regla CSS sobre **qué tan específico es el estilo**, esto para que los navegadores puedan saber qué estilos aplicar sobre otros, independientemente de dónde se encuentren en el código. **El estilo se aplicará donde la especificidad sea mayor.**

### Tipos de especificidad en CSS

Existen 6 tipos de especificidad con su respectivo valor, donde `X` es la cantidad de estilos que lo contienen. Mira la siguiente imagen:

![Tipos de especificidad en CSS](https://static.platzi.com/media/user_upload/especificidad-a630e9d4-545b-4ac1-9fb3-0e443ea066ea.jpg)

### Valor con mayor especificidad

La palabra reservada `!important` es **un valor de toda propiedad CSS que provee una especificidad de `10000`**, por lo que se aplicará ante otros estilos. Esto es una mala práctica y no deberías utilizarlo.

```css
h1 {
    color: red !important;
}
```

- [Ejemplo de !important](https://codi.link/PGgxPkVzcGVjaWZpY2lkYWQ8L2gxPg0K%7CaDEgew0KICBjb2xvcjogcmVkOw0KfQ0KDQpoMSB7DQogIGNvbG9yOiBncmVlbiAhaW1wb3J0YW50Ow0KfQ0KDQpoMSB7DQogIGNvbG9yOiBibHVlOw0KfQ0KDQpoMSB7DQogIGNvbG9yOiBwYXBheWF3aGlwOw0KfQ0K%7C)

### Estilos en línea

Los estilos en línea **son las propiedades CSS escritas en el HTML a través de la propiedad `style` de toda etiqueta**. También es una mala práctica y debes evitarlo.

```html
<h1 style="color: blue;">Especificidad</h1>
```

- [Ejemplo de estilos en línea](https://codi.link/PGgxIHN0eWxlPSJjb2xvcjogYmx1ZTsiPkVzcGVjaWZpY2lkYWQ8L2gxPg0K%7CaDEgew0KICBjb2xvcjogcmVkOw0KfQ0KDQpoMSB7DQogIGNvbG9yOiBncmVlbjsNCn0NCg0K%7C)

### Especificidad en selectores

El tema de los selectores ya lo conoces, por lo tanto, los selectores de tipo ID son más específicos que las clases, atributos y pseudoclases. Estas últimas son más específicas que los elementos y pseudoelementos. El selector universal tiene una especificidad de `0`.

En un proyecto deberías evitar los `!important` y estilos en línea, para trabajar únicamente con la especificidad de los selectores. Sin embargo, **debes tener presente que los selectores combinadores suman la especificidad de cada selector básico para obtener la especificidad total de la regla CSS**.

![Cálculo de la especificidad en selectores combinadores](https://static.platzi.com/media/articlases/Images/frontend_developer18.png)

Si utilizas Visual Studio Code y mantienes el _mouse_ sobre el selector, te mostrará la especificidad total.

##  Tipos de Display en CSS: Inline, Bloque e Inline-Block
La propiedad `display` establece el **tipo de visualización de los elementos HTML sin afectar el flujo normal de los elementos**.

![Visualización de elementos en CSS](https://static.platzi.com/media/articlases/Images/frontend_developer19.png)

Existen etiquetas que por defecto su display ya está determinado, como la etiqueta `<div>` que tiene display `block`, `<span>` tiene display `inline` y `<button>` tiene display `inline-block`.

Abordaremos los tipos de display `block`, `inline` e `inline-block` a continuación.

### Visualización en bloque (`block`)

El display `block` **establece que un elemento ocupará todo el espacio disponible por defecto y el siguiente elemento a este se situará por debajo.

Es posible **añadir medidas** de anchura `width` y altura `height` a estos a elementos.

También es posible **agregar todas las propiedades del modelo de caja** (no te preocupes de este concepto, ya lo abordaremos).

- [Ejemplo de display block](https://codi.link/PGRpdj5Tb3kgZGlzcGxheSBibG9jazwvZGl2Pg0KPGRpdj5Tb3kgZGlzcGxheSBibG9jazwvZGl2Pg0KPGRpdiBjbGFzcz0iY29uX21lZGlkYXMiPlNveSBkaXNwbGF5IGJsb2NrPC9kaXY+DQoNCg==%7CLyogUXVpdGEgbG9zIGNvbWVudGFyaW9zIHkgb2JzZXJ2YSBlbCBjb21wb3J0YW1pZW50byAqLw0KZGl2ew0KICBiYWNrZ3JvdW5kLWNvbG9yOiBhcXVhOw0KICAvKiBtYXJnaW46IDEwcHg7ICovDQogIC8qIHBhZGRpbmc6IDEwcHg7ICovDQp9DQoNCi5jb25fbWVkaWRhcyB7DQogIC8qIHdpZHRoOiAyMDBweDsgKi8NCiAgLyogaGVpZ2h0OiAyMDBweDsgKi8NCn0NCg0KLyogSWdub3JhIGVzdG9zIGVzdGlsb3MsIHBvciBhaG9yYSAqLw0KKiB7DQogIGZvbnQtc2l6ZTogMS4ycmVtOw0KICBtYXJnaW46IDA7DQp9DQoNCg0KDQo=%7C)

### Visualización en línea (`inline`)

El display `inline` **establece que un elemento ocupará el espacio del contenido del mismo y el siguiente elemento se situará a la derecha**.

**No es posible añadir medidas** de anchura `width` y altura `height` a estos a elementos.

También, **no es posible agregar todas las propiedades del modelo de caja, únicamente funcionará la propiedad `margin` en el eje horizontal** (no te preocupes de este concepto, ya lo abordaremos).

- [Ejemplo de display inline](https://codi.link/PHNwYW4+U295IGRpc3BsYXkgaW5saW5lPC9zcGFuPg0KPHNwYW4+U295IGRpc3BsYXkgaW5saW5lPC9zcGFuPg0KPHNwYW4+U295IGRpc3BsYXkgaW5saW5lPC9zcGFuPg0KPHNwYW4+U295IGRpc3BsYXkgaW5saW5lPC9zcGFuPg0KPHNwYW4gY2xhc3M9ImNvbl9tZWRpZGFzIj5Tb3kgZGlzcGxheSBpbmxpbmU8L3NwYW4+DQoNCg==%7CLyogUXVpdGEgeSBhZ3JlZ2EgbG9zIGNvbWVudGFyaW9zIHkgb2JzZXJ2YSBlbCBjb21wb3J0YW1pZW50byAqLw0Kc3BhbnsNCiAgYmFja2dyb3VuZC1jb2xvcjogYXF1YTsNCiAgLyogbWFyZ2luOiAyMHB4OyAqLw0KICAvKiBwYWRkaW5nOiAyMHB4OyAqLw0KfQ0KDQouY29uX21lZGlkYXMgew0KICAvKiB3aWR0aDogMjAwcHg7ICovDQogIC8qIGhlaWdodDogMjAwcHg7ICovDQp9DQoNCi8qIElnbm9yYSBlc3RvcyBlc3RpbG9zLCBwb3IgYWhvcmEgKi8NCiogew0KICBmb250LXNpemU6IDEuMnJlbTsNCiAgbWFyZ2luOiAwOw0KfQ0KDQoNCg0K%7C)

### Visualización de bloque y línea (`inline-block`)

El display `inline-block` combina las ventajas de `bloque` de colocar medidas al elemento y propiedades del modelo de caja correctamente; con las ventajas de `inline` de color un elemento seguido de otro en el mismo espacio.

Si elemento excede el contenido total, se coloca en la siguiente línea por debajo.

- [Ejemplo de display inline-block](https://codi.link/PGJ1dHRvbj5Tb3kgZGlzcGxheSBpbmxpbmUtYmxvY2s8L2J1dHRvbj4NCjxidXR0b24+U295IGRpc3BsYXkgaW5saW5lLWJsb2NrPC9idXR0b24+DQo8YnV0dG9uPlNveSBkaXNwbGF5IGlubGluZS1ibG9jazwvYnV0dG9uPg0KPGJ1dHRvbj5Tb3kgZGlzcGxheSBpbmxpbmUtYmxvY2s8L2J1dHRvbj4NCjxidXR0b24gY2xhc3M9ImNvbl9tZWRpZGFzIj5Tb3kgZGlzcGxheSBpbmxpbmUtYmxvY2s8L2J1dHRvbj4NCg0K%7CLyogUXVpdGEgbG9zIGNvbWVudGFyaW9zIHkgb2JzZXJ2YSBlbCBjb21wb3J0YW1pZW50byAqLw0KYnV0dG9uew0KICAvKiBtYXJnaW46IDEwcHg7ICovDQogIC8qIHBhZGRpbmc6IDEwcHg7ICovDQp9DQoNCi5jb25fbWVkaWRhcyB7DQogIC8qIHdpZHRoOiAzMDBweDsgKi8NCiAgLyogaGVpZ2h0OiAxMDBweDsgKi8NCn0NCg0KLyogSWdub3JhIGVzdG9zIGVzdGlsb3MsIHBvciBhaG9yYSAqLw0KKiB7DQogIGZvbnQtc2l6ZTogMS4xcmVtOw0KICBtYXJnaW46IDA7DQp9DQoNCg0KDQo=%7C)

##  Flexbox y CSS Grid: Fundamentos y Aplicaciones Prácticas
### Visualización nula (`none`)

El display `none` **desactiva la visualización de un elemento**, como si el elemento no existiera.

- [Ejemplo de display none](https://codi.link/PGRpdj48L2Rpdj4NCjxkaXY+PC9kaXY+DQo8ZGl2IGNsYXNzPSJkZXNhcGFyZWNlciI+DQogIEVuIG1pIHNpZ3VpZW50ZSB0cnVjbywgwqF2b3kgYSBkZXNhcGFyZWNlciENCjwvZGl2Pg0KPGRpdj48L2Rpdj4NCjxkaXY+PC9kaXY+DQo=%7CLyogUXVpdGEgbG9zIGNvbWVudGFyaW9zIHkgb2JzZXJ2YSBlbCBjb21wb3J0YW1pZW50byAqLw0KLmRlc2FwYXJlY2Vyew0KICAvKiBkaXNwbGF5OiBub25lOyAqLw0KICBiYWNrZ3JvdW5kLWNvbG9yOiBjb3JuZmxvd2VyYmx1ZTsNCiAgDQp9DQoNCi8qIElnbm9yYSBlc3RvcyBlc3RpbG9zLCBwb3IgYWhvcmEgKi8NCiogew0KICBib3gtc2l6aW5nOiBib3JkZXItYm94Ow0KICBmb250LXNpemU6IDEuMXJlbTsNCiAgbWFyZ2luOiAwOw0KfQ0KDQpib2R5ew0KICBkaXNwbGF5OiBmbGV4Ow0KfQ0KDQpkaXZ7DQogIGJhY2tncm91bmQtY29sb3I6IGNvcmFsOw0KICB3aWR0aDogMTIwcHg7DQogIGhlaWdodDogMTIwcHg7DQogIGZvbnQtd2VpZ2h0OiA4MDA7DQogIHBhZGRpbmc6IDhweDsNCn0NCg0KDQoNCg==%7C)

El display `flex` y `grid` son formas de visualización de elementos recientes y cada uno tienen sus propias características para crear interfaces de manera efectiva, a partir de un contenedor padre que dotará a los elementos hijos de superpoderes del posicionamiento.

Ambas son herramientas muy útiles en el desarrollo, especialmente para la creación de interfaces amigables al usuario y aptas para cualquier dispositivo, que este último se lo conoce como [responsive design](https://platzi.com/clases/2467-frontend-developer/40845-responsive-design/).

Sin embargo, ambas herramientas tienen temas muy extensos de entender, y como mi intención no es estresarte con demasiada información, simplemente ten presente de manera general en qué consisten.

### Qué es flexbox

_Flexbox_ consiste en el **ordenamiento de elementos hijos en un solo eje**, por defecto horizontalmente. El elemento padre o contenedor deberá contener la propiedad `display` con el valor `flex`. A partir de aquí, ya puedes ordenar los hijos según sea necesario.

- [Ejemplo de flexbox](https://codi.link/PGRpdiBjbGFzcz0iY29udGFpbmVyIj4NCiAgPGRpdj48L2Rpdj4NCiAgPGRpdj48L2Rpdj4NCiAgPGRpdj48L2Rpdj4NCiAgPGRpdj48L2Rpdj4NCiAgPGRpdj48L2Rpdj4NCjwvZGl2Pg0KDQoNCg0K%7CKiB7DQogIG1hcmdpbjogMDsNCiAgcGFkZGluZzogMDsNCiAgYm94LXNpemluZzogYm9yZGVyLWJveDsNCn0NCg0KLyogUXVpdGEgbG9zIGNvbWVudGFyaW9zIHkgb2JzZXJ2YSBlbCBjb21wb3J0YW1pZW50byAqLw0KLmNvbnRhaW5lcnsNCiAgLyogZGlzcGxheTogZmxleDsgKi8NCn0NCg0KLmNvbnRhaW5lciBkaXYgew0KICB3aWR0aDogMTAwcHg7IA0KICBoZWlnaHQ6IDEwMHB4Ow0KfQ0KDQouY29udGFpbmVyIGRpdjpudGgtY2hpbGQoMm4pew0KICBiYWNrZ3JvdW5kLWNvbG9yOiBhcXVhOw0KfQ0KDQouY29udGFpbmVyIGRpdjpudGgtY2hpbGQoMm4rMSl7DQogIGJhY2tncm91bmQtY29sb3I6IGJyb3duOw0KfQ0KDQoNCg0KDQoNCg0K%7C)

Cuando domines los temas básicos de CSS y las propiedades más usadas, revisadas en el contenido del curso, sigue con _Flexbox_. Puedes utilizar la guía y el curso en Platzi sobre el tema:

- [A Complete Guide to Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
- [Curso de Diseño Web con CSS Grid y Flexbox](https://platzi.com/clases/flexbox-css-grid/)

### Qué es grid

_Grid_ consiste en el **ordenamiento de elementos hijos en dos ejes**, como si fuera una cuadrícula o tabla. El elemento padre o contenedor deberá contener la propiedad `display` con el valor `grid` y debes definir las medidas de las columnas y de las filas. A partir de aquí, ya puedes ordenar los hijos según sea necesario.

- [Ejemplo de grid](https://codi.link/PGRpdiBjbGFzcz0iY29udGFpbmVyIj4NCiAgPGRpdj48L2Rpdj4NCiAgPGRpdj48L2Rpdj4NCiAgPGRpdj48L2Rpdj4NCiAgPGRpdj48L2Rpdj4NCiAgPGRpdj48L2Rpdj4NCiAgPGRpdj48L2Rpdj4NCiAgPGRpdj48L2Rpdj4NCiAgPGRpdj48L2Rpdj4NCiAgPGRpdj48L2Rpdj4NCjwvZGl2Pg0KDQoNCg0K%7CKiB7DQogIG1hcmdpbjogMDsNCiAgcGFkZGluZzogMDsNCiAgYm94LXNpemluZzogYm9yZGVyLWJveDsNCn0NCg0KLyogUXVpdGEgbG9zIGNvbWVudGFyaW9zIHkgb2JzZXJ2YSBlbCBjb21wb3J0YW1pZW50byAqLw0KLmNvbnRhaW5lcnsNCi8qICAgDQogIGRpc3BsYXk6IGdyaWQ7DQogIGdyaWQtdGVtcGxhdGUtY29sdW1uczogMTAwcHggMTAwcHggMTAwcHg7DQogIGdyaWQtdGVtcGxhdGUtcm93czogMTAwcHggMTAwcHggMTAwcHg7IA0KICAqLw0KDQoNCn0NCg0KLmNvbnRhaW5lciBkaXYgew0KICB3aWR0aDogMTAwcHg7IA0KICBoZWlnaHQ6IDEwMHB4Ow0KfQ0KDQouY29udGFpbmVyIGRpdjpudGgtY2hpbGQoMm4pew0KICBiYWNrZ3JvdW5kLWNvbG9yOiBhcXVhOw0KfQ0KDQouY29udGFpbmVyIGRpdjpudGgtY2hpbGQoMm4rMSl7DQogIGJhY2tncm91bmQtY29sb3I6IGJyb3duOw0KfQ0KDQoNCg0KDQoNCg0K%7C)

Cuando domines lo básico de _Flexbox_, sigue con _Grid_. Puedes utilizar la guía y el curso en Platzi que tenemos sobre el tema:

- [A Complete Guide to Grid](https://css-tricks.com/snippets/css/complete-guide-grid/)
- [Curso de CSS Grid Básico](https://platzi.com/cursos/css-grid/)

Y cuando domines lo básico de ambas, sigue con el [Curso de Diseño Web con CSS Grid y Flexbox](https://platzi.com/cursos/flexbox-css-grid/). Para que aprendas a emplear y combinar ambas herramientas correctamente.

##  Modelo de Caja en CSS: Propiedades y Uso Práctico
El modelo de caja se compone de cuatro elementos: _margin, border, padding_ y contenido.

![Representación del modelo de caja en CSS](https://static.platzi.com/media/articlases/Images/frontend_developer20.png)

Si entras a las herramientas de desarrollador de tu navegador y señalas un elemento HTML, en la sección de estilos te aparecerá una vista parecida a la anterior imagen, este es el modelo de caja del elemento señalado.

### Qué es el contenido del elemento HTML

**El contenido del elemento, como su nombre lo indica, es todo lo que está dentro del elemento**. Este tiene medidas establecidas por las propiedades `width` y `height`, que representan la anchura y la altura, respectivamente. Si imaginamos una caja, este valor sería todo lo que decidas colocar dentro.

```css
div {
    width: 100px;
    height: 100px;
}
```

### Qué son los bordes del elemento HTML

**El `border` consiste en el perfil o borde de un elemento HTML**. Si imaginamos una caja, sería la caja en sí. Para definir un borde es necesario utilizar las siguientes tres propiedades:

- `border-color`: establece el **color** del borde.
- `border-style`: establece el **estilo propio** del borde, estos pueden ser: `none` (sin borde), `dotted` (puntos), `dashed` (guiones), `solid` (continuo), `double` (doble continuo), `groove` (recuadro).
- `border-width`: estable la **anchura** del borde.

También se puede establecer los tres valores en una sola propiedad `border` donde no importa el orden.

```css
div {
    border: [color] [style] [width];
}

div {
    border-color: red;
    border-style: solid;
    border-width: 1px;
}
```

- [Ejemplo de bordes](https://codi.link/PGRpdiBjbGFzcz0ibm9uZSI+U2luIGJvcmRlPC9kaXY+DQo8ZGl2IGNsYXNzPSJkb3R0ZWQiPkNvbiBwdW50b3M8L2Rpdj4NCjxkaXYgY2xhc3M9ImRhc2hlZCI+Q29uIGd1aW9uZXM8L2Rpdj4NCjxkaXYgY2xhc3M9InNvbGlkIj5Db250aW51bzwvZGl2Pg0KPGRpdiBjbGFzcz0iZG91YmxlIj5kb2JsZSBjb250aW51bzwvZGl2Pg0KPGRpdiBjbGFzcz0iZ3Jvb3ZlIj5Db24gcmVjdWFkcm88L2Rpdj4NCg0KDQo=%7CZGl2ew0KICB3aWR0aDogMTIwcHg7DQogIGhlaWdodDogMTIwcHg7DQp9DQoNCi5ub25lew0KICAvKiBWYWxvciBwb3IgZGVmZWN0byBkZSBkaXYgKi8NCiAgYm9yZGVyOiAzcHggYmxhY2sgbm9uZTsNCn0NCg0KLmRvdHRlZHsNCiAgYm9yZGVyOiAzcHggYmxhY2sgZG90dGVkOw0KfQ0KDQouZGFzaGVkew0KICBib3JkZXI6IDNweCBibGFjayBkYXNoZWQ7DQp9DQoNCi5zb2xpZHsNCiAgYm9yZGVyOiAzcHggYmxhY2sgc29saWQ7DQp9DQoNCi5kb3VibGV7DQogIGJvcmRlcjogM3B4IGJsYWNrIGRvdWJsZTsNCn0NCg0KLmdyb292ZXsNCiAgYm9yZGVyOiA1cHggZ3JlZW55ZWxsb3cgZ3Jvb3ZlOw0KfQ0KDQoNCg0KLyogSWdub3JhIGVzdG9zIGVzdGlsb3MsIHBvciBhaG9yYSAqLw0KKiB7DQogIGZvbnQtc2l6ZTogMS4xcmVtOw0KICBtYXJnaW46IDA7DQp9DQoNCmJvZHl7DQogIGRpc3BsYXk6IGZsZXg7DQogIGZsZXgtd3JhcDogd3JhcDsNCiAgZ2FwOiAxLjVyZW07DQogIG1hcmdpbjogMjBweDsNCiAgZm9udC13ZWlnaHQ6IDgwMDsNCn0NCg0KDQoNCg==%7C)

También estableciendo de manera individual los valores de cada posición:

```css
div {
  border-top: 5px solid blue;
  border-bottom: 5px solid red;
  border-left: 5px solid black;
  border-right: 5px solid yellow;
}
```

### Qué es el espaciado interno del elemento HTML o padding

**El `padding` consiste en el espacio entre el borde y el contenido del elemento HTML**. Si imaginamos una caja, este valor sería el espacio entre la caja y lo que deseas guardar.

```css
div {
    padding: 100px;
}
```

- [Ejemplo de padding](https://codi.link/PGRpdj5Mb3JlbSBpcHN1bSBkb2xvciBzaXQgYW1ldCBjb25zZWN0ZXR1ciBhZGlwaXNpY2luZyBlbGl0aTwvZGl2Pg0KDQoNCg==%7CLyogUXVpdGEgbG9zIGNvbWVudGFyaW9zIHkgb2JzZXJ2YSBlbCBjb21wb3J0YW1pZW50byAqLw0KZGl2ew0KICB3aWR0aDogMTIwcHg7DQogIGhlaWdodDogMTIwcHg7DQogIGJhY2tncm91bmQtY29sb3I6IGdyZWVueWVsbG93Ow0KICBib3JkZXI6IHNvbGlkIDFweCBibGFjazsNCiAgLyogcGFkZGluZzogMzBweDsgKi8NCn0NCg0KDQoNCi8qIElnbm9yYSBlc3RvcyBlc3RpbG9zLCBwb3IgYWhvcmEgKi8NCiogew0KICBmb250LXNpemU6IDEuMXJlbTsNCiAgbWFyZ2luOiAwLjVyZW07DQp9DQo=%7C)

Puedes establecer el _padding_ en cada posición en una sola línea de las siguientes maneras:

- `padding: [arriba] [derecha] [abajo] [izquierda]`, siguiendo el sentido horario.
- `padding: [arriba] [derecha e izquierda] [abajo]`, siguiendo el eje principal.
- `padding: [arriba y abajo] [derecha e izquierda]`, siguiendo los ejes del elemento.

También estableciendo de manera individual los valores de cada posición:

```css
div {
    padding-top: 10px;
    padding-bottom: 15px;
    padding-left: 20px;
    padding-right: 10px;
}
```

### Qué es el espaciado externo del elemento HTML o margin

**El `margin` consiste en el espacio entre el borde y otro elemento HTML**. Si imaginamos una caja, es el espacio entre tu caja y otra caja.

```css
div {
    margin: 10px;
}
```

- [Ejemplo de margin](https://codi.link/PGRpdiBjbGFzcyA9ICJtYXJnaW4iPkxvcmVtIGlwc3VtIGRvbG9yIHNpdCBhbWV0IGNvbnNlY3RldHVyIGFkaXBpc2ljaW5nIGVsaXRpPC9kaXY+DQo8ZGl2PlNveSBvdHJvIGVsZW1lbnRvPC9kaXY+DQoNCg0K%7CLyogUXVpdGEgbG9zIGNvbWVudGFyaW9zIHkgb2JzZXJ2YSBlbCBjb21wb3J0YW1pZW50byAqLw0KZGl2ew0KICB3aWR0aDogMTIwcHg7DQogIGhlaWdodDogMTIwcHg7DQogIGJhY2tncm91bmQtY29sb3I6IGdyZWVueWVsbG93Ow0KICBib3JkZXI6IHNvbGlkIDFweCBibGFjazsNCn0NCg0KLm1hcmdpbiB7DQogIC8qIG1hcmdpbjogMjBweDsgKi8NCn0NCg0KDQoNCi8qIElnbm9yYSBlc3RvcyBlc3RpbG9zLCBwb3IgYWhvcmEgKi8NCiogew0KICBmb250LXNpemU6IDEuMXJlbTsNCiAgbWFyZ2luOiAwOw0KfQ0KDQpib2R5ew0KICBkaXNwbGF5OiBmbGV4Ow0KICBtYXJnaW46IDIwcHg7DQogIGZvbnQtd2VpZ2h0OiA4MDA7DQp9DQoNCg0KDQoNCg==%7C)

Puedes establecer el _margin_ en cada posición en una sola línea de las siguientes maneras:

- `margin: [arriba] [derecha] [abajo] [izquierda]`, siguiendo el sentido horario.
- `margin: [arriba] [abajo] [derecha e izquierda]`, siguiendo el eje principal.
- `margin: [arriba y abajo] [derecha e izquierda]`, siguiendo los ejes del elemento.

También estableciendo de manera individual los valores de cada posición:

```css
div {
    margin-top: 10px;
    margin-bottom: 15px;
    margin-left: 20px;
    margin-right: 10px;
}
```

### Qué son los valores por defecto

Por defecto, el navegador establece valores iniciales a algunas propiedades CSS, este es el caso de `margin` y `padding`. Una buena práctica es utilizar el selector universal para restablecer estos valores a `0`, para que no surjan errores inesperados.

```css
* {
    margin: 0;
    padding: 0;
}
```

### Qué es el tamaño total del elemento

El tamaño total del elemento está determinado por la suma de los valores de las propiedades `border` `padding` y `width`o `height`, dependiendo del eje. La propiedad `margin` no está incluida en este cálculo.

Por ejemplo, definimos los siguientes estilos:

```css
div{
  width: 150px;
  height: 150px;
  padding: 20px;
  border: 10px solid gray;
  margin: 30px;
}
```

- [Ejemplo de medidas totales](https://codi.link/PGRpdj5Mb3JlbSBpcHN1bSBkb2xvciBzaXQgYW1ldCBjb25zZWN0ZXR1ciBhZGlwaXNpY2luZyBlbGl0aTwvZGl2Pg0KDQoNCg==%7CKiB7DQogIG1hcmdpbjogMDsNCiAgcGFkZGluZzogMDsNCn0NCg0KZGl2ew0KICBiYWNrZ3JvdW5kLWNvbG9yOiBncmVlbnllbGxvdzsNCiAgd2lkdGg6IDE1MHB4Ow0KICBoZWlnaHQ6IDE1MHB4Ow0KICBwYWRkaW5nOiAyMHB4Ow0KICBib3JkZXI6IDEwcHggc29saWQgZ3JheTsNCiAgbWFyZ2luOiAzMHB4Ow0KfQ0KDQoNCg0KDQoNCg0KDQoNCg==%7C)

El tamaño total del elemento será de `210px` en ambos ejes, donde la suma fue: `150` (altura/anchura) + `20 x 2` (_padding_ ambos lados) + `10 x 2` (borde ambos lados). Si evaluamos este elemento en las herramientas del desarrollador mostrará su tamaño como `210x210`.

![Medidas totales de un elemento HTML](https://static.platzi.com/media/articlases/Images/frontend_developer22.png)

Aunque se conozca las medidas de los elementos de esta manera, no siempre existirá un control total. Por lo que podríamos establecer el **tamaño total del elemento** con `width` y `height`, y no solo del contenido, añadiendo la propiedad `box-sizing`.

### Propiedad _box-sizing_

**La propiedad `box-sizing` establece cómo se calculará el `width` y el `height` si incluyen bordes y espacios internos.** Como buena práctica, se lo coloca en el selector universal, para que todos los elementos sigan esta tendencia.

```css
* {
  box-sizing: border-box;
}
```

**Con el valor `border-box`, el tamaño total del elemento será igual al especificado en el `width` y `height`**, provocando que las medidas del contenido cambien con respecto a los bordes y espacios internos.

Por ejemplo, con los estilos que definimos anteriormente, establezcamos esta nueva propiedad.

- [Ejemplo de box-sizing](https://codi.link/PGRpdj5Mb3JlbSBpcHN1bSBkb2xvciBzaXQgYW1ldCBjb25zZWN0ZXR1ciBhZGlwaXNpY2luZyBlbGl0aTwvZGl2Pg0KDQoNCg==%7CLyogUXVpdGEgbG9zIGNvbWVudGFyaW9zIHkgb2JzZXJ2YSBsbyBxdWUgb2N1cnJlICovDQoqIHsNCiAgbWFyZ2luOiAwOw0KICBwYWRkaW5nOiAwOw0KICAvKiBib3gtc2l6aW5nOiBib3JkZXItYm94OyAqLw0KfQ0KDQpkaXZ7DQogIGJhY2tncm91bmQtY29sb3I6IGdyZWVueWVsbG93Ow0KICB3aWR0aDogMTUwcHg7DQogIGhlaWdodDogMTUwcHg7DQogIHBhZGRpbmc6IDIwcHg7DQogIGJvcmRlcjogMTBweCBzb2xpZCBncmF5Ow0KICBtYXJnaW46IDMwcHg7DQp9DQoNCg0KDQoNCg0K%7C)

El tamaño total del elemento será de `150px` en ambos ejes, donde se calcularon las medidas del contenido para que la suma total sea lo especificado en el `width` y `height`. Si evaluamos este elemento en las herramientas del desarrollador mostrará su tamaño total como `150x150` y el contenido como `90x90`.

![Propiedad box-sizing de CSS](https://static.platzi.com/media/articlases/Images/frontend_developer23.png)

##  Colapso de márgenes en CSS: Bloques, Flexbox y Grid
El colapso de márgenes sucede cuando **dos elementos bloque adyacentes tienen un determinado valor de `margin`**, entonces estos márgenes se solapan en un solo valor, el mayor de ambos.

![Colapso de márgenes](https://static.platzi.com/media/articlases/Images/frontend_developer25.png)

### Ejemplo de colapso de márgenes

Mira el siguiente código, cambia el valor de `display` a `inline-block` y observa el resultado.

- [Ejemplo de colapso de márgenes](https://codi.link/PGRpdj5Mb3JlbSBpcHN1bSBkb2xvciBzaXQgYW1ldCBjb25zZWN0ZXR1ciBhZGlwaXNpY2luZyBlbGl0aTwvZGl2Pg0KPGRpdj5Mb3JlbSBpcHN1bSBkb2xvciBzaXQgYW1ldCBjb25zZWN0ZXR1ciBhZGlwaXNpY2luZyBlbGl0aTwvZGl2Pg0KPGRpdj5Mb3JlbSBpcHN1bSBkb2xvciBzaXQgYW1ldCBjb25zZWN0ZXR1ciBhZGlwaXNpY2luZyBlbGl0aTwvZGl2Pg0KPGRpdj5Mb3JlbSBpcHN1bSBkb2xvciBzaXQgYW1ldCBjb25zZWN0ZXR1ciBhZGlwaXNpY2luZyBlbGl0aTwvZGl2Pg0KDQoNCg0K%7CKiB7DQogIG1hcmdpbjogMDsNCiAgcGFkZGluZzogMDsNCiAgYm94LXNpemluZzogYm9yZGVyLWJveDsNCn0NCg0KLyogUXVpdGEgbG9zIGNvbWVudGFyaW9zIHkgb2JzZXJ2YSBsbyBxdWUgb2N1cnJlICovDQpkaXZ7DQogIC8qIGRpc3BsYXk6IGlubGluZS1ibG9jazsgKi8NCiAgbWFyZ2luOiA0MHB4Ow0KICBiYWNrZ3JvdW5kLWNvbG9yOiBncmVlbnllbGxvdzsNCiAgd2lkdGg6IDgwJTsNCiAgaGVpZ2h0OiA1MHB4Ow0KICBwYWRkaW5nOiAxMHB4Ow0KfQ0KDQoNCg0KDQoNCg0K%7C)

![Explicación de colapso de márgenes](https://static.platzi.com/media/articlases/Images/frontend_developer24.png)

Como puedes observar, al cambiar el display este comportamiento desaparece. **Además, en [flexbox y grid](https://platzi.com/clases/2467-frontend-developer/40839-tipos-de-display-mas-usados-flexbox-y-css-grid/) no ocurre el colapso de márgenes.** Cuida los márgenes que colocas en los elementos de tipo bloque.

##  Tipos de posicionamiento en CSS: Relative, Absolute, Fixed y Sticky
El posicionamiento en CSS consiste en **cómo un elemento se situará, con respecto a su elemento padre y al flujo normal del documento**. El flujo normal del documento es el orden de los elementos establecidos en el HTML.

La posición del elemento se la define con la propiedad `position`, mediante los siguientes valores:

- `static`
- `relative`
- `absolute`
- `sticky`

![Tipos de posicionamiento en CSS](https://static.platzi.com/media/articlases/Images/frontend_developer26.png)

### Propiedades de posición

Además de la propiedad `position`, existen cuatro propiedades del elemento de acuerdo a su posición con respecto a su padre, estas son: `top` (arriba), `bottom` (debajo), `left` (izquierda) y `right` (derecha).

```css
div {
    top: 10px;
    bottom: 15px;
    left: 20px;
    right: 10px;
}
```

Estos valores estarán establecidos en el padre próximo que tenga la posición `relative`.

Si `top` y `bottom` están definidos, `top` gana. Si `left` y `right` están definidos, `left` gana (dependiendo el idioma configurado).

### Posición estática

La posición `static` es el valor por defecto de todo elemento HTML, consiste en **respetar el flujo normal del documento donde las propiedades de posición no pueden ser establecidas**.

- [Ejemplo position static](https://bit.ly/3KjpQuN)

### Posición relative

La posición `relative` consiste en **respetar el flujo normal del documento donde las propiedades de posición sí pueden ser establecidas**.

- [Ejemplo position relative](https://bit.ly/3KB4Akp)

### Posición absoluta

La posición `absolute` consiste en **quitar al elemento del flujo normal del documento donde las propiedades de posición sí pueden ser establecidas**.

En el siguiente ejemplo, observa que pasa con el primer elemento con respecto a los demás.

- [Ejemplo position absolute](https://bit.ly/3Cy16gc)

Habrás notado que el elemento "“2"” desaparece, pero en realidad lo que sucede es que **sitúa por detrás del elemento con posición absoluta que salió del flujo normal del documento**. Este comportamiento se debe al eje Z de la pantalla y al [contexto de apilamiento](https://platzi.com/clases/2467-frontend-developer/40842-z-index-y-el-contexto-de-apilamiento/).

### Elemento padre más próximo con posición relativa

El elemento con posición absoluta se desplazará arriba, abajo, izquierda o derecha con respecto al **elemento padre más próximo con posición relativa.**

**Si no existe un padre con posición relativa de un elemento con posición absoluta, este se desplazará con respecto al elemento raíz del documento.**

En el siguiente ejemplo, te encontrarás varios contenedores padres, incluso las etiquetas `<html>` y `<body>`. Sigue los pasos y observa el comportamiento. Ignora los estilos iniciales, simplemente sirven para establecer la estructura del ejercicio.

- [Ejemplo de position en diferentes contenedores padre](https://bit.ly/3ThZRrx)

Como pudiste observar, **en el elemento con posición absoluta, su desplazamiento se basa con relación al elemento padre más próximo con posición relativa.**

### Posición fija

La posición `fixed` consiste en **quitar al elemento del flujo normal del documento y fijarlo en un lugar; donde las propiedades de posición sí pueden ser establecidas**.

En el siguiente ejemplo, desplázate por el documento, observa el comportamiento antes y después de colocar la posición fija.

- [Ejemplo position fixed](https://tinyurl.com/2p94fbc7)

### Posición variable fija

La posición `sticky` consiste en **quitar al elemento del flujo normal del documento y fijarlo en un lugar mientras su contenedor sea visible; donde las propiedades de posición sí pueden ser establecidas**.

En el siguiente ejemplo, desplázate por el documento, observa el comportamiento antes y después de colocar la posición variable fija.

- [Ejemplo de position sticky](https://tinyurl.com/4cnxu8rx)

##  Z-Index y Contexto de Apilamiento en HTML/CSS
El contexto de apilamiento consiste en la **superposición de capas o elementos a lo largo del eje Z del navegador**. Esto es importante para evitar que un elemento esté ocultando a otro.

![Contexto de apilamiento - RetaxMaster](https://media1.giphy.com/media/1IvbqeWg7gLlRi2TAC/giphy.gif?cid=790b7611ba7156183cec0ef1ba9e76527d6adfbc2610e94c&rid=giphy.gif&ct=g)

### Qué son los planos y ejes

El navegador está constituido de tres planos y ejes: **el ancho o X; el alto o Y; y el de profundidad o Z**.

El eje X positivo está hacia la derecha; el eje Y positivo está hacia abajo; y el eje Z positivo está hacia el usuario.

![Planos y ejes del navegador](https://static.platzi.com/media/articlases/Images/animationland03.PNG)

Estos son muy importantes para mover los elementos del HTML desde un punto inicial hacia un punto final.

### Qué es la propiedad z-index

**El contexto de apilamiento se configura con la propiedad `z-index`.**

Por defecto, todos los elementos tienen un valor `auto`, es decir, el orden está definido por la estructura del HTML. Los primeros elementos estarán detrás y los últimos estarán de frente.

Si se establece un valor positivo, este elemento se sitúa por delante de los demás. Si se establece un valor negativo, se sitúa por detrás.

Si un elemento tiene un `z-index` mayor a otro, estará por delante. Sin embargo, **si un elemento que tiene un `z-index` menor a otros, sus hijos nunca estarán por encima, aunque su `z-index` sea mayor**.

![Ejemplo de contextos de apilamiento](https://static.platzi.com/media/user_upload/frontend_developer27-03c2127b-6cff-45e7-b502-9e05808ea394.jpg)

- [Ejemplo de contexto de apilamientos](https://bit.ly/3KkZisS)

Como puedes observar en la imagen, el elemento con la clase `yellow` tiene un `z-index` mayor a `red`, pero no está por encima, **porque su contexto de apilamiento está dentro del contexto de apilamiento del elemento `blue`**, así mismo, nunca estará por detrás de su elemento padre.

## Propiedades CSS más utilizadas en diseño web
Las propiedades CSS más usadas son las siguientes, separadas en secciones comunes, algunas ya las conocemos:

- Display
- Margin
- Padding
- Border
- Width
- Height
- Color
- Background

![Propiedades comunes de CSS](https://static.platzi.com/media/articlases/Images/frontend_developer28.png)

También, si deseas conocer todas las etiquetas existentes, puedes revisar el sitio web [CSS Reference](https://cssreference.io/).

### Propiedades de textos

Las propiedades para manipular los textos y tipografía son los siguientes:

- `font-size`: establece un tamaño de fuente.
- `font-weight`: establece el resaltado del texto, con valores de `100` a `900` en intervalos de `100`; donde `100` es delgada y `900` es negrita.
- `font-family`: establece el tipo de fuente.
- `text-align`: establece la posición del texto: `right`, `left`, `center` y `justify`.
- `color`: establece el color del texto.

### Bordes redondeados

La propiedad que establece bordes redondeados es: `border-radius`.

- [Ejemplo de bordes redondeados](https://bit.ly/3e4JQW0)

# Diseño responsivo

## Unidades de Medida en CSS: Absolutas y Relativas
**Las unidades de medida establecen una longitud para un determinado elemento o tipografía.** Existen dos tipos de medidas: absolutas y relativas.

![Medidas absolutas y relativas](https://static.platzi.com/media/articlases/Images/frontend_developer29.png)

### Qué son las medidas absolutas

**Las medidas absolutas son valores fijos, por lo que la medida no cambiará**. La unidad absoluta más utilizada son los píxeles `px`, las demás son muy poco utilizadas, pero es bueno que las conozcas.

| **Unidad** | **Nombre**            | **Equivalencia**       |
| ---------- | --------------------- | ---------------------- |
| px         | píxeles               | 1 px = 1/96 in         |
| cm         | centímetros           | 1 cm = 96/2.54 px      |
| mm         | milímetros            | 1 mm = 1/10 cm         |
| Q          | cuartos de milímetros | 1 Q = 1/4 mm           |
| in         | pulgadas              | 1 in = 2.54 cm = 96 px |
| pc         | picas                 | 1 pc = 1/6 in          |
| pt         | puntos                | 1 pt = 1/72 in         |

### Qué son las medidas relativas

**Las medidas relativas son valores variables, por lo que la medida depende de un valor externo.** Se debe tener en cuidado con estas porque un pequeño cambio puede desencadenar tamaños muy elevados.

| **Unidad** | **Depende de**                                        |
| ---------- | ----------------------------------------------------- |
| em         | el elemento que lo contiene                           |
| rem        | el elemento raíz                                      |
| vw         | 1% del ancho de la pantalla (view width)              |
| vh         | 1% de la altura de la pantalla (view height)          |
| vmin       | 1% de la dimensión más pequeña de la pantalla         |
| vman       | 1% de la dimensión más grande de la pantalla          |
| ch         | anchura del caracter “0” del elemento que lo contiene |
| lh         | altura de la línea del elemento que lo contiene       |

### Diferencia entre rem y em

La medida `em` depende del elemento que lo contiene, es decir, si un elemento tiene `font-size` de `20px`, el valor de `em` es igual a `20px`, el valor de `2em` será de `40px` y así sucesivamente.

La medida `rem` depende del elemento raíz, el valor del `font-size` del elemento raíz es de `16px`, por lo tanto, el valor de `2rem` es igual a `32px`, y así sucesivamente.

- [Ejemplo de medida em](https://bit.ly/3CzUNJb)

En las herramientas del desarrollador, te muestra el tamaño de la fuente _(font)_ en píxeles.

![Medida absoluta en las herramientas de desarrollador](https://static.platzi.com/media/articlases/Images/frontend_developer30.png)

- [Ejemplo de medida rem](https://bit.ly/3cqUJRq)

### Diferencia entre porcentajes y la anchura y altura de la pantalla

Los porcentajes representan el tamaño con respecto al total del **elemento padre**. Si el elemento padre tiene `20px`, entonces el `100%` será de `20px`.

Por otra parte, las medidas de anchura `vw` y altura `vh` representan el tamaño con respecto al total de la pantalla. Si el elemento tiene un tamaño de `100vw` será el 100 por ciento de la pantalla.

Si un elemento tiene todo el tamaño de la pantalla, entonces solamente en ese punto la medida `100%` será igual a `100vw` o `100vh`.

### Problema con las medidas de texto

Los navegadores tienen una opción para cambiar el tamaño del texto. Con medidas absolutas, el tamaño de la letra no cambiará, por lo que será un problema para el usuario.

Con medidas relativas, el tamaño cambiará con respecto a la fuente del elemento raíz. Por lo que estas son una buena opción para solucionar este problema de accesibilidad, en específico la medida `rem`.

Sin embargo, la medida `rem` equivale a `16px` y puede ser confuso mientras utilices valores altos. Por lo que vamos a cambiar el valor del elemento de la raíz para que la medida `rem` sea igual a `10px`.

En la etiqueta `<html>` cambia el valor de la propiedad `font-size` a `62.5%`, resultado de una regla de tres: si `16px` es igual al `100%` entonces cuál será el porcentaje para `10px`.

```css
html {
    font-size: 62.5%;
}
```

Con este cambio, la medida `rem` será igual a `10px`, ahora los puedes utilizar sin problema y tus textos cambiarán según las preferencias de usuario.

## Media Queries y Diseño Responsivo en CSS
El diseño responsivo _(Responsive Design)_ **consiste en un conjunto de herramientas para que tu sitio se vea bien en varias medidas de pantalla,** esto incluye imágenes, tipografía, internacionalización de la página y entre otros.

En la actualidad, la mayoría de sitios web son visitados desde un celular, por lo que asegurarse que nuestro sitio sea responsivo para cualquier dispositivo es fundamental para optimizar las ganancias.

### Qué son las media queries

Las _media queries_ son reglas CSS que establecen un comportamiento distinto o diferentes estilos en un cierto rango de la pantalla. Esto sirve para establecer el _layout_ del sitio web para diferentes tipos de pantalla: escritorio, tablets y celulares.

Estos son dos tipos de _media querie_ :

- `max-width / max-height`: establece un rango máximo para cierto comportamiento.
- `min-width / min-height`: establece un rango mínimo para cierto comportamiento.

Estos valores son parecidos a condicionales, mientras se cumpla la condición, aplica determinados estilos.

### Estructura de la media querie

La estructura de una _media querie_ consiste en empezar con `@media`, seguido del tipo de la _media querie_ estableciendo un rango, envolviendo las reglas CSS dentro de ese rango.

![Diseño responsivo](https://static.platzi.com/media/articlases/Images/frontend_developer31.png)

```css
@media (max-width:750px){
    div {
        color: red;
    }
    p {
        background-color: red;
    }
}
```

### Herramientas del desarrollador para media queries

Para observar que los cambios se estén aplicando correctamente, las herramientas de desarrollador serán de gran ayuda.

Abre las herramientas del navegador y da clic en la opción “Toggle device tool”, aquí podrás manipular la pantalla y observar en cuántos píxeles está ocurriendo determinados estilos.

![Herramientas de desarrollador para media queries](https://static.platzi.com/media/articlases/Images/frontend_developer32.png)

Utiliza el siguiente ejemplo para visualizar cómo cambian los estilos según la longitud de la pantalla. Puedes revisar la _media querie_ que está en el código. Aunque solo cambien el color de dos elementos, puede estar cualquier propiedad que desees, prueba con todo.

- [Ejemplo de media queries](https://bit.ly/3CEnBAf)

# Arquitecturas en CSS
## Arquitecturas CSS: Mejora de Legibilidad y Mantenibilidad del Código
**Las arquitecturas CSS consisten en manejar el código CSS con una serie de reglas y patrones para facilitar su lectura, mantenibilidad y escabilidad**.

El código que has manejado no se asemeja a la realidad, pues deberás manejar varios cientos o miles de líneas de código. Las arquitecturas CSS se encargan de manejar una norma en el código para que cualquiera pueda añadir o quitar funcionalidad sin mucho trabajo.

![Características de las arquitecturas de CSS](https://static.platzi.com/media/articlases/Images/frontend_developer33.png)

### Objetivos de las arquitecturas de CSS

Los objetivos de las arquitecturas de CSS son:

- **Ser predecible:** el código debe ser lo menos complejo posible.
- **Reutilizable:** el código debe ser lo menos redundante, para evitar problemas con la especificidad.
- **Mantenible:** el código debe ser lo más fácil de manejar para añadir o quitar estilos.
- **Escalable:** el código debe ser capaz de crecer.

### Buenas prácticas de las arquitecturas de CSS

Las buenas prácticas de las arquitecturas de CSS son:

- **Lineamientos y estándares:** definir normas en tu grupo de trabajo de cómo estará escrito el código.
- **Documentación:** establecer una breve explicación del código y de los lineamientos, esto sirve especialmente para nuevas personas se familiaricen con lo que deben hacer.
- **Componentes:** establecer de manera componetizada cada uno de los elementos de tu página, es decir, manejarlos por partes para después unirlos en un todo.

## Metodologías de CSS: OOCSS, VEM, SMACS y Atomic Design
**La arquitectura OOCSS _(Object Oriented CSS)_ consiste en separar la estructura principal y la piel o máscara**.

En otras palabras, consiste en tener objetos que son estructuras principales. Estos objetos estarán unidos en una máscara, donde esta será la que cambie pero **manteniendo la estructura intacta**.

![CSS Orientado a objetos](https://static.platzi.com/media/articlases/Images/frontend_developer34.png)

### Qué es BEM: bloque, elemento y modificador

**La arquitectura BEM _(Block-Element-Modifier)_ es una de las más utilizadas actualmente.** Consiste en manejar los elementos en clases definidas por bloques, elementos y modificadores.

- **Bloque:** es la estructura principal que es contenedora de varios elementos.
- **Elemento:** es el elemento HTML que hace referencia el contenedor.
- **Modificador:** es un estilo específico para el elemento. Por ejemplo, un botón que tenga un color diferente a los demás, esto tiene relación con la [especificidad](https://platzi.com/clases/2467-frontend-developer/40837-cascada-y-especificidad-en-css/).

![Bloque, elemento y modificador](https://static.platzi.com/media/articlases/Images/frontend_developer35.png)

Puedes revisar más sobre esta arquitectura en el siguiente artículo:

- [Guía de BEM para CSS | Cohete Falcon 9 de SpaceX](https://platzi.com/blog/bem/)

### Qué es la arquitectura escalable y modular de CSS

**La arquitectura SMACSS _(Scalable and Modular Architecture for CSS)_ indica el orden de componentes que estarán ubicados en carpetas**. La unión de estos componentes dará como resultado tu página web con estilos.

- **Base:** elementos base, como botones, títulos, enlaces.
- **Layout:** estructura de la página, relacionado con el _[Responsive Design](https://platzi.com/clases/2467-frontend-developer/40845-responsive-design/)_.
- **Módulos:** elementos que contienen a los elementos base.
- **Estado:** estilos relacionados con el comportamiento de elemento, relacionado con las [pseudoclases y pseudoelementos](https://platzi.com/clases/2467-frontend-developer/40836-tipos-de-selectores-pseudoclases-y-pseudoelementos/).
- **Temas:** conjunto de estilos que definen tu página web.

![Arquitectura escalable y modular de CSS](https://static.platzi.com/media/articlases/Images/frontend_developer36.png)

### Qué es el triángulo invertido de CSS

La arquitectura ITCSS _(Inverted Triangle CSS)_ consiste en **separar los archivos del proyecto**; mediante ajustes, herramientas, elementos, entre otros. Todo esto para **manejar los detalles de especificidad, claridad y magnitud**.

![Triángulo invertido de CSS](https://static.platzi.com/media/articlases/Images/frontend_developer37.png)

### Qué es el diseño atómico

**La arquitectura _Atomic Design_ también es una de las más utilizadas actualmente.** Consiste en manejar los elementos como una estructura mínima, a partir de la unión de varias de estas, dará como resultado los estilos de la página web. Se basa en la estructura mínima de la materia, los átomos.

- **Átomos:** estructura mínima; como botones, enlaces, títulos, entre otros.
- **Moléculas:** unión de átomos.
- **Organismos:** unión de moléculas.
- **Plantillas:** unión de organismos.
- **Páginas:** unión de plantillas.

![Diseño atómico](https://static.platzi.com/media/articlases/Images/frontend_developer38.png)

