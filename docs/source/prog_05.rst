Introducción a los objetos
======

.. image:: https://upload.wikimedia.org/wikipedia/commons/thumb/6/6e/Similar-geometric-shapes.png/640px-Similar-geometric-shapes.png
    :align: center

Todo lo que nos rodea en la vida lo podemos denominar un **objeto**, como por ejemplo 
una taza, un árbol, una mesa, una puerta, etc…, todo estos son **objetos** que interactuamos 
con ellos cotidianamente de forma normal, pero la programación parece ser algo raro que no 
se ajusta a esta realidad, es un trozo de código que hace cosas, pero no parece un **objeto** como 
lo que nosotros conocemos en la vida real, ni siquiera un programa lo podemos considerar un 
**objeto** ya que no lo podemos tocar, solo vive en la memoria de un computador y se muestra en una 
pantalla.

Pero hace muchos años atrás, por el año 1967, unos programadores quisieron cambiar esto y darle 
vida a los **objetos** con la programación y poder representar cosas como en el mundo real.

Normalmente cuando hablamos de un **objeto** lo hacemos para **objetos** inanimados, como los descritos 
anteriormente, pero también hay objetos que tienen funciones, como un vehículo o un aparato 
electrónico.

Si nos centramos en los vehículos, estos tienen varias características comunes, una de ellas es 
que tienen ruedas, hay de 1 de 2 de 3 y 4 ruedas o más, dependiendo de su uso o fin.

También tienen algunas funciones como: retroceder, avanzar, acelerar, frenar, prender luces, tocar 
la bocina, activar el limpia parabrisa, rociar con agua, cargar combustible, etc...

Hay otro vehiculos que tienen lo mismo pero le agregan algo más como un descapotable, puertas que 
se abren hacia arriba, luces que se salen desde el capó, también existen tipos de ellos como 
automáticos o mecánicos, podemos darle muchos atributos, podemos hacer que tengan muchas 
funciones, y que sean de distintos tipos, pero todos estos siguen siendo vehículos, todas estas 
características y funciones pertenecen a un vehículo, porque conocemos cómo es un vehículo.

¿Qué es la pertenencia?
######

El concepto de pertenencia de un objeto es aquello que es característico o propio de ese objeto y que no es de ningún otro más, por ejemplo que un vehículo pueda retroceder y avanzar, son característicos de un vehículo, o la cantidad de ruedas que tiene también. La pertenencia es esto, tener conciencia de qué cosas le pertenecen a un objeto y cuáles no.
Vamos a hacer un ejercicio donde colocaremos distintos elementos y vamos a definir a cuál objeto pertenecen esos elementos.

hacer los ejemplos


¿Que es un atributo?
######

Los atributos de un objeto son las características del objeto que lo distinguen de otro, 
determinan su forma y como se vé. Imagina en este punto un objeto inanimado, todas las 
características que tienen, se les denomina atributo.

¿Que es un método?
######

Cuando al objeto queremos darle vida, animarlo, sacarlo de ese estado inanimado o estático, 
debemos agregarle funciones, a estas funciones se les llama métodos, porque describe la manera 
como este debe hacer cierta acción, es decir, definen un método de hacer algo. Si te das cuenta
 he conectado la palabra función a este concepto es porque son funciones de programación que se 
 les ha dado una utilidad en los objetos.

Ya teniendo claro estos 3 conceptos, pertenencia, atributo y método podemos construir nuestro 
primer objeto, ahora ya no tendremos una función que le pasamos como parametro a un personaje 
para que corra, sino que el personaje va a tener la función de correr como parte de él.

.. code-block:: python

    #definimos la clase del objeto Personaje
    class Personaje:
        velocidad = 2  # metros / segundos

        def correr(self):
            # acciones para hacer correr al personaje

    #creando el objeto
    personaje1 = Personaje()
    personaje1.correr()

¿Que es class?
######

Como puedes ver en el código anterior nosotros hemos ocupado la palabra **class** que en español 
significa **clase**, esta palabra nos sirve para definir clases de objetos, para que te hagas 
una idea, imagina que todo lo que pensamos con tan solo tronar los dedos aparece físicamente, 
entonces pensamos en una pizza, el tipo de masa, los ingredientes, peperoni, doble queso, 
definimos todas las características que queremos degustar, tronamos los dedos, y aparece 
la pizza en la mesa, tronas nuevamente y aparece otra, y luego otra, ahora tenemos 3 pizzas de 
la misma **clase**, entonces cuando escribimos el código de la **clase** es como si estuviesemos 
pensando en todo lo que tendrá nuestro **objeto**, pero aún no se materializa. una vez que tronamos 
los dedos recién se crea el objeto y a cada objeto de la clase que hemos creado se le llama una 
**instancia**.

Volviendo al ejemplo, como puedes ver, el personaje tiene la acción correr y a la velocidad de 2 
metros por segundo, todo esto es algo que nosotros vamos ir definiendo de acuerdo a como se 
deberia comportar en un videojuego.

Es aqui donde hemos creado la instancia de objeto:

.. code-block:: python

    #creando el objeto
    personaje1 = Personaje()

Es como llamar a un comando, pero con el nombre de la clase.


¿Que es la herencia?
######

La herencia es capacidad que tienen los objetos de adoptar los atributos y funciones de otro objeto y hacerlo parte de él, además de conservar sus propias características y funciones. Para entender esto más fácil, es cuando Goku y Vegeta se fusionan, nace un nuevo personaje con los atributos y poderes de Goku y Vegeta, pero este personaje no es ni Goku ni Vegeta, es un nuevo personaje con más poder, bueno seria como la capacidad de herencia en los objetos.

.. code-block:: python

    class Saiyajin:
        def teletrasportar(self):
            #teletrasportarse

    class Goku(Saiyajin):
        ki: 10000
        def kamehameha(self):
            #lanza kamehameha
        def kaioken(self):
            #hace kaioken

    class Vegeta(Goku): # fusion de Goku con Vegeta
        ki: 180000
        def velocidad(self):
            #tecnica de velocidad

Como puedes ver la fusión de Goku con Vegeta (Vegeta adopta la forma de Goku en este caso) hizo aumentar el ki a 180.000, y le agrego la posibilidad de hacer kamehameha, y mantiene su técnica de velocidad y ambos pueden teletransportarse por que son  Saiyajin, 
com Goku es Saiyajin y Vegeta se fusionan a él, también sería un Saiyajin, aunque todos sabemos que ambos son Saiyajines, pero los objetos no saben mucho de Dragon Ball así que solo se puede hacer de esta forma.
Ahora te puedes dar cuenta la cantidad de cosas que puedes hacer con los objetos, representar una fusión de Goku con Vegeta en una forma tan simple.

Por ahora lo dejaremos simple, existen otros conceptos sobre objetos que veremos más adelante, pero ya con esto puedes empezar a trabajar con ellos de una forma simple y práctica.

¿Qué es una API?
######

Es la sigla en inglés de 'Application Programming Interface', que en español es 'Interfaz de Programación de Aplicaciones', pero bueno, entonces ¿Qué significa eso?.

para explicartelo simple una API te provee un conjunto de funciones y clases ya previamente programadas por otros programadores, que te ayudan a hacer tu programa mucho más rápido y fácil. Para que lo entienda mejor, Imagínate que quieres hacer un huevo frito, entonces no se te ocurriría nunca construir una cocina, construir el sartén, cosechar maravilla para hacer aceite, buscar pólvora para hacer fuego y finalmente criar gallinas para que te den huevos y así poder hacer un huevo frito. lo normal es comprar una cocina, comprar aceite, comprar huevos, comprar cerillas, comprar la sartén y hacer huevo frito. Las APIs serían la cocina, el sartén, el aceite, las cerillas y el huevo, nosotros solo nos dedicamos a cocinarlo, que sería nuestro programa. lo mejor es que las APIs en su mayoría no se compran, están disponibles de forma gratuita para que las ocupes sin restricciones (Pero la de Playstation tienes que pagar una licencia para poder usarla)

Usado una API
++++++

Para usar una API es mejor cuando usamos la API de un motor para videojuegos, porque con ella podemos hacer que nuestra idea de videojuego sea haga real, así que en el siguiente artículo empezaremos a crear un videojuego.

Si tienes dudas y necesitas una guía más personalizada contáctanos a través de 
nuestra `página de facebook Rdckgames <http://facebook.me/rdckgames>`_.


