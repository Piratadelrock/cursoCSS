# CSS
    Cascading style sheets
    describe la presentacion de los docs HTML
    un doc HTML puede tener multiples estilos css
    con un HTML se puede cambiar los css para que se vean de diferentes estilos el mismo doc html

# COMO FUNCIONA CSS (estructura)
    selectores: seleccionar elementos que se encuentren documento html, 
    seleccionar +1 elementos: uno o mas de un elemento  
        html {} seleccionamos html 
        * {} es para seleccionar todos los elementos 
        .card {} clase css card seleccionando posibles elementos que se llaman card
    propiedades: las propiedades son internas en las llaves. 
                propiedad : el valor ;

# Formas de css 
    dentro de etiquetas o elementos de html 
    <body  style="color: tomato;">
    dentro de la etiqueta head colocar un 
            <style> 
                body{
                        color: tomato;
                    }
            </style>
    * la mas adecuada sera crear un archivo style.css dentro de una carpeta css 
      usando el link para importar el archivo css en el html 
        <link rel="stylesheet" href="./css/style.css">

        dentro del archivo usaremos el uso de el css.
         body{
              color: tomato;
             }

# SELECTORES
    colocando la etiqueta 
    colocando id: 
        <h1 id="titulo">texto</h1>
        en css usamos # para identificar el id de cualquier etiqueta 
            #texto
    realizando clases 
        <p class="texto">texto</p>
        en css . para identificar la clase de cualquier etiqueta y p.texto para identificar
        cualquier clase llamada texto pero solo de la etiqueta p
            .texto{
                propiedad:;
            }
    realizando etiqueta sobre etiqueta 
    div p {
        los espacios cuentan
    } : En todas nuestras etiquetas div que contengan hijos(nietos tataranietos...) de etiqueta p 

    selector universal: este posee un catch o truco o maña, aplica las propiedades solo si estas no han sido definidas por otros selectores 
    que dependiendo del orden que escribamos nuestro css, es como se ira aplicando este estilo 
    por lo que si queremos realizar un override o queremos reemplazar un estilo de css a una etiqueta que se halla escrito mas arriba, y se coloque al final, esto quiere decir que color deberia remplazar a todos los demas colores que se an puesto anteriormente 
    *{
        color : black;
    }

# PROPIEDADES CSS

## UNIDADES DE MEDIDA DE CSS
    asignar dimensiones a los elementos utilizando css antiguamente los monitores usaban cuadrados pequeños usando rgb para mostrar algo al usuario, se puede identificar en algun monitor de baja densidad, no ocurre con los telefonos porque tiene alta densidad de los pixeles.

    un pixel es una unidad relativa que trata de hacer referencia a ese cuadrado de luz o led con el cual se puede generar imagenes
    pero dependiendo del dispositivo esto podria representar mas de uno de esos cuadraditos, como un iphone o samsung de alta densidad de pixeles, un pixel equivale a 4 de esas luces, inclusive puede equivaler a mas si tiene mayor densidad de pixeles, 
    un pixel es la unidad minima que se necesita para poder mostrar algo.

    sin embargo, existen otras unidades son relativas que son relativas al tamaño del dispositivo, por ejemplo centimetros, pulgadas o milimetros 
    si usamos centimetros, nos damos cuenta que no son exactamente 1 cm dependiendo del dispositivo que se este utilizando, por lo que no sera algo tan 
    confiable, y tampoco significa que si damos 1cm esto se vera igual en todos los dispositivos, es subjetivo dependiendo de los dispositivos que se vea 

        1cm no necesriamente sera 1 cm si pasamos a mm (milimetros)
        ch
        em
        cm
        mm
        in 
        pt (puntos)
        pc (1picas son 12 puntos)
        px
    estas medidas no son recomendables usar para diferentes dispositivos es mejor usar medidas relativas a las fijas

    2em (2veces el tamaño de la fuente que se esta utilizando actualmente,
    cambia dependiendo del elemento que se esta usando)
    2rem (relativo al tamaño de la fuente del elemento raiz, se encuentra dentro de nuestro html y es nuestra etiqueta html, se puede considerar 1 rem = 16px o 2rem=32px a no ser de que cambiemos el tamaño de la fuente que en este caso esta en 24px)

## color PROPIEDAD
    Estos estan disponibles en la lista de colores de los editores como black, white, tomato, 
    pero los principales son rgb, hexadecimal, y los hsl 

### Hexadecimal  
    para un color hexadecimal, se coloca # seguido de 6 digitos 
    0= maxima ausencia de color(LA AUSENCIA DEL COLOR ES NEGRO)
    f= maxima expresion del color(LA EXPRESION DEL COLOR ES BLANCO) 
    
    podemos indicar los colores indicando 3 caracteres o los 6 caracteres 

    * convencion 3 digitos
        #000 nos entrega el color negro, si lo que hago es remplazar el primer digito
            #f00: rojo, en su primer digito (en su mayor expresion)
            #0f0: verde,en su segundo digito (en su mayor expresion)
            #00f: azul, en su tercer digito (en su mayor expresion)
        #ff0: amarillo, mientras mas alto sea el valor mas cercano al color blanco va a ser
            significa que como f es mas alto colocar 2 efes sera mas claro y blanco 
        #eee : gris suave
   
    convencion 6 digitos #000000
        los dos primeros ceros son rojos
        los 2 del medio son verdes 
        lso 2 finales son azul 

