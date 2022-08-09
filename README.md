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

    /* el orden de los selectores influye en las propiedades que le asignemos 
    si por ejemplo movemos p.texto encima de p.especial, los colores cambiaran
*/

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


#fondo {
    /* como debe quedar */
    background-color: rgba(255, 0, 0);
    height: 200px;
    background: #ff0 url('../img/coffee.png') repeat-y center bottom / 100px 100px;

    /* opacity: 0.3; */
    /* indicando una imagen de fondo
    background-image:url('../img/coffee.png');
    background-repeat: repeat-y;
    /* primer valor es en el eje horizointal el otro es vertical 
    o tambien valores de dimension */
  
    /* background-position: center top; 
    background-size: 100px 100px; */

    /* asignamos alto de imagen */
    /* height: 400px; */

    
}
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
    /* quitando valores cambiara la forma del padding */
    /* border esta afuera de pading pero dentro de margin, 
    justo en el medio */
    border: solid 1px black;
       /* todo el contenido que no alcanza a mostrarse dentro del elemento 
    lo oculta 
    lo podemos cambiar por scroll y agrega barras laterales, 
    y poder ver el contenido que tiene  */
    overflow: scroll;
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
    text-shadow: 3px 5px 5px blue;}

    para fuentes customisadas
        google font la mayoria son gratis
    buscamos y seleccionamos la fuente deseada y nos podremos descargar la fuente o podemos usar 
    en el html del head el link de la fuente 

# BOXMODEL CSS
    boxmodel: margen, un border, un pading y el contenido.

    Es como se posiciona cada elemento html en nuestro documento
    y toda etiqueta va a tener un margen un border un padding y el contenido.
    cuando especificamos la propiedad de width de un elemento 
    estamos indicando solo el ancho que tendra el contenido que se encuentra dentro de la etiqueta, no contempla el margin ni el padin, ni el border, por lo que 
    si queremos calcular el ancho completo que va a tener el elemento tendremos sumar todos estos elementos, el margin el border el pading 

# links 
    los links en html pueden tener 4 estados 
        no ha sido visitado 
        ha sido visitado 
        se pasa por mouse encima de el 
        se encuentra activo
    * seleccionar todos los links 

    a:link{} estamos indicando a css, queremos es seleccionar 
    cuando el link no ha sido seleccionado
    a:visited{} indica los visitados
    a:hover{} indica el puntero encima del link
    a:active{} cuando pincho el link (activo)

# tablas 
    
    se puede interactuar de varias formas con las tablas, dandole colores centrando textos un ejemplo seria:

    table {
        width: 100%;
        /* eliminando espacio entre celdas */
        border-collapse: collapse;
    }

    th,td{
        border: solid 1px #eee;
        padding: 5px;

    }
    th{
        background-color: tomato;
        color: white;
        text-align: left;
    }

    tr:hover{
        background-color: #aaa;
    }
    /* seleccionar elementos sean pares o impares 
    dependiendo si esta en un listado o una tabla, dando colores a cada celda par o impar  
    odd = par 
    even = impar
    SUGERENCIA: no quise mover esta propiedad para que se den cuenta de que debe estar arriba de la propiedad anterior hover, para demostrar que se esta seleccionando */

    tr:nth-child(even){
        background-color: #eee;
    }

# display
    nos indica como nosotros vamos a colocar los elementos del html en el documento 
    " la etiqueta de span hace una seleccion silenciosa de nuestros elementos, pero cuando trabajabamos con los divs o p esta necesariamente hacia un salto de linea."

    En la mayoria de elementos viene la propiedad de display:block;

    usando la etiqueta div y span se puede comparar que abarca todo el documento o solo el elemento en el caso de span, haciendo una modificacion del elemnto span podemos hacer que se vuelva block

    span{
        display: block;
    }
    tambien podemos modificar los divs, podemos darle una clase y usar display: inline-block;
    se puede usar las siguientes propiedades:
    block: todo el ancho
    inline-block: solo el contenido del elemento

    height y width pueden ser asignados a inline-block la propiedad inline no puede ser aplicado 
    inline block se usa mucho para menus navegacion siempre que tenga los links de izq a der o der a izq  de esta manera se le puede asignar un ancho fijo y pueda estar de manera uniforme

# ocultar elementos 
    display:none;
    visibility: hidden;

# widh y max-width
    max-width: 300px; se vuelve dinamico y reduce su tamaño o maximiza su tamaño hasta los 300
    width: 300px; se mantiene los 300 

# position 
        
    valor por defecto: 
    * static, vienen todos los elementos de html 
    relative: es una posicion relativa a donde debiese estar posicionado este elemento
    
    position: relative;
    left: 20px;
    /* top: 25px; */

    fixed: dice que tiene que tener una posicion con respecto a lo que se esta viendo en el explorador
    digamos que el elemento se mantiene en la pagina 
    position: fixed;

    lo que hace absolute ocurre lo mismo que fixed pero no se mueve, este se posiciona relativo con el elemento padre mas cercano que este tenga, y en caso de no existir un elemento padre se pegara a body 
    position: absolute

    sticky: esta tomando la posicion que le corresponde, si hace scroll no realiza nada, pero si se le agrega la propiedad top empieza a realizar algo 
    mezcla de relative y fixed
    position: sticky;
    left: 20px;
    top: 25px;

