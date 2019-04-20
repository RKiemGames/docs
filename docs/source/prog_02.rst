Programando decisiones
######

.. image:: https://lh3.googleusercontent.com/s9JY6oNZ2-ceHFBsXD1fW3HP6PXyoxZiDamc1CQpCw5hl2kZ-qgDLDmQVhiiD36RXv3PWOs1BvXPMqkYSJn2m_5znEvZbr1AUtZ7j7IU7FuNqudTqzmzj_BmArkAvefcz0Irh1Wp7g=w410-h253-no
    :align: center


Programar decisiones suele sonar muy raro, pero lo que realmente haremos
en este capítulo es hacer que el programa tome decisiones cuándo nosotros se lo 
indiquemos.

Imagina que vas en tu automóvil y te encuentras que la ruta se divide en 2 
caminos y debes escoger 1, para este caso tu debes tomar una decisión como
conductor, pero esa decisión no es al azar, la tomas de acuerdo a información
que te dice cual es la ruta correcta, en este caso puede ser que google map
te indica que es la ruta más corta para llegar a tu destino y tu con esa 
información tomas el camino indicado.

¿Qué aprenderé?
======

1. Saber cuándo debes programar una decisión.
2. Como se escriben las decisiones cómo se componen.
3. Un comando nuevo: **int()**
4. Realizar un pequeño programa que toma decisiones.

¿Qué necesito?
======

Seguiremos usando el programa **Thonny**, pero no requieres nada más así que
te recomendamos tener abierta la aplicación.

Si no sabes que es **Thonny** puedes ir a la `introducción a la programación <prog_01.html#que-necesito>`_.

¿Qué es una decisión?
======

Una decisión en programación es mucho más básica que lo que nosotros hacemos 
a diario, las computadoras son más limitadas que nuestro cerebro y solo pude 
saber si algo es cierto o es falso comparando 2 cosas.

Por ejemplo podemos decirle a la computadora que compare 2 números y nos diga
si uno es mayor que otro, y de ser así, haga algo y sino, haga otra cosa.

Si volvemos al ejemplo anterior de usar una **edad**, imagina que debemos 
preguntarle a un **gamer** que edad tiene, y hacer que el juego tome la decisión 
de dejarlo entrar a la partida o denegarle el acceso, simplemente porque es para
personas desde 18 años en adelante.

¿Cómo creo una decisión?
======

Para esto cualquier lenguaje de programación usa las llamadas **palabras reservadas**
y esto lo hace porque como decíamos anteriormente la computadora es limitada y
necesita tener una **lista de palabras** que **no puedes usar como variables**.
Pero no te preocupes tanto de esto si llegaras usar una por desconocimiento 
la computadora te dirá que no puedes usar ese nombre como variable y que le 
coloques otro.

Continuando, para tomar decisiones en programación se hace con la palabra:

.. code-block:: python

    if

**if** en español significa **SI**, de la misma forma cuando uno se pregunta,
¿Qué pasaría **SI** hoy nevara?. básicamente lo que le estamos indicando al
programa es que haga una pregunta. LLevándolo al ejemplo, verificaremos si la persona 
es mayor de 18 años y para ello debemos usar los llamados **operadores**.

¿Qué son los operadores?
======

Los operadores nos permiten comparar 2 cosas, en nuestro ejemplo **la edad ingresada
por la persona** con **la edad de mayoría de edad** que es **18**. Para ser más precisos
se llaman **operadores lógicos**, pero por ahora esto no es relevante.

Los operadores lógicos básicos son símbolos y se listan a continuación:

+---------------+-------------------------+-------------------------------------------------------------------------+
| Símbolo       | Se escribe              | Descripción                                                             |
+===============+=========================+=========================================================================+
| **<**         | a < b                   | Compara si la variable **a** es **menor qué** la variable **b**         |  
+---------------+-------------------------+-------------------------------------------------------------------------+
| **>**         | a > b                   | Compara si la variable **a** es **mayor qué** la variable **b**         |
+---------------+-------------------------+-------------------------------------------------------------------------+
| **<=**        | a <= b                  | Compara si la variable **a** es **menor o igual qué** la variable **b** |
+---------------+-------------------------+-------------------------------------------------------------------------+
| **>=**        | a >= b                  | Compara si la variable **a** es **mayor o igual qué** la variable **b** |
+---------------+-------------------------+-------------------------------------------------------------------------+
| **==**        | a == b                  | Compara si la variable **a** es **igual qué** la variable **b**         |
+---------------+-------------------------+-------------------------------------------------------------------------+
| **!=**        | a != b                  | Compara si la variable **a** es **distinta qué** la variable **b**      |
+---------------+-------------------------+-------------------------------------------------------------------------+

