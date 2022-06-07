# Guía de estilos JS

Esta guía servirá de manual para usar siempre las mismas convenciones de codificación en los proyectos de Javascript, haciendo uso de las mejores prácticas para escribir código limpio y comprensible. 

## ¿Qué es?

Esta guía no son reglas estrictas para escribir código JavaScript válido, sino sugerencias para mantener un estilo consistente y legible en nuestro código. Esto es especialmente interesante para JavaScript, ya que es un lenguaje bastante flexible y permisivo que puede adoptar una gran variedad de estilos.

Estas reglas versarán sobre la denominación y declaración de variables y funciones, sobre el uso de espacios en blanco y la sangría o sobre la programación de buenas prácticas y patrones de diseño.


## Principios

-	Mantener un **código limpio y legible**, y poder reusarlo lo máximo posible
-	Implementar un código que luzca como si lo hubiera escrito una **única persona**
-	Codificar para mayor **escalabilidad, mantenibilidad y visibilidad**

## Arquitectura

La arquitectura usada para los proyectos sigue la estructura de carpetas estándar que la comunidad de JavaScript sigue por convención para diferenciar los archivos de desarrollo y los de producción. A continuación se muestra la estructura jerárquica:


```
guia-estilos
|
|- dist/			
|  |- index.html   
|  |      
|  |- assets/				
|     |- css/				
|     |  |- style.min.css			
|     |
|     |- images/			
|     |  |- background-header.webp	
|     |
|     |- js/				
|        |- main.min.js
|
|- src/ 				
|  |- assets/				
|     |- css/				
|     |  |- style.css
|     |  |- style.css.map
|     |
|     |- images/			
|     |  |- background-header.jpg
|     |
|     |- js/			
|     |  |- main.js
|     |  |- imagemin.js
|     |  
|     |- scss/
 
```

-	`dist`  Este directorio contiene la versión minificada del código fuente. Los documentos alojados en ella se usan en la aplicación en el modo de **producción**. 
-	`assets`  Los assets web son las hojas de estilo CSS, los archivos JavaScript y las imágenes que se utilizan en la interfaz de la aplicación.
-	`css`  Contiene las hojas de estilo usadas para dar formato al contenido y presentar la aplicación con un diseño personalizado.
-	`images`  En este directorio se alojarán todas las imágenes usadas en el proyecto.
-	`js`  Contiene los scripts implementados para agregar funcionalidad interactiva. 
-	`src`  Este directorio contiene el código fuente en bruto. Los documentos alojados en ella son las fuentes puras usadas en el modo de **desarrollo**.
-	`scss`  Este directorio contiene el código fuente de todos los estilos de aplicación agrupados en *partials*, para que posteriormente sean mapeados y procesados a una única hoja de estilo interpretada por los navegadores.

## Reglas generales

-	El estilo de escritura para funciones, objetos e instancias es **Camel Case** (*Ejemplo: `let sumaNumeros = …`*).
-	El estilo de escritura para constructores o clases es Pascal Case (*Ejemplo: `class User`*). 
-	Todos los nombres comienzan con una letra. Evita nombres de una sola letra. Se debe ser descriptivo con los nombres.
-	Los nombres de las constantes serán en mayúsculas y separadas por un guión bajo (*Ejemplo:  `CONSTANT_CASE`* ).
-	Se hará siempre uso del modo estricto  `"use strict"`; .
-	El código Javascript de la aplicación viene documentado con la herramienta **JSDoc**.
-	Para validar el código usaremos la herramienta **JSHint**.
-	Las variables se declararán con  `const` o `let`. Se hará uso de `const` por defecto, a menos que la variable vaya a ser reasignada. La palabra clave  var  no debe usarse.
-	Con ES6, el lenguaje tiene ahora tres tipos diferentes de iteración `for`. Pueden usarse todas, aunque el tipo `for-of` debe ser el preferente cuando sea posible.

## Sintaxis

-	Cada sentencia debe terminar con un punto y coma.
-	Debido a la simplicidad del código, para este proyecto no se usarán los módulos ES6.
-	El alineamiento horizontal está desaconsejado. (*La alineación horizontal es la práctica de usar un número variable de espacios adicionales en el código, para que ciertos elementos aparezcan justo debajo de otros elementos de las líneas anteriores*).
-	Se priorizan las funciones flecha sobre la palabra clave `function`, especialmente en funciones anidadas.
-	Evitar el uso de funciones anónimas.
-	Se usarán plantillas de strings (delimitadas por `) en lugar de concatenaciones complejas de strings, especialmente si están involucrados varios literales. 
-	Cada declaración de variable local declara una sola variable. Se asignarán las variables en una nueva línea, no separadas por comas.
-	Se priorizará el uso de comillas simples, en lugar de comillas dobles.
-	Uso de la sintaxis literal para la creación de objetos y arreglos:
```javascript
 const objeto = {}; 
 const arreglo = []; 
 ```
-	Cuando se acceda a las propiedades se usará la notación de punto. 
-	Se usará === y !== en vez de == y != respectivamente.
-	Se usarán llaves en todos los bloques de múltiples líneas.
-	En los comentarios de múltiples líneas se usará /** ... */. 
-	En los comentarios de una sola línea se usará //.
-	1 tabulación para la identación.
-	1 espacio antes de la llave de apertura.
-	1 espacio antes del paréntesis de apertura en las sentencias de control (`if, while…`).
-	0 espacios antes de la lista de argumentos en las invocaciones y declaraciones de funciones.
-	Se separarán los operadores con espacios.
-	1 línea en blanco al final del archivo.
-	1 línea en blanco luego de los bloques y antes de la siguiente sentencia.

