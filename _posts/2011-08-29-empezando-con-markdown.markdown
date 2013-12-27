---
layout: post
title:  "Empezando con Markdown"
date:   2011-08-29 13:14:36
categories: markdown tutorial old
author: Daniel Rodríguez
twitter: sadasant
---

[0]:http://sadasant.com/ "Daniel Rodríguez"
[0t]:http://tecnoyucas.org/ "TecnoYucas.org"
[1w]:https://secure.wikimedia.org/wikipedia/es/wiki/Markdown "Markdown en Wikipedia"
[1o]:http://daringfireball.net/projects/markdown/ "Sitio oficial de Markdown"
[2]:https://secure.wikimedia.org/wikipedia/es/wiki/Lenguaje_de_marcas_ligero "Lenguaje de Marcas Ligero en Wikipedia"
[3]:http://daringfireball.net/ "'Daring Fireball' por John Gruber"
[4]:http://www.aaronsw.com/ "Sitio oficial de Aaron Swartz"
[5]:http://daringfireball.net/projects/markdown/dingus "Dingus, por John Gruber"
[Enlace1]:http://tecnoyucas.org/ "Texto Alternativo Opcional"
[Enlace2]:http://something.com
[6]:https://code.google.com/p/google-code-prettify/ "Google Code Prettify"
[7]:http://stackoverflow.com/ "StackOverflow.com"
[8]:http://stackexchange.com/ "StackExchange.com"
[9]:http://github.com "GitHub.com"
[10]:http://reddit.com "Reddit.com"
[11]:http://posterous.com "Posterous.com"
[12]:http://wordpress.com "WordPress.com"
[13]:http://tumblr.com "Tumblr.com"
[14]:https://github.com/tecnoyucas/Documentos-de-TecnoYucas "Documentos de TecnoYucas en GitHub"

[img0]:https://s.deviantart.com/th/fs70/f/2011/149/3/5/droid_01_by_sadasant-d3hiqxw.png "Droide PixelArt"

Tal como nos cuenta [este artículo de Wikipedia][1w], *[Markdown][1o]* es un *[lenguaje ligero de marcas][2]* creado por [John Gruber][3] y [Aaron Swartz][4] con la finalidad de conseguir la máxima legibilidad y facilidad de publicación de textos, tanto en sus formas de entrada como de salida. Markdown es dos cosas, un formato mucho más simple, limpio y legible que *HTML* para enriquecer textos, y un software para procesarlo en un *HTML* bien estructurado y listo para ser publicado.

[John Gruber][3] tiene un programa en línea al que llama [Dingus][5] que permite hacer pruebas con Markdown, pero además nos da una guía práctica y muy resumida de su sintaxis. Markdown posee muchas características de utilidad, entre las cuales puedo destacar que es capaz de identificar todas las nuevas líneas automáticamente, al separar una línea de otra él entiende que es una nueva línea sin necesidad de colocar la etiqueta "`<br/>`" de HTML. Si se insertan líneas vacías en el texto, él entiende que debe separar una línea mas, y si se quiere obligar a separar una línea de otra (o un elemento de otro) solo se deben colocar **dos espacios** al final de la línea anterior a la separación que se desea.

A continuación les explicaré poco a poco el resto de las características de este lenguaje, además de incluirles una diferencia visual con respecto a la estructura de HTML.

# Sintaxis de Markdown #  

### 1. Énfasis en oraciones: ###
> *Énfasis simple*    **Énfasis fuerte**

En HTML, hacer énfasis en frases u oraciones se puede hacer de esta manera:

    <em>Énfasis simple</em>    <b>Énfasis fuerte</b>  

En Markdown lo puedes hacer con menos caracteres y tienes dos posibles estilos:

    *Énfasis simple*    **Énfasis fuerte**
    _Énfasis simple_    __Énfasis fuerte__


### 2. Enlaces: ###
> [Enlace a TecnoYucas][0t]

Para colocar enlaces en el texto, en HTML acostumbramos a utilizar lo siguiente:

    <a href="http://tecnoyucas.org/">Enlace a TecnoYucas</a>

En Markdown hay tres maneras de hacerlo, iremos de fácil a recomendado (por no decir difícil). La primera manera de hacerlo es simplemente colocar el enlace dentro de un símbolo de menor-que "<" y otro de mayor-que ">", de esta manera:

    <http://tecnoyucas.org/>

