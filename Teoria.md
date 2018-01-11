# Diseño Responsivo [Enlace a la LU](http://learn.ironhack.com/#/learning_unit/2596)


### ¿Que es? 

El diseño web que permite que los contenidos expuestos se puedan adaptar a cada dispositivo.
Es mas que obvio que hoy en dia el contenido digital web se ha dejado de consumir en exclusiva en el PC,
es por ello que en la actualidad el diseño ha virado en el sentido de construcción de la web.

_Antaño pensabamos en la web como algo propio del escritorio, a partir de ahi construiamos y tras ello pensabamos_
_en los posibles dispositivos secundarios que fueran a comsumir dicho contenido. Hoy en dia todo eso ha cambiado y_
_en la actualidad la mayoria de los contenidos se consumen en telefonia y menos grado tabletas. Es por ello que actualmente_
_trabamos con la filosofía: MOBILE FIRST. Pensamos en como desarollar nuestro contenido para la version movil haciendola_
_extensible a otros formatos. Para enfrentarnos a esta metodología debemos pensar de manera "minimalista" pues el tamaño de_ 
_las pantallas aun siendo creciente en los último años siguen siendo reducidas respecto de aquello que puede ofrecer un ordenador._

### ¿Y como "demonios" hago que mi web valga para todos los dispositivos?

He aqui el eje central de esta "learning unit" :
> La MEDIA QUERY es sin duda el elemento sobre el que vertebrar nuestro diseño responsivo.

### Sintanxis

- **!!BUENA!!**
    `@media [(media-features)] {`
       `// Styles`
    `}`
    
- **!!CACA!!**
`<link rel="stylesheet" media="(media-features)" href="styles.css" />`


### Viewport Meta Tag

`<meta name="viewport" content="width=device-width, initial-scale=1">`

Para los mas curiosos donde pone content estamos fijando que el ancho se correspondera con el ancho de la pantalla.
La escala inicial especifica el nivel de zoom que tendra la página al cargar por primera vez.

### Hablemos de las fuentes

Obviamente la fuente que usaremos en un escritorio no tiene nada que ver con la que debemos emeplear en un movil. Es por ello
que debemos trabajar en el uso de fuentes tambien responsivas, al igual que el trabajo con los anchos de linea.

- Font-size: XXpx
- Line-heigt: XXpx --> Esta propiedad solo afecta a la altura de la página. Como recomendación usemos 1.2em to 1.45em

### Implementando fuentes responsivas

#### CSS Viewport Units
Este tipo de nomenclatura para las fuentes nos permite el que estas se adapten a la pantalla en las que estan siendo exhibidas

vw. Viewport width. 1vw es igual a 1% del viewport width.
vh. Viewport height. 1vh igual a 1% del viewport height.
vmin. Viewport minimum. Relativo a la minima dimensión.
vmax. Viewport maximum. Relativo a la máxima dimensión.
The problem with viewport units


##### Esto no será un camino de rosas...

- Texto demasiado grande o demasiado pequeño, al encontrarnos con un mal uso como 1vw en una pantalla con 1920px de ancho, produciendo una tipo de 19px, sin embargo este mismo tamaño se reduce e 6px en una pantalla de 640px
- Un problema curioso es que al depender el tañaño de la fuente de la anchura de la ventana puede suceder que el ancho del sitio sea menor, produciendo una escala superior a la que se expera, al igual que puede ocurrir con el tamaño minimo.


### Pixels, ems, rems and Media Queries

El otro modo que tenemos para crear fuentes responsivas es el uso de los siguientes atributos:

- px. Dentro de una media query podemos expecificar el tamaño de la letra de nuevo.
- em. Hace que el tamaño se relativice respecto del anterior tamaño definido: si el padre tiene fiente de una fuente
      de 10px, y asignamos una fuente de 2em estaremos hablando de 20px.
- rem. Hace referencia al tamaño definido para todo el HTML. Funciona igual que em.

### Tips de diseño

- NO usar elementos grandes de ancho fijo: por ejemplo, si una imagen se muestra con un ancho más ancho que la ventana gráfica, puede hacer que la ventana se desplace horizontalmente.

- NO permitir que el contenido dependa de un ancho de ventana particular para representarlo bien . Dado que las dimensiones y el ancho de la pantalla en píxeles CSS varían ampliamente entre los dispositivos. "Evitar el uso de px".

- Establecer anchos de CSS absolutos grandes para elementos de página hará que el elemento sea demasiado ancho para la ventana gráfica en un dispositivo más pequeño. Considerar el uso valores de ancho relativo, como ancho: 100%. Además, tengan cuidado de usar valores grandes de posicionamiento absoluto, puede hacer que el elemento se caiga fuera de la ventana gráfica en dispositivos pequeños.


[Enlace a Ejemplo1](https://victoririx.github.io/CSS-Media/mediasimple)
[Enlace a Ejemplo2](https://victoririx.github.io/CSS-Media/mediadoble)