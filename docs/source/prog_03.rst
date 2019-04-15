Programado repeticiones
======

Hay muchas situaciones en la vida que debemos hacer algo repetidas veces,
como por ejemplo, ir checando una lista de papeles uno por uno, uno tras de otro
hasta finalizar, una tarea aburrida y tediosa, nos cambiaría mucho la vida si eso
se puediese hacer de forma automatica.

¿Qué aprenderé?
######

1. Conocer que son las repeticiones.
2. Saber cuándo debemos usar una repetición.
3. Crear una lista de elementos. 
4. Hacer un pequeño programa con repeticiones.

¿Qué necesito?
######

Debes haber leido los apartados:
 1. `Introducción a la programación </prog_01>`_ 
 2. `Programando decisiones </prog_02>`_

También seguiremos usando la aplicación **Thonny**

¿Qué es una repetición?
######

Una repetición en programación es cuando algo debe 
realizarse repetidas veces, como por ejemplo, tomar
la lista de artículos en nuestro bolso e ir anotando
las cantidades en un papel para compartirla con un
amigo, así como en los vídeojuegos de rol o también llamados
RPG. Vamos sacando uno a uno y contando cuantos hay y anotando
en el papel. Un ejemplo de esto en programación sería así:

.. code-block:: python

    print('Billetera: 1')
    print('Cantimplora: 1')
    print('Posima de energia: 2')
    print('Cinta de curacion: 10')
    print('Monedas de oro: 345')

El resultado en pantalla debería ser similar a esto:

.. code-block:: python

    Billetera: 1
    Cantimplora: 1
    Posima de energia: 2
    Cinta de curacion: 10
    Monedas de oro: 345

Entonces está es la lista de artículos en nuestro bolso
(las tildes las he omitido para evitar errores), no son muchos
y no es un problema aún, pero imagina que llevas 100, 1.000 o 10.000 
artículos, escribir 10.000 veces eso es un real problema ¿Cierto?.

La solución es usar las **repeticiones**, una forma de hacer lo mismo 
pero de forma automática, 100, 1.000, 10.000 veces o las que necesites
y de forma muy fácil.

Para esto vamos a ocupar otra **palabra reservada** llamada:

.. code-block:: python

    for

**for** en español significa **para**, y la forma de escribirlo es
la siguiente:

.. code-block:: python

    for articulo in bolso

¿Qué quiere decir esto?, que **para** cada **articulo** en el **bolso**
realice las instrucciones que le indiques al programa. Aqui hay algo
muy especial es que **for** te permite crear una **variable**, para 
este ejemplo, le hemos llamado **articulo** y vamos a tomar cada artículo
desde otra variable llamada **bolso**. ¿Pero, Dónde está la variable **bolso**?
La respuesta es creando una **lista**.

¿Cómo crear una lista?
######

Las listas son muy útiles y además son muy fáciles de crear. En 
programación, las listas se crean usando **[** para indicar donde
empieza la lista y **]** para indicar donde termina la lista y cada
artículo va separado por una **coma**.

Esto sería algo así:

.. code-block:: python

    bolso = [
        'Billetera: 1', 
        'Cantimplora: 1', 
        'Posima de energia: 2',
        'Cinta de curacion: 10',
        'Monedas de oro: 345'
    ]

Luego vamos a tomar los artículos uno a uno usando **for**

.. code-block:: python

    for articulo in bolso:
        print(articulo)

El resultado de esto será:

.. code-block:: python

    
    Billetera: 1
    Cantimplora: 1
    Posima de energia: 2
    Cinta de curacion: 10
    Monedas de oro: 345


Sí, exactamente el mismo que el anterior. Comparemos un poco 
el programa.

La forma tediosa:

.. code-block:: python

    print('Billetera: 1')
    print('Cantimplora: 1')
    print('Posima de energia: 2')
    print('Cinta de curacion: 10')
    print('Monedas de oro: 345')

La forma automática:

.. code-block:: python

    for articulo in bolso:
        print(articulo)

Como puedes notar, en tan solo **2 líneas**, hicimos exactamente lo 
mismo que en **5 líneas**, como muestra **la forma tediosa**, y lo mejor
de todo, es que no importa si son 100, 1.000 o 10.000, siempre serán
menos líneas, y lo importante acá es ahorrarnos trabajo, por eso
la programación es tan práctica y es tan linda, porque puedes hacer
con **muy poco** algo **muy grande**. Aquí ya podemos encontrarle 
el sentido a que las personas crean **apps** para facilitarle la vida
a la gente.

Pequeño programa con repeticiones
######

Ya que haz aprendido a realizar repeticiones, ahora vamos a 
crear un programa que le permita al gamer, añadir los artículos
que él quiera en su bolso, y luego vamos a mostrarle los artículos
que lleva en su bolso, esto es como el bolso de Ash en Pokémon.

Mira este ejemplo y ejecutalo en **Thonny**

.. code-block:: python

    bolso = [] #  El bolso esta vacio
    articulo = ''
    while True
        articulo = input('Escriba el Nombre del articulo a Guardar: ')
        if not articulo:
            break
        bolso.append(articulo)

    for articulo in bolso:
        print(articulo)

¿Haz notado que hay cosas nuevas como **while**, **True**, **not** y **break**?,
bien, **while** es otra **palabra reservada** y que también sirve para
hacer repeticiones, en este caso lo estamos usando para que le pregunte
al gamer, repetidas veces, cual es el siguiente artículo a ingresar al bolso. la ventaja que
tiene **while** es que se va a ejecutar siempre que lo que le siga a continuación
dé como resultado **verdadero**, en este caso, la palabra reservada **True**, tal
cual escrita con la **T** mayúscula, siempre nos dará un resultado **verdadero**,
ya que la palabra **True** en español significa **verdad**, así que esto
es un truco para que **while** haga de forma ílimitada repeticiones.

Luego vemos que después del comando **input()** está este código

.. code-block:: python

     if not articulo:
            break

La palabra reservada **not** nos sirve para verificar si algo **no es** lo
que debería ser, en este caso, nosotros estamos esperando que la variable **articulo**
lleve escrito el nombre del artículo que queremos ingresar al bolso, pero qué pasa
si el gamer no escribe ningún nombre, entonces asumimos que el gamer ya no quiere ingresar
más artículos porque ya no queda ninguno, así que no tiene ningún otro nombre por ingresar,
así que el gamer solo presiona **ENTER** sin ingresar nada, entonces al preguntar `if not articulo`
estamos preguntando, **Si no es un artículo entonces realice lo siguiente dentro de mi bloque**.
y justamente lo único que está dentro de este **if** es la palabra reservada **break**

¿Qué es **break**?, **break** permite detener de forma inmediata una repetición, sin
importar si faltan artículos más adelante, simplemente termina de repetir.

Esto hará que deje de repetir el **while** y ya no le preguntará más al gamer que ingrese
otro artículo, se saltará la línea

.. code-block:: python

    bolso.append(articulo)
    
y procederá a listar los artículos en pantalla

.. code-block:: python

    for articulo in bolso:
            print(articulo)

Un momento, ¿Qué es eso de **bolso.append(articulo)**?, aaah!, pensate que lo pasé por alto,
te explico, las listas son objetos con muchas funciones, y una de esas funciones
es permitir fácilmente agregar un elemento sin perder los que ya ingresaron anteriormente.

**append** en español significa **añadir** y para usar una función de lista debemos 
usar un **.** (punto) y luego escribir el nombre de la función (Que es parecido a 
un **comando**, ¿No te parece?).

Cuando escribimos **'bolso.'** le estamos indicando al programa que queremos usar una 
función. ¿Pero cómo sabe que funciones puedo usar?, el programa tiene una inteligencia
que cuando tu creas la variable de esta forma:

.. code-block:: python

    bolso = []

automaticamente el programa sabe que es una lista y que debe incorporarle las
funciones de listas. Ahora también hay una forma mucho más natural de crear listas 
y es usar:

.. code-block:: python

    bolso = list()


Ambas, **[]** y **list()** son exactamente lo mismo, la diferencia es que **list()** es 
un **comando** que te crea una lista y **[]** es una lista que creas de forma manual, 
pero el uso es exactamente el mismo y tienen las mismas funciones, digamos que son
dos formas de usar listas y es cosa de gustos.

Este artículo ha sido un poquito más complejo que los anteriores, por lo mismo
queremos ayudarte a que resuelvas tus dudas,  así que si necesitas una guía 
más personalizada contáctanos a través de nuestra `página de facebook Rdckgames <http://facebook.me/rdckgames>`_.

