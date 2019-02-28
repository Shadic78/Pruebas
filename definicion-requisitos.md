## Terminos

**Encargado**: usuario o usuarios encargados de un centro de acopio.

**Donador**: usuario no encargado de un centro de acopio.

**BDI**: base de datos interna; una base de datos privada que los actores del sistema (donadores y encargados) no pueden acceder.

**BDP**: base de datos personal; una base de datos que puede ser modificada por el encargado de esta.

**Plantilla**: Estructura predefinida

## Requisitos funcionales

- *RF001*:El sistema deberá registrar y almacenar en la BDI un correo electrónico (ya sea del encargado o uno especial creado por la organización para el uso del sistema), la contraseña que usará para acceder a la cuenta (que será confirmada reescribiéndola), la ubicación del centro de acopio (calle, cruzamientos, colonia, numero y código postal), el nombre del centro de acopio, del centro de acopio.

- *RF002*: El sistema deberá verificar el correo electrónico proporcionado.

- *RF003*: El sistema deberá permitir al encargado acceder al mismo usando el correo electrónico y la contraseña proporcionada.

- *RF004*: El sistema deberá aportarle una herramienta de edición de bases de datos al encargado para que pueda modificar una BDP.

- *RF005*: El sistema deberá proporcionarle herramientas al encargado para la edición del perfil - -del centro de acopio para ingresar la descripción y el objetivo de este al igual que su horario de atención.

- *RF006*: El sistema deberá proporcionar otra área en donde un donador podrá ver la información de los centros de acopio.

- *RF007*: El sistema pedirá al donador un código postal para saber su ubicación aproximada para posteriormente mostrarlo en un mapa.

- *RF008*: El donador podrá navegar por el mapa para buscar centros de acopio cercanos al código postal proporcionado.

- *RF009*: El donador podrá seleccionar un centro de acopio y al hacerlo le mostrará la información de este.

## Requisitos no funcionales

- *RNF001*: La verificación del correo electrónico no debe durar más de 5 minutos.

- *RNF002*: La BDP no deberá pesar mas de 500mb.

- *RNF003*: La BDP tendrá una plantilla la cual no podrá ser modificada por los actores.

- *RNF004*: La interfaz deberá ser minimalista.

- *RNF005*: El sistema debe ser accesible únicamente por un navegador de internet.

## Pruebas unitarias

Para elaborar pruebas unitarias fácilmente con el lenguaje de programación JavaScript, se usará unit.js el cual es una librería de aserciones las cuales corren en node.js y en el buscador web.

Por ejemplo:
```JavaScript
	var test = require('unit.js');

	describe('Learning by the example', function(){

	  it('example variable', function(){

	    // just for example of tested value
	    var example = 'hello world';
	    test
	      .string(example)
	        .startsWith('hello')
	        .match(/[a-z]/)

	      .given(example = 'you are welcome')
	        .string(example)
	          .endsWith('welcome')
	          .contains('you')

	      .when('"example" becomes an object', function(){

	        example = {
	          message: 'hello world',
	          name: 'Nico',
	          job: 'developper',
	          from: 'France'
	        };
	      })

	      .then('test the "example" object', function(){

	        test
	          .object(example)
	            .hasValue('developper')
	            .hasProperty('name')
	            .hasProperty('from', 'France')
	            .contains({message: 'hello world'})
	        ;
	      })

	      .if(example = 'bad value')
	        .error(function(){
	          example.badMethod();
	        })
	    ;
	
	  });

	  it('other test case', function(){
	    // other tests ...
	  });

	});
```
