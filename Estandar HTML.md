**Estándares de codificación**

**Estándar de codificación para HTML**

Lo siguiente serán las reglas que el equipo deberá seguir al momento de crear
código HTML.

Generar la plantilla base
=========================

Todo documento HTML comenzará con una plantilla base, la cual será generada
automáticamente utilizando el “package” **emmet** en el editor de texto
**atom**.

Dicha platilla se generará creando un nuevo documento HTML y escribiendo:

-   html:5

Posterior a escribir lo anterior se presionará la tecla TAB y se generara la
plantilla, la cual tiene los elementos listados a continuación.

Elementos de la plantilla
=========================

Para empezar, todos los archivos HTML deberán comenzar con la siguiente
etiqueta:
```html
<!DOCTYPE HTML>
```

Dentro del header la primera etiqueta que deberá incluirse será:

```html

<meta charset="utf-8" />

```

Seguido de las siguientes etiquetas:
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
```
```html
<meta http-equiv="X-UA-Compatible" content="ie=edge"/>
```

Etiquetas
=========

Todas las etiquetas HTML deberán estar escritas en minúsculas.
```html
<!-- Correcto -->

<span></span>

<!-- Incorrecto -->

<SPAN\></SPAN>
```
Todas las etiquetas deberán tener su etiqueta de cierre correspondiente.
```html
<!-- Correcto -->

<h1>Titulo 1</h1>

<p>Párrafo 1</p>

<!-- Incorrecto -->

<h1>Titulo 1

<p>Párrafo 1
  ```
Las etiquetas que no lleven etiqueta de cierre deberán llevar una “/” al final.
```html
<!-- Correcto -->

<br />

<hr />

<img src="john.jpg" alt="John Doe" width="200" height="100" />

\<input name="age" type="text" size="3" />

<!-- Incorrecto -->

<br>

<hr>

<img src="john.jpg" alt="John Doe" width="200" height="100">

<input name="age" type="text" size="3">
```
Atributos
=========

Los atributos siempre deberán ir escritos en minúsculas.
```html
<!-- Correcto -->

<input name="name" type="text" />

<!-- Incorrecto -->

<input NAME="name" TYPE="text" />
```
Los valores de los atributos de las etiquetas siempre deberán ir entre comillas
(“ ”).
```html
<!-- Correcto -->

<input name="age" type="text" size="3" />

<!-- Incorrecto -->

<input name=age type=text size=3 />
```
Indentación
===========

Cuando un elemento contenga a uno o más elementos, dichos elementos deberán
indentarse apropiadamente utilizando 2 espacios, ejemplo:
```html
<div class="container">

<header class="header">

<h1>Site Name<span></span\></h1>

</header>

<hr>

<nav class="navigation">

<ul>

<li><a href="#">Link</a></li>

<li><a href="#">Link</a></li>

<li><a href="#">Link</a></li>

<li><a href="#">Link</a></li>

<li><a href="#">Link</a></li>

</ul>

</nav>

</div>
```
Comentarios
===========

Deberán ponerse comentarios abajo de la etiqueta de cierre de los elementos HTML
indicando que elemento acaba de terminar, de la siguiente forma:
```html
<ol class="accessibility-nav">

<li><a href="#navigation">Skip to navigation</a></li>

<li><a href="#content">Skip to content</a></li>

<li><a href="#sidebar">Skip to sidebar</a></li>

</ol>

<!-- / Fin barra de navegacion -->

<p>

<a href="#" title="Go to homepage"><em>Home</em></a>

</p>

<!-- / Fin parrafo -->
```
Imágenes
========

Las imágenes deberán estar dentro de una carpeta llamada img y al llamarlas con
la etiqueta \<img /\> debera colocarse la extensión de la imagen. (jpg, png,
etc.).

\<img src="img/imagen1.png" /\>

Las imágenes deberán tener el atributo “alt” especificando que imagen es.

\<img src="img/logo.png" alt="Logo de la empresa" /\>

Formularios
===========

Las cajas de texto deberán llevar el atributo “placeholder” indicando que se
debe ingresar.

\<input type="text" placeholder="Numero de celular" /\>

Las cajas de texto deberán tener un id y name iguales, el cual deberá ser
representativo.

\<input type="text" placeholder="Numero de celular" id="numCelular"
name="numCelular" /\>

Los labels deberán incluir el atributo “for” indicando el id del input al que se
refieren.

\<label for="numCelular" \>Ingresa tu número de celular: \</label\>

\<input type="text" placeholder="Numero de celular" id="numCelular"
name="numCelular" /\>

Titulos
=======

Se debera utilizar las etiquetas h1 – h6 para indicar los títulos que se
necesiten.

\<h1\>Titulo\</h1\>
