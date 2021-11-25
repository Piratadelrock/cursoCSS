# QUE ES CSS
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

# formas de css 
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

# COLORES 
    Estos estan disponibles en la lista de colores de los editores como black, white, tomato, 
        pero los principales son rgb, hexadecimal, y los hsl 
    
    para un color hexadecimal, se coloca # seguido de 6 digitos 
    0= maxima ausencia de color(LA AUSENCIA DEL COLOR ES NEGRO)
    f= maxima expresion del color(LA EXPRESION DEL COLOR ES BLANCO) 
    
    podemos indicar los colores indicando 3 caracteres o los 6 caracteres 
    * convencion
    #000 nos entrega el color negro, si lo que hago es remplazar el primer digito
        #f00: rojo, en su primer digito (en su mayor expresion)
        #0f0: verde,en su segundo digito (en su mayor expresion)
        #00f: azul, en su tercer digito (en su mayor expresion)
    #ff0: amarillo, mientras mas alto sea el valor mas cercano al color blanco va a ser
         significa que como f es mas alto colocar 2 efes sera mas claro y blanco 
    #eee : gris suave