Teniendo de referencia la tabla anterior haremos nuestra primera comparación, escribe
este programa:

.. code-block:: python

    edad_minima = 18

    edad_gamer = input('Ingrese su edad: ')

    if int(edad_gamer) >= edad_minima:
        print('Hola, eres bienvenido a nuestra crew')

Como te puedes dar cuenta, acá hemos creado una variable llamada **edad_minima** 
para almacenar la edad mínima que es 18 años, y así dejar al gamer entrar a la crew, también 
supongo que te diste cuenta que existe un **guión bajo** (**_**) entre **edad** y **minima**,
esto es porque las variables **no pueden contener espacios**, así que un truco es 
colocarlas con guiones bajos para que parezca una frase, y así es más fácil
entender el programa.

También hay otra cosa más aquí

.. code-block:: python

    int(edad_gamer)

Esto es un nuevo comando llamado **int()**, y sé que te estarás preguntando 
¿Por qué hay que colocar eso? y ¿Para qué sirve?. Te explico: sucede que el
comando **input()** es muy limitado y no sabe si lo que estás escribiendo es un
número o una palabra. entonces para el comando **input()** todo es una palabra 
incluso si son solo números, es un poco extraño esto, pero tenlo en cuenta (recuerda
que la computadora es muy limitada y no es tan inteligente como tú), todos 
sabemos que los números y las palabras son 2 cosas totalmente distintas, pero por 
suerte el comando **int()** nos permite leer una palabra y revisar si son solo 
números y nos convierte esa palabra a un número de verdad, que quiere decir esto, 
que al ser un número lo podemos comparar, sumar, restar, entre otras cosas, pero 
con las palabras no se puede hacer eso, y es por eso que **int()** es nuestro 
comando que lo arregla.

Si tratas entregarle a **int()** una palabra como 'Arturo' el programa fallará.

Analizando el más el programa podemos ver un símbolo **:** (dos puntos) después de
**edad_minima** ¿Qué es esto?, te estarás preguntando, para indicarle al programa
que ya hemos terminado con la comparación debemos terminar la línea de **if** con 
dos puntos.

La línea siguiente

.. code-block:: python

    print('Hola, eres bienvenido a nuestra crew')
 

está más adentro que la línea del **if**, esto es porque le estamos indicando al
programa que si la condición del **if** se cumple como **verdadera**, es decir, 
la **edad_gamer** es **mayor o igual** que la **edad_minima** entonces debe ejecutar
todo lo que está contenida dentro de ella, como ves visualmente la línea de **print()**
está contenida dentro de **if**. cuando el programa ya no encuentra nada dentro
de **if** entonces asume que ya no es parte de lo que debe hacer cuando la comparación
se cumple como verdadera.

entonces qué sucede si queremos hacer otra cosa, como por ejemplo 
decirle que no está admitirlo a la crew si es menor de 18 años.

para ello existe una palabra reservada que acompaña a **if** que se llama:

.. code-block:: python

    else

**else** en español significa sino, y es justamente para hacer algo sino se cumple
la condición en **if**.

así debería escribirse para nuestro ejemplo:

.. code-block:: python

    edad_minima = 18

    edad_gamer = input('Ingrese su edad: ')

    if int(edad_gamer) >= edad_minima:
        print('Hola, eres bienvenido a nuestra crew')
    else:
        print('Lo siento, nuestra crew es para mayores de 18')

simplemente el programa ejecutará todo lo contenido en **else** si no se cumple 
la condición en **if**.

Si tienes dudas o requieres una guía más personalizada contáctanos a través de 
nuestra `página de facebook Rdckgames <http://facebook.me/rdckgames>`_.