El método anterior producirá este enlace: <http://tecnoyucas.org/>, que muestra como texto la URL a donde se dirige. Para hacer que un enlace tenga un texto distinto, debemos presentarlo de esta manera:

    [Enlace como este](http://tecnoyucas.org/ "Texto Alternativo opcional")

De esa manera logramos un [Enlace como este](http://tecnoyucas.org/ "Texto Alternativo opcional"), que posee un texto alternativo visible al colocar el puntero encima. El texto alternativo es opcional, por lo que podrías simplemente terminar la URL con un paréntesis.

El tercer método es el que más recomiendo, permite dar identificaciones únicas a los enlaces para separarlos del texto, y luego encerrar la frase que deseamos enlazar con corchetes, añadiéndoles la identificación también encerrada en corchetes. La sintaxis es así:

    [Enlace1]:http://tecnoyucas.org/ "Texto Alternativo Opcional"
    [Enlace2]:http://something.com
    
    Para ver [este enlace][Enlace1] simplemente tenemos que colocar la palabra que deseamos enlazar entre corchetes con la identificación al lado, también encerrada en corchetes.
    
    [Este otro enlace][Enlace2] no tiene texto alternativo, a diferencia del [primer enlace][Enlace1].

[Este enlace][Enlace1] y [este otro][Enlace2] fueron también incluidos en la codificación de este documento y pueden acceder a ellos aquí: [Enlace 1][Enlace1] y [enlace 2][Enlace2].

Este último método es sin duda mi favorito, ya que permite organizar los enlaces separados del texto y con una identificación única, que permite repetirlos en todo el contenido sin llenarlo con URLs ilegibles.

Un punto importante a aclarar es que **la identificación del enlace** puede estar **antes o después** del mismo. Adicionalmente deben recordar seguir la sintaxis tal cual como aparece en los ejemplos, es decir, al lado de la identificación del enlace se deben colocar los **dos puntos** ":" y después de la URL se debe colocar al menos **un espacio** para poder añadir el texto alternativo.


### 3. Imágenes: ###
> ![Droide PixelArt][img0]

Para colocara imágenes en HTML utilizamos una sintaxis como esta:

    <img src="https://s.deviantart.com/th/fs70/f/2011/149/3/5/droid_01_by_sadasant-d3hiqxw.png" alt="Droide PixelArt" title="Droide PixelArt" />

En Markdown, la sintaxis es bastante similar a la de los enlaces, pero hay solo dos métodos de hacerlo, el primero (el más sencillo) es el siguiente:

    ![Droide PixelArt](https://s.deviantart.com/th/fs70/f/2011/149/3/5/droid_01_by_sadasant-d3hiqxw.png "Droide PixelArt")

Lo que va entre corchetes "[]" es el texto alternativo (alt), y lo que va entre comillas es el título de la imagen (title), ninguno de los dos es obligatorio.

El otro método para insertar imágenes es bastante similar al tercer método de los enlaces:

    ![Droide PixelArt][img0]
    
    [img0]:https://s.deviantart.com/th/fs70/f/2011/149/3/5/droid_01_by_sadasant-d3hiqxw.png "Droide PixelArt"

Si se fijan, coloqué el enlace antes de la identificación, aún así funciona :)


### 4. Encabezados: ###
> Como el de arriba, que dice "4. Encabezados:".

Para colocar encabezados también existen dos maneras. La primera es seguir la frase con una serie de iguales "=" o signos negativos "-":

    Esto es equivalente a encerrar el texto en <H1></H1>
    ====================================================
    
    Esto es equivalente a encerrar el texto en <H2></H2>
    ----------------------------------------------------

Cualquier número de iguales o signos menos servirá, sin embargo, para editores mono-espaciados es quizás mejor colocar la misma cantidad de estos símbolos como tenga el texto.

El segundo método es encerrar el texto con numerales "#", la cantidad de numerales equivale al número de la H que deseamos (es decir, un solo "#" será igual a H1, dos serán iguales a H2). Para cerrar el encabezado se debe colocar un mínimo de numerales igual a la cantidad que lo abrió.

    # Esto es equivalente a <H1></H1> #
    ## Esto es equivalente a <H2></H2> ##
    ### Esto es equivalente a <H3></H3> ################


### 5. Listas: ###
> 1. Lista ordenada.
>    1. Lista ordenada y anidada.
>    2. ...  
>
> * Lista sin orden.
>    * Lista sin orden y anidada.
>    * ...

Las listas en HTML suelen hacerse de esta manera:

    <ol>
        <li>Lista ordenada</li>
        <ol>
            <li>Lista ordenada y anidada</li>
            <li>...</li>
        </ol>
    </ol>
    <ul>
        <li>Lísta sin orden</li>
        <ul>
            <li>Lista sin orden y anidada</li>
            <li>...</li>
        </ul>
    </ul>

En Markdown, para hacer listas ordenadas basta con colocar el número inicial seguido de un punto y uno o mas espacios ("1. ", "2.  ", "3. "). Para hacer listas desordenadas se puede usar un asterisco "*", u mas "+" o un menos "-". Utilizando asteriscos quedaría así:

    1. Lista ordenada.
        1. Lista ordenada y anidada.
        2. ...  
    
     * Lista sin orden.
        * Lista sin orden y anidada.
        * ...

Las listas, sin importar su nivel, asumirán que la línea que les sigue es parte de ellas, pero es recomendable colocar **tres espacios** después del símbolo de la lista en la primera línea y **cuatro espacios** antes de cada una de las siguientes líneas para un mayor entendimiento:

    *   Lista sin orden con varios párrafos
        Todavía sigue dentro de la lista.
        Esto también.

Para terminar una lista se debe colocar una línea vacía antes del siguiente bloque o texto.

### 6. Citas: ###
> Esto es una cita.  
    :)
> > Esto es una cita dentro de una cita.

En HTML las citas se escriben dentro de las etiquetas "`<blockquote></blockquote>`", en Markdown es tan sencillo como colocar un símbolo de mayor-que ">" y **un espacio** antes de cada línea:

    > Esto es una cita.  
        :)
    > > Esto es una cita dentro de una cita.

Para separar las líneas de una cita no basta con insertar una línea más, hay que forzar la separación colocando **dos espacios** al final, pero puedes colocar muchas líneas o párrafos dentro de una cita simplemente colocando cuatro espacios en cada línea después de la línea inicial, que deberá empezar con el símbolo de mayor-que *>* y el **espacio**.

Los bloques de citas pueden contener cualquier cosa, desde otras citas hasta código, imágenes, listas, de hecho todos los ejemplos que he utilizado después de cada número de este tutorial han sido citas escritas con *Markdown*.

### 7. Código: ###
>     for (var i = 0; i <= 10; i++) {
>          if (i == 5) alert("¡Mira, un "+i+"!");
>     }

Pre-formatear el código es uno de los aspectos más útiles de Markdown, es tan sencillo como colocar **cuatro espacios** iniciando cada una de las líneas que deban estar dentro del bloque de código. Esto en esencia solo crea las etiquetas "`<pre><span></span></pre>`" y dentro de ellas el código con los espacios adecuados y los caracteres escapados para que no se mezclen con el HTML. Si quieren lograr que la sintaxis se coloree deben utilizar librerías JavaScript como [Google Code Prettify][6], para lo cual deben insertar el siguiente código antes de terminar el "`</header>`" de sus páginas:

    <script src="http://code.jquery.com/jquery-1.6.2.min.js" type="text/javascript"></script>
    <link href="http://google-code-prettify.googlecode.com/svn/trunk/src/prettify.css" type="text/css" rel="stylesheet"/>
    <script src="http://google-code-prettify.googlecode.com/svn/trunk/src/prettify.js" type="text/javascript"></script>
    <style>
    pre.prettyprint {
        overflow-x: auto;
        margin: 5px 20px 20px;
    }

Y el siguiente código al final de la misma, después del "`</body>`" y antes del "`</html>`":

    <script>
        $("pre").addClass("prettyprint");
    </script>

De este modo, todo el texto que tengamos dentro de etiquetas "`<pre><code></code></pre>`" estará pre-formateado por Markdown y coloreado por Google Code Prettify, tal como hacemos en este Tumblr.

Otra manera de colocar el código dentro de otros bloques o líneas de texto. En markdown es tan sencillo como encerrar ese segmento del texto en estos símbolos: **\`**, de esta manera:

    El código embebido dentro de "`<pre><code></code></pre>`" estará pre-formateado por Markdown

### 8. Reglas Horizontales: ###
Las reglas horizontales, que en HTML podemos escribir de esta manera "`<hr/>`", en Markdown se forman con mínimo tres asteriscos "\*" o símbolos negativos "-", con o sin espacios entre ellos, como pueden ver a continuación:

    ***
    * * *
    
    - - - --
    ----- - - -

El código de arriba producirá esto:

***
* * *
- - - --
----- - - -  

# Ejemplos de usos de Markdown #

*Markdown*, aunque pase desapercibido, es utilizado por [StackOverflow][7] y otras plataformas de [StackExchange][8], además de [GitHub][9], [Reddit][10], [Posterous][11], [WordPress][12] y tal como ven en esta publicación: [Tumblr][13].

Si desean ver ejemplos de cómo nosotros utilizamos esta tecnología, pueden ir a [nuestros documentos en GitHub][14]. Para más detalles pueden visitar el [artículo en Wikipedia][1w], o el [sitio web oficial de Markdown][1o]

Espero les haya sido de utilidad este tutorial :)
