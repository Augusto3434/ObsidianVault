##🎯 Objetivo
Aprender a transformar un diseño gráfico en una interfaz web funcional utilizando HTML y CSS, siguiendo buenas prácticas y aplicando maquetación responsiva.

📌 Conceptos clave

 ✅ Buenas prácticas
- No son reglas absolutas, dependen del contexto.
- Mejoran la legibilidad, mantenimiento y escalabilidad del código.
- Es vital cuestionarlas y adaptarlas según la situación específica del proyecto.

🧱 Sistema de diseño
🎨 Variables en CSS
- Se declaran con `--nombre-variable` dentro del selector `:root`.
- Permiten mantener coherencia en colores, tamaños, fuentes, etc.

🔤 Fuentes
- Se obtienen de Google Fonts.
- Se incluyen con `<link>` en el `<head>` del HTML.

📁 Organización de recursos
- Carpeta para íconos, logos, imágenes, etc.
- Estructura clara de carpetas y archivos para escalabilidad.

📱 Maquetación responsiva: Pantallas de autenticación

🏗️ Estructura base
- HTML semántico con `<form>`, `<input>`, `<button>`.
- Diseño adaptable a móvil y escritorio.
🎯 Recomendaciones
- Usa `display: flex` o `grid` para alineación.
- Aplica `media queries` para adaptar la interfaz.
- Nombres de clases intuitivos y reutilizables.
- Mantén el diseño simple y centrado en la usabilidad.

📐 Orden de estilos sugerido
1. Posicionamiento  
2. Modelo de caja  
3. Tipografía  
4. Estilos visuales  
5. Otros  
6. Responsive Design (`media queries`)
🧪 Pruebas constantes
- Verifica en múltiples resoluciones.
- Itera frecuentemente.

🖥️ Maquetación responsiva: Vistas principales
🏠 Página de inicio
- Cards de productos con imagen, nombre, precio y botón de compra.
🖼️ Imágenes en HTML
- Etiqueta `<img src="..." alt="...">`
- Usa `alt` para accesibilidad y SEO.
- Apoya con `<figure>` y `<picture>` para semántica y adaptabilidad.
🧩 CSS Grid
- Clase `.cards-container { display: grid; }`
- Uso de `grid-template-columns`, `repeat()`, `auto-fill`, `gap`, `place-content`.
📂 Menú desplegable (mobile)
- Dos estados: activo e inactivo.
- Estructura basada en listas (`<ul><li>`).
- Navegación construida con `<nav>`.
🧾 Orden de compra
- Lista dinámica de productos.
- Estilo adaptable a diferentes cantidades.
📸 Propiedad `object-fit`
- Ajusta cómo la imagen encaja en su contenedor.
- Valores comunes:
  - `contain`, `cover`, `fill`, `none`, `scale-down`

🧭 Etiquetas semánticas útiles
- `<nav>` para navegación.
- `<aside>` para contenido complementario.
- `Lorem Ipsum` como texto de prueba para validar diseños.
🧠 Conclusión
Este curso proporciona una base sólida para desarrollar interfaces web responsivas utilizando HTML y CSS. A través del uso de sistemas de diseño, maquetación semántica y enfoque mobile-first, te prepara para proyectos más complejos y el uso de frameworks como React.

🧭 Recomendaciones finales
- Aplica las buenas prácticas con criterio y entendiendo el contexto.
- Mejora continua mediante la prueba y la iteración.