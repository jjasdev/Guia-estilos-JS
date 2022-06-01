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
|     |- js/				/
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