### rgb
    se ubica como    color: rgb(red, green, blue)
    rgb(0,0,255)
### rgba
    para usar transparencia 
    colocamos a y podremos agregar un 
    1 mayor opacidad y 0 menor opacidad
    se puede usar como si fuera rgb es decir dejandolo asi:
         rgba(0, 0, 0); queda negro 

    background-color: rgba(0, 0, 0,0.3); queda negro transparente y permite ver elementos detras de el
    
    opacity: es pasando la propiedad al elemento completo 
    1 se ve completamente
    0  no se ve en absoluto 
    opacity: 0.3; 

    esta oculta todo el texto porque el fondo era negro 
    pero ahora vemos que el rojo es mas suave y el texto tambien es transparente
    toma el elemento completo y no solo al color en especifico
___

    
## border PROPIEDAD
   
    border: 5px gold ridge;
    /* 
        dotted
        dashed
        solid
        double
        groove - valores que se pueden asignar a objetos tridimensionales
        ridge
        inset
        outsed
        none
        hidden
    */
    
    border-style: groove;
    border-color:blue;
    border-radius: 5px;
    border-width: 5px;
___

## background PROPIEDAD
    indicando una imagen de fondo 
        background-image:url('../img/coffee.png');
        height: 300px;
         background-size: cover;
     
    * auto: nos definira automaticamente la imagen respecto al tamaño del elemento 
    * contain: sirve para contener la imagen en las medidas que le especifiquemos

    * cover: nos cubrira la imagen unica usando el el ancho completo del elemento html, ADEMAS DE QUE SE ADAPTA MIENTRAS CAMBIA DE TAMAÑO LA PAGINA, COSA QUE LOS DEMAS NO HACE.

    tambien asignamos dimensiones siendo el primero el ancho, el segundo el alto
    background-size: 400px 400px;

    /* asignamos alto de imagen */
    /* height: 400px; */

### background-repeat
    background-repeat: no-repeat;
    repetir en horizontal
        background-repeat: repeat-x;
    repetir en vertical
        background-repeat: repeat-y;

    height: 200px;
    /* background-image:url('../img/coffee.png');
    background-repeat: repeat-y;
    /* primer valor es en el eje horizointal el otro es vertical 
    o tambien valores de dimension */
    /* background-position: center top; */ 
## background en general
    Se podra definir lo anterior en una sola linea 
    el background size debe ir despues, no lo toma antes
        background: #ff0 url('../img/coffee.png') repeat-y center bottom;
        background-size: 100px 100px;
        opcion con el size:
        background: #ff0 url('../img/coffee.png') repeat-y center bottom / 100px 100px;
## margen margin
    para diferenciar 
    background-color: chocolate;
    
    /* top right bottom left */
    /* margin son espacios generados fuera del elemento */
    margin: 15px 20px 25px 30px;
    /* padding son espacios generados dentro del elemento */
    padding: 30px 25px 20px 15px;
    /* border esta afuera de pading pero dentro de margin, 
    justo en el medio */
    border: solid 1px black;
     /* un borde pero externo antes del margin*/
    outline: 1px red solid;
## text 
     /* si en caso de no ser cargada la primera seguira con la siguiente */
    font-family: Verdana, Geneva, Tahoma, sans-serif;
    /* left es por defecto, justyfy toma todo el ancho disponible*/
    text-align:justify;
    /* ancortag  */
    /* text-decoration: underline ; */
    /* text-decoration: line-through ; */
    text-decoration: overline;
    /* sombreado:
    1erdato: cuanto se mueve a la derecha 
    2do: cuanto se mueve hacia abajo 
    3er da un color de sombra o agregando pixeles para mejorar el difuminado (blur)
    4to el color
    */
    /* este texto aparece por detras  */
    /* text-shadow: 3px 5px blue; */
    /* este contiene blur para difuminar la sombra */
    text-shadow: 3px 5px 5px blue;

# BOXMODEL CSS
    boxmodel: margen, un border, un pading y el contenido.

    Es como se posiciona cada elemento html en nuestro documento
    y toda etiqueta va a tener un margen un border un padding y el contenido.
    cuando especificamos la propiedad de width de un elemento 
    estamos indicando solo el ancho que tendra el contenido que se encuentra dentro de la etiqueta, no contempla el margin ni el padin, ni el border, por lo que 
    si queremos calcular el ancho completo que va a tener el elemento tendremos sumar todos estos elementos, el margin el border el pading 