# flotante float
    como el elemento esta dentro de otro elemento se puede notar que un elemento queda flotante hacia el lado donde lo posicione, en este caso se posiciona a la izquierda, el div que lo contiene tiene una altura definida y tiene un ancho de 100, pero el que tiene el ancho de 100 solo es el ellemento flotante de la izquierda, sin embargo todo el resto del contenido se desplazo hacia abajo no asi el elemento que se encuentra al lado, y es porque seencuentran dentro del mismo div

    toma el elemento y dentro de la etiqueta html en la que se encuentre lo va a hacer flotar a la izquierda

   .left{
        float: left;
        width:100px;
    }
# CENTRAR CON CSS
    margin: 0 auto; 
    indicando el 0 top y bottom no se centre veritcalmente 
    auto se centra horizontalmente
    dandole un padding vertical de 50px y 0 en horizonal podemos centrar el texto verticalmente, el text aling centrara horizontalmente
    .center{
        padding: 50px 0;
        text-align: center;
        width: 200px;
        margin: 0 auto;
        background-color: aqua;
    }

   con lo que se aprendio hasta ahora se puede dar cualquier estilo a cualquier elemento, usando el selector de hover, en un boton se puede cambiar el color para cuando se pase cambie de color, suponiendo que "es presionable"

# HTML SEMANTICO
	para indicar si hay una barra lateral un menu de navegacion etc

	<article> artigulo de la pagina
	<aside>barra lateral del menu            
	<figcaption>imagen y texto descriptivo de las imagenes  
	<figure> hace de la imagen en si
	<header> encabezado
	<footer>pie de pagina
	<main> contenido principal(que si alguien busca por el contenido lo encuentre)
	<nav>menu de navegacion  
	<section> seccion de la pagina
	<time>ira dentro un reloj, o cualquier cosa de tiempo

	div es un contenedor no semantico pero que ayuda a maquetar el contenido de la pagina
	por ejemplo para dos secciones diferenciadas se realiza dos divs con textos y demas
	en inspeccionar elemento se ve un color naranja o el mas grande  seria el contenedor

	*se debe indicar semanticamente cada cosa para que se pueda encontrar mejor en los buscadores
	*normalmente seria header y dentro del header el nav 

	header
		nav 

	article   	   aside 
		figure

	footer

	<form>  como por ejemplo para que el cliente se comunique con nosotros 
			se crea un form para indicar a html que apartir de ahora sera un formulario 
			lo que valla dentro del form seran elementos que el cliente pueda introduccir datos 
			selecionando entre diferentes soluciones y demas
			sus atributos serian 
		
	<form action="" method="">
		*action: que indica la url, puede ser cualquier pagina o una
		api para redirigir esa informacion(destino)
		*method: GET POST PUT DELETE
		*
	<label for="nombre">Nombre:</label>
		suele ir acompañado de imput para introducir los elementos solicitados
		*for para que objeto
	<input type="text">
		type 
		*text cajon para escribir 
		*number solo se puede ingresar numeros
		*password oculta el texto


~~~
html:5
<!DOCTYPE html>
<html lang="es">
    <head>
        <meta charset="utf-8">
        </meta>
		<!-- se le da compatibilidad a otros navegadores que no tienen ciertas propiedades porque no renderizan de la misma manera y dejan por un lado 
		ciertas opciones -->
		<meta http-equiv="X-UA-Compatible" content="IE=edge">
		<!-- contenedor visual de la aplicacion, viewport, sea multidispositivo por el content device-width el tamaño del dispositivo  -->
		<meta name="viewport" content="width=device-width, initial-scale=1.0">
		    <title>
                estructura basica
            </title>
    </head>
    <body>
    </body>
</html>

<!-- html>head+body -->
<html>
    <head>
		<nav><a href="index.html">inicio</a></nav>   

    </head>
    <body>
		<p>elementos que se pueden escribir para crear mas rapido etiquetas</p>
		<section id="editable" contenteditable="true">
			<ol>
				<li>html:5</li>
				<li>html>head+body</li>
				<li>div.caja>ul>li*5>a</li>
				<li>ul#nav>li.item$*4>a{Item $}</li>
				<li>h1.title>span.span</li>
				<li>ul>li*5>a</li>
				<li>.content</li>
				
			</ol>
	</section>
			<!-- div.caja>ul>li*5>a 
			<div class="caja">
				<ul>
					<li><a href=""></a></li>
					<li><a href=""></a></li>
					<li><a href=""></a></li>
					<li><a href=""></a></li>
					<li><a href=""></a></li>
				</ul>
			</div>
	
	
			ul#nav>li.item$*4>a{Item $} 
			<ul id="nav">
				<li class="item1"><a href="">Item 1</a></li>
				<li class="item2"><a href="">Item 2</a></li>
				<li class="item3"><a href="">Item 3</a></li>
				<li class="item4"><a href="">Item 4</a></li>
			</ul>
	
			 h1.title>span.span 
			<h1 class="title"><span class="span"></span></h1>
			 ul>li*5>a 
			<ul>
				<li><a href=""></a></li>
				<li><a href=""></a></li>
				<li><a href=""></a></li>
				<li><a href=""></a></li>
				<li><a href=""></a></li>
			</ul>
	
			 .content
			<div class="content"></div>
			 -->
    </body>
</html>
~~~