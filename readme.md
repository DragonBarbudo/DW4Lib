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

```html
<link rel="stylesheet" href=" https://cdn.rawgit.com/DragonBarbudo/DW4Lib/master/dw4.css" />
```



### Contenedores

Para que cualquier columna pueda trabajar necesita estar rodeado de un **.container**

El **contenedor** trabaja en las medidas responsive, en estado DESKTOP mide 1200px, en TABLET mide 720px y en MOBILE su ancho es del 100%.

```html
<div class="container"></div>
```



Si se desea tener un contenedor que en todo momento tenga un ancho de 100% se puede utilizar la clase **.fluid** en conjunto con **.container**.

```html
<div class="container fluid"></div>
```

> La clase **.fluid** se puede utilizar con cualquier elemento que se quiera tenga "width: 100%"



### Columnas

Se trabaja con una rejilla de 12 columnas. Cada elemento puede tener diferentes columnas dependiendo del estado responsivo.

La columna base para Desktop esta conformada por la clase **".c"** seguida del número de columnas del 1 al 12. Si no se añade ninguna otra clase esta funcionará para los 3 estados responsivos.

Las columnas responsivas funcionan como **".ct{col}"** y **".cm{col}"** y deben estar asignadas únicamente cuando ya existe la clase base, de lo contrario no se comportará correctamente.

| Columnas | Clase base (desktop) | Tableta | Móvil |
| -------- | -------------------- | ------- | ----- |
| 1        | .c1                  | .ct1    | .cm1  |
| 2        | .c2                  | .ct2    | .cm2  |
| 3        | .c3                  | .ct3    | .cm3  |
| 4        | .c4                  | .ct4    | .cm4  |
| 5        | .c5                  | .ct5    | .cm5  |
| 6        | .c6                  | .ct6    | .cm6  |
| 7        | .c7                  | .ct7    | .cm7  |
| 8        | .c8                  | .ct8    | .cm8  |
| 9        | .c9                  | .ct9    | .cm9  |
| 10       | .c10                 | .ct10   | .cm10 |
| 11       | .c11                 | .ct11   | .cm11 |
| 12       | .c12                 | .ct12   | .cm12 |

Ejemplo de un contenedor que mide 6 columnas, en tablet mide 10 y en móvil mide 12:

````
<div class="container">
	<div class="c6 ct10 cm12"></div>
</div>
````

#### Clase .c (ajustable)

Cuando se busca una columna que se ajuste automáticamente sin establecer columnas se puede utilizar únicamente la clase **".c"**, que se estirará dependiendo del tamaño disponible dentro del contenedor, es decir que si sólo existe 1 div, éste se estirará para medir las 12 columnas, pero si existen dos divs, ambos con la clase ".c", ambos medirán 6 columnas. Si ya existe un div con 10 columnas (.c10) y se añade otro (.c), éste ocupará las 2 columnas restantes.



<iframe height='265' scrolling='no' title='DW4.css | Ejemplo de uso' src='//codepen.io/ealbinu/embed/mObmYe/?height=265&theme-id=0&default-tab=html,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>See the Pen <a href='http://codepen.io/ealbinu/pen/mObmYe/'>DW4.css | Ejemplo de uso</a> by Albin Rodriguez (<a href='http://codepen.io/ealbinu'>@ealbinu</a>) on <a href='http://codepen.io'>CodePen</a>.
</iframe>