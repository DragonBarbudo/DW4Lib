# DW4 Lib

Librerías de DW4 para uso en proyectos externos.

## dw4.css

Actualmente únicamente la librería CSS ha sido liberada con un peso de 33kb.

DW4.css utiliza FLEXBOX para generar una rejilla de 12 columnas. Esta basada en [Flexbox Grid](http://flexboxgrid.com/) y compilada con LESS.

Incluye 3 modos responsivos: "Desktop", "Tablet" y "Móvil".

| Modo    | Responsive          |
| ------- | ------------------- |
| Desktop | 1200px hacia arriba |
| Tablet  | 1199px a 720px      |
| Móvil   | 719px hacia abajo   |



Para utilizarla se puede descargar el archivo dw4.css o desde RawGit:

>  https://cdn.rawgit.com/DragonBarbudo/DW4Lib/master/dw4.css

Uso:

> <link rel="stylesheet" href=" https://cdn.rawgit.com/DragonBarbudo/DW4Lib/master/dw4.css" />



### Contenedores

Para que cualquier columna pueda trabajar necesita estar rodeado de un **.container**

El **contenedor** trabaja en las medidas responsive, en estado DESKTOP mide 1200px, en TABLET mide 720px y en MOBILE su ancho es del 100%.

Si se desea tener un contenedor que en todo momento tenga un ancho de 100% se puede utilizar la clase **.fluid** en conjunto con **.container**.



> <div class="container fluid"></div>