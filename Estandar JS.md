Estandar de codificación para JavaScript
================
Lo siguiente sera el estandar que el equipo usara para JavaScript.

Documento JS
================
Para utilizar JS se deberá crear un archivo con extensión .js que se vinculara con los distintos archivos HTML que lo necesiten, se deberá crear un archivo distinto para cada funcionalidad que se quiera implementar, intentando seguir el lema de “alta cohesión, bajo acoplamiento”.

Se deberá evitar poner código JS directamente dentro de un documento HTML, a menos que el código que se necesite sea pequeño y solo se vaya a utilizar en ese único documento HTML, si el código es pequeño, pero se utilizara en mas de un archivo HTML entonces ese código se deberá poner en un archivo .js.

Documentación automática
================
Para la documentación se utilizará la herramienta “ESDoc”, la cual permite generar documentación automática en formato HTML, la herramienta puede encontrarse en el siguiente enlace:
https://esdoc.org/manual/feature.html#documentation-coverage

Variables
================
Las variables deberán tener nombres representativos, evitando nombres como “x”, se deberá utilizar minúsculas a menos que la variable tenga mas de una palabra, en ese caso la segunda palabra iniciará en mayúscula, además las variables preferiblemente deberán ser declaradas utilizando “block scoping”, empleando “let” en lugar de “var”.
```javascript
let opcionEscogida = 2;
```
Las variables siempre deberán inicializarse y cuando se declare varias variables idealmente debe hacerse de la siguiente manera:
```javascript
let opcionEscogida = 2,
    salario = 0,
    numero = 3;
```
Para el nombramiento de constantes se deberá usar la palabra reservada “const”, los nombres de las constantes deberán estar en mayúsculas y si son de mas de una palabra deberán estar separadas por guiones bajos.
```javascript
const MARGIN_TOP = 2;
```
Uso de llaves
================
Al momento de utilizar if, for, while, funciones, etc. Se deberá de utilizar las llaves de la siguiente forma:
```javascript
  for(let i = 0; i < 10; i++) {
  }
```
La llave de apertura deberá estar en la misma línea que la función y separada por un espacio.

Comentarios
================
(Para los comentarios que no sean de documentación automática) Se deberá evitar el uso de comentarios innecesarios para cosas que sean muy obvias, como por ejemplo “lee una variable”, los comentarios deberán utilizarse cuando el programa no sea tan obvio o cuando haya posibles excepciones o errores. 

En la parte superior del archivo JS deberá estar la siguiente estructura de documentación la cual deberá ser llenada de ser posible.
```javascript
  /*
    Entradas: (si aplica)
    Salidas: (si aplica)
    Procedimientos:
  */
```
Para las pruebas se deberá tener comentarios hasta abajo del documento con la siguiente estructura:
```javascript
  /*
    ----------- Pruebas ------------
    Funcion1
    Entradas:
    Salidas:
    Observaciones:

    Funcion2
    Entradas:
    Salidas:
    Observaciones:

  */
```

Indentación
================
El código deberá estar indentado con dos espacios a la izquierda.
```javascript
  class App {
    constructor() {
      this.doSomething();
    }

    doSomething() {
      console.log('Oh boy a class!');
    }
  }
```

Modularización
================
Todo el código deberá de modularizarse lo máximo posible, por medio de funciones.

Las funciones en la medida de lo posible deberán nombrarse haciendo uso de “get” y “set”, si el nombre de una función tiene más de una palabra entonces la primera letra de la segunda palabra deberá iniciar en mayúscula, por ejemplo, una función que lea el nombre del usuario idealmente deberá llamarse “setNombre()”.

Una función que únicamente devuelva un valor, sin solicitar ninguna entrada como por ejemplo una función que devuelva el salario de una persona deberá llamarse idealmente: “getSalario()”
```javascript
    function setNombre() {
      let a = prompt("Ingresa tu nombre: ");
      return a;
    }
    function getSalario() {
      return salario;
    }
```
