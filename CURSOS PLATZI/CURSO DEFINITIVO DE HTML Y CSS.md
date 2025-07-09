## 🧱 Fundamentos del Desarrollo Web

- **[[CURSO TEORICO FRONTEND|HTML]]**: Estructura del contenido.
- **[[CURSO TEORICO FRONTEND|CSS]]**: Estilo y presentación visual.
- **JavaScript**: Interactividad y lógica en el navegador.

### Analogía:
- HTML → Esqueleto
- CSS → Apariencia/Piel
- JavaScript → Movimiento/Músculos

---

## 🖥️ Frontend vs Backend

- **Frontend**: Visual e interacción del usuario (HTML, CSS, JS).
- **Backend**: Lógica del servidor (Node.js, Python, PHP, etc.).
- **Full Stack**: Maneja ambas áreas.

### Tecnologías Full Stack comunes:
- LAMP (Linux, Apache, MySQL, PHP)
- MERN (MongoDB, Express, React, Node.js)
- Django, Laravel, Rails, Spring

---

## 🧰 Herramientas Frontend

- **Documentación oficial**:  
  - [HTML](https://devdocs.io/html/)  
  - [CSS](https://devdocs.io/css/)  
  - [JavaScript](https://devdocs.io/javascript/)  

- **Frameworks CSS**:  
  - [Bootstrap](https://getbootstrap.com/)  
  - [Foundation](https://get.foundation/)  
  - [Materialize](https://materializecss.com/)  

- **Frameworks JS**:  
  - [React](https://es.reactjs.org/)  
  - [Angular](https://angular.io/)  
  - [Vue](https://vuejs.org/)  

- **Preprocesadores CSS**:  
  - [SASS](https://sass-lang.com/)  
  - [Stylus](https://stylus-lang.com/)  

- **Compiladores/Bundlers JS**:  
  - [Babel](https://babeljs.io/)  
  - [Webpack](https://webpack.js.org/)  

---

## 🌐 HTML

### [[CURSO DE FRONTEND DEVELOPER|Estructura]]: ^estructura-html


```html
<!DOCTYPE html>
<html>
  <head>...</head>
  <body>
    <header>...</header>
    <main>...</main>
    <footer>...</footer>
  </body>
</html>
Etiquetas comunes:
h1–h6: Títulos

p: Párrafos

a: Enlaces 

img: Imágenes

ul, ol, li: Listas

div: División genérica

section, article, aside, nav, figure, figcaption

Formularios:
<form method="" action="">

Inputs: text, email, date, time, number

Atributos útiles: placeholder, required

Selectores: select, datalist, option

🖼️ Imágenes Web
Tipos:
Lossless: PNG, SVG, GIF

Lossy: JPG, WebP

Optimización:
Peso ideal: ≤ 70KB

Herramientas: TinyPNG, Verifix

Etiquetas:
<img src="" alt="">

<figure> + <figcaption> para contexto semántico

🎨 CSS
Integración con HTML:
Externo (recomendado):

html
Copiar
Editar
<link rel="stylesheet" href="styles.css">
Interno:

html
Copiar
Editar
<style> h1 { color: red; } </style>
En línea (evitar):

html
Copiar
Editar
<p style="color: red;">Hola</p>
Selectores:
Elemento: p {}

Clase: .titulo {}

ID: #principal {}

📦 Modelo de Caja (Box Model)
content → padding → border → margin

Uso recomendado:

css
Copiar
Editar
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
📏 Unidades en CSS
Absolutas: px, cm, in

Relativas: %, em, rem, vw, vh

css
Copiar
Editar
html { font-size: 62.5%; } /* 1rem = 10px */
⚙️ Posicionamiento
static (por defecto)

relative

absolute

fixed

sticky

🧱 Display
block: Ocupa todo el ancho disponible

inline: Solo el espacio del contenido

inline-block: Combinación útil de ambos

none: Oculta elementos

📐 Flexbox
css
Copiar
Editar
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
}
Direcciones: row, column

Alineaciones: center, space-between, flex-end

👁️ Herencia y Especificidad
Herencia automática: color, font-size

No heredan: margin, padding, width

Especificidad:

!important > Inline > ID > Clase > Elemento

🧱 Metodología BEM
Bloque: .btn

Elemento: .btn__icon

Modificador: .btn--active

🔗 Combinadores en CSS
Descendiente: div p

Hijo directo: div > p

Hermano adyacente: h1 + p

Hermano general: h1 ~ p

🎯 Buenas Prácticas
Evitar estilos en línea

Usar rem en lugar de px para consistencia

Reiniciar estilos del navegador con *

Optimizar imágenes antes de subirlas

Nombrar clases con lógica clara (ej. BEM)