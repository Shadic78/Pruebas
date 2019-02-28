Estandar de codificación para CSS
====================

Documento CSS
====================
Todos los estilos CSS que se utilicen deberán estar en un archivo “style.css”, deberá evitarse colocar estilos dentro de los documentos HTML.
Nombres
Las clases e id deberán ser representativas y si tienen mas de una palabra deberán separarse con “- “, todo deberá estar en minúsculas.
```css
/* Correcto */
.contenedor-articulos

/* Incorrecto */
.contenedor_articulos
.ContenedorArticulos
```
Valores
Siempre deberá declararse mas de una fuente en caso de que el navegador no pueda mostrar la primera opción, además cada valor deberá estar separado por un espacio después de la coma.
```css
/* Correcto */
font-family: Arial, Helvetica, sans-serif;

/* Incorrecto */
font-family: Arial;
```
Si se usa cero como valor, no deberá incluirse la medida que se está usando.
```css
/* Correcto */
.nav a {
  padding: 5px 0 5px 2px;
}

/* Incorrecto */
.nav a {
  padding: 5px 0px 5px 2px;
}
```
Selectores
Los selectores deberán estar separados por un espacio entre si y entre la llave de apertura, además el siguiente selector deberá estar separado por una línea del anterior.
```css
.nav li {
}

.nav a {
}
```

Se deberá evitar el uso de expresiones grandes como la siguiente:
```css
/* Incorrecto */
.my-inbox .flyout-content .inner .message .inbox li div.take-action .actions ul li a {
}
```
Para evitar lo anterior se deberá tener el cuidado de estructurar de la manera mas optima posible el código HTML.

Indentación
Las propiedades deberán estar indentadas con dos espacios y solo deberá haber una propiedad por línea.
```css
.titulo-header span {
  position: absolute;
  top: 0;
  left: 0;
}
```
Comentarios
Deberá usarse el siguiente tipo de comentario para separar las secciones principales.
```css
/* ==========================================================================
   Estilos del header
   ========================================================================== */
```
Deberá tener una línea vacía antes y después, se utilizará para las secciones principales como puede ser el header, la barra de navegación, etc.
Se utilizará el siguiente tipo de comentario para separar subsecciones, como por ejemplo dentro de un contenedor se tiene otro contenedor donde se muestran artículos y hay otro contenedor con una barra de contenidos.
```css
/* Estilos de los artículos
   ========================================================================== */
```
Deberá tener una línea en blanco antes y después.
Si se necesita poner otros comentarios deberán ser de una línea, sin espaciado antes o después.
```css
/* Comentario */
```
