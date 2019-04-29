Formalizando la programación
======

Hasta ahora, hemos tratado de no ser tan técnicos con los temas de programación, para que los puedas entender y llegar 
hasta acá con el conocimiento adecuado, pero ahora te vamos a enseñar conceptos y términos ocupados en programación, 
para que te sientas desde ya desarrollador y sepas cómo solucionar los problemas más comunes del desarrollo de videojuegos.

Conceptos de programación
######

En programación existen muchísimos conceptos que debemos conocer sin entrar en programar códigos, son conceptos que provienen 
de la arquitectura de softwares, pero para hacerte esto más fácil y no tengas que estar memorizando cosas. te las vamos a 
explicar aquí de una forma simple.

**Lenguaje**: Un lenguaje en programación es lo que permite a la computadora entender que queremos que ella haga, normalmente 
se les llama lenguajes formales, porque son estrictos y limitados a definiciones específicas, es decir, no le puedes escribir 
como si fuera una carta para tu amigo que está lejos, los computadores no entienden así, por eso hay que escribirlo en una 
forma que el computador entienda. existen muchos lenguajes, pero son tan parecidos entre ellos que si aprendes uno, es fácil 
aprender los demás, hay excepciones pero así como son excepciones tampoco son tan usados.

**Sintaxis**: la sintaxis es la forma en cómo se escribe en un lenguaje, es decir, que símbolos de puntuación debemos usar, 
como se deben crear las variables, como se escribe un programa en general, cuando tu programa arroja un error de sintaxis 
te está diciendo que está mal escrito algo, es como cometer una falta ortográfica o una falta gramatical.

**Programa**: El programa es lo que resulta de ejecutar el código escrito con palabras. también las personas les suelen llamar 
aplicaciones o simplemente apps.

**Código**: tambien llamado código fuente, es la versión de texto de tu programa escrito en el lenguaje formal de tu elección. 
es fácil de transportar ya que no pesa tanto como el programa, pues son solo archivos de texto.

**Compilador**: el compilador es una herramienta que nació con los lenguajes de programación y es el encargado de convertir ese 
archivo de código fuente a un programa para ejecutarlo.

**Ejecutable**: ejecutable es la versión de tu programa que te permite iniciarlo para usarlo.

**Intérprete**: un intérprete es parecido a un compilador, pero con la diferencia que no te genera un ejecutable, sino que lee 
el código fuente y lo va ejecutando línea a línea y a medida que hace eso, puedes usar el programa.

Terminología
######

Ya con lo anterior en mente puedes entender un poco más sobre programación, ahora vamos a algo más específico, que es la 
terminología usada por los programadores, esto te ayudará a entender como un programador piensa y cómo habla cuando está 
en un proceso de producción de videojuegos. Estos son algunos términos que podrás escuchar.

**Ticket**: Conjunto de especificaciones que detalla cómo se debe crear alguna funcionalidad o característica del videojuego.

**Bug**: Un error inesperado que el videojuego tiene y que no deja seguir jugándolo.

**Error**: Sinónimo de bug.

**Commit**: Es cuando un programador guarda el progreso de su trabajo en el código cuando cree que tiene una funcionalidad 
estable y probada.

**Tag**: Es cuando queremos poner colocarle una etiqueta de versión a algún punto del código del videojuego.

**Sistema**: Un conjunto de aplicaciones que funcionan para un objetivo en común.

**Conexión**: Cuando un programa establece una comunicación con otra aplicación o el exterior como internet, en los juegos 
online es muy común esto.

**Push**: Es cuando el desarrollador sube sus trabajo para compartirlo con los demás desarrolladores.

**Pull**: Es cuando el desarrollador se descarga el trabajo que han subido sus otros compañeros.

**Merge**: es cuando el desarrollador combina su trabajo con los de los demás desarrolladores.

**Deploy**: es cuando se disponibiliza los cambios del programa o videojuego para tu clientes o gamers.

Nombrado de variables
######

Las variables deben seguir una regla muy simple de nombrado:

* Debe empezar por una letra
* Puede  tener números
* Puede tener _ (guión bajo)
* No debe contener espacios
* No puede contener tildes ni ñ
* No puede usar símbolos

Te mostraremos ejemplos de nombrados válidos e inválidos para que tengas una referencia

Listado de variables admitidas como válidas.

* variable_1
* variable1
* variable_uno

Listado de variables definidas como erróneas.

* 1_variable (Empieza por número, esto no se puede hacer)
* 1variable (También empieza por un número, mal)
* 1 variable (Tiene un espacio, no debes hacer esto)
* ñandu (Tiene una ñ, no sirve como variable)
* camión (Tiene una tilde, tampoco nos sirve como variable)
* @correo (Tiene un símbolo, tampoco los símbolos los puedes usar)

Inicializar variables
######

Una de las buenas prácticas que todo programador debería seguir es definir antes sus variables y cuales van a ser sus valores 
iniciales, a esto se le llama inicializar variables, si crees que necesitas una variable debes inicializarla antes con un valor 
inicial, como por ejemplo en este código:

.. code-block:: python

    puerta_cerrada = True
    ventanas_cerradas = True
    alarma_activada = True
    luces_apagadas = True


Como puedes ver en el código anterior, parece ser que es el sistema de seguridad de una casa,
lo ideal es que esté asegurada siempre, así que inicializamos las variables la seguridad de la casa todas activadas (True), para evitarnos problemas como que un ladrón entre a robar a la casa sin que el sistema esté activado. Luego podemos usar estas variables para hacer comprobaciones

.. code-block:: python

    sistema_asegurado = False

if puerta_cerrada and ventanas_cerradas and alarma_activada and luces_apagadas:

.. code-block:: python

    sistema_asegurado = True
    if sistema_asegurado:
        print(“Su sistema esta asegurado, puede ir tranquilo”)
    else:
        print(“Debe revisar la seguridad algo no esta bien cerrado”)

Si ves cosas nuevas en este código no te preocupes más adelante te las explicaremos en detalle,
pero lo que trata de transmitir el ejemplo es que inicializando variables tienes el control total de cómo se va a comportar desde un principio tu programa.

¿Qué son los Tipos de datos?
######

En el primer artículo hablamos que una variable puede almacenar números y palabras, ahora, para que la computadora diferencie un número de una palabra u otra cosa ocupa los tipos de datos. Los tipos de datos te permiten, como programador, decidir cómo se va a ocupar una variable, es decir, si queres que se ocupe para números, si quieres que se ocupe para almacenar palabras, o algo más específico, si quieres que un número permita llevar decimales, o si una variable va a tener 2 valores solamente, verdadero o falso. a continuación vamos a listar algunos tipos de datos que podrías usar al programar videojuegos:

int: el tipo de dato int, significa que almacena números enteros, los números enteros son aquellos que en la escuela les llaman números del conjunto Z, o los números positivos y negativos. para ser mas graficos te daremos unos ejemplos:

.. code-block:: python

    ... , -9 ,-8 ,-7, -6 , -5, -4, -3 , -2, -1, 0 , 1, 2, 3, 4, 5, 6, 7, 8, 9, …

y así hasta el infinito negativo hacia la izquierda e infinito positivo hacia la derecha. Nos son útil para contar cosas, como por ejemplo cantidad de enemigos en pantalla, cantidad de artículos en un bolso, etc…

float: el tipo de dato float, tambien almacena numeros pero esto permiten llevar decimales, en la escuela les llaman números del conjunto R o reales. recuerdas el valor de PI 3.14159…, bueno este tipo de números son el tipo de dato float. tienen alta precisión y nos sirven para mover un personaje por pantalla o hacer barras de energía para los enemigos. usar sistemas de corazones para la vida del personaje, donde podemos dividir en cuatro 1 corazón (0.25 cada parte de corazón), lo importante es que estos números van separados por un punto “.” seguido del la porción decimal, esto es importante por que la coma “,” acá no funciona para números.

string: el tipo de dato string es el que te permite guardar palabras, frases, o textos muy largos, en español string significa cadena, pero el por qué se llama así, lo explicaremos más adelante. Los string deben ir siempre encerrados entre comillas (“) o cremillas (') para que el programa los entienda como este tipo de datos, si no se hace eso, el programa los tratará como variables y arrojará un error.

boolean: este tipo de dato tiene un nombre muy raro, cierto?, bueno su nombre proviene de George Boole, para resumir, el creador de este tipo de dato, a raíz de lo que se llama Álgebra Booleana, que solo acepta 2 valores, Verdadero (True) o falso (False), y por reconocimiento, le llamaron boolean, basándose en su apellido (Boole).

Con estos cuatro tipos de datos podemos hacer casi cualquier programa o videojuego, por supuesto que hay otros, pero más adelante los iremos descubriendo.

Hasta ahora los programas que puedes construir funcionan bien sin problemas, pero hay algo que nos hace falta, te coloco un ejemplo:

Digamos que tenemos un programa para hacer correr un personaje, ahora necesitamos que ese mismo programa haga correo a otros personajes también, lo lógico sería copiar el programa y agregarlo al otro personaje. pero qué pasa si tienes 1000 personajes distintos copiar 1000 veces el mismo programa para los 1000 personajes ya parece algo engorroso, y peor, digamos que no te diste cuenta que el programa tenía un error y lo debes corregir, entonces ¿estás dispuesto a corregir 1000 veces lo mismo?,  claro que no!. También podemos pensar que es una acción repetida, pero en realidad no lo es, porque no queremos que todos los personajes corran a la vez, sino que corran independientemente, así que te vamos a enseñar a como crear funciones.

¿Qué son las funciones?
######

Las funciones son porciones de código que las agrupar mediante un nombre y en vez de escribir ese código cada vez, solo usamos a la función por su nombre.

Usando funciones
######

Te vamos a mostrar y explicar cómo es una función:

.. code-block:: python

    def correr(personaje):
        # linea de codigo 
        # otra linea de codigo

    correr(personaje1) # hace correr al personaje 1
    correr(personaje2) # ahora hace corre al personaje 2

Lo importante de este ejemplo es que para que el programa sepa que quieres crear una funcion debe usar la palabra *def* seguida del nombre, y este nombre sigue la misma regla de nombrado de las variables, luego deben ir entre paréntesis parámetros de entrada de la función y finalizar con : para luego colocar el código indentado que ejecutará.

Esto es solo un ejemplo, hay cosas que debes saber también para usar funciones 

Parámetros formales y actuales

¿Qué es esto?, los parámetros son la lista de variables que podemos usar con una función además ellos nos dan una pista de qué cosas espera que le pasemos para que pueda trabajar.

existen 2 conceptos aquí

Parámetros formales: son los parámetros que están explícitos en la función, en el ejemplo anterior la función correr, permite 1 parámetro llamado personaje, y los parámetros deben ir entre paréntesis, si decides que una función no necesita pasarle parámetros, entonces los paréntesis deben ir vacíos

.. code-block:: python

    def correr(personaje):
        # hace correr al personaje
        return 1

    def fin_del_juego():
        #cerrar el programa.
        return 1

Parámetros actuales: son los parámetros que usamos para hacer trabajar a la función, un ejemplo de esto es cuando le pasamos la variable personaje1 a correr:

.. code-block:: python

    # creando función correr con 1 parámetro llamado personaje
    def correr(personaje):
        # hace correr al personaje
        return True

    # llamando a la función pasándole la variable personaje1 que representa a un personaje
    correr(personaje1)

como puedes notar, hemos creado la función y luego la hemos llamado con el parámetro personaje1, a este parámetro se le llama parámetro actual.

Las funciones también tiene la posibilidad de devolver un resultado usando la palabra return seguido de el resultado que queramos enviar, este resultado lo podemos guardar en alguna variable para luego usarla más adelante en el programa.

.. code-block:: python

    esta_corriendo = correr(personaje1)
    if esta_corriendo:
        # usar la animación que muestra al personaje corriendo

¿Qué son los Operadores?
######

Los operadores en programación nos permiten trabajar con variables para combinarlas, sumarlas, restarlas, compararlas, entre otras cosas más te mostraremos una lista de operadores por tipo de uso:

**Lógicos**: Los operadores lógicos nos permiten comparar 2 variables y saber si se cumple una condición verdadera o una condición falsa, los más comunes son and y or

El  operador lógico and comparar 2 operaciones o variables booleanas que denominaremos expresión, si ambas expresiones son verdaderas entonces and nos dirá verdadero, pero si alguna de las expresiones es falsa and nos dirá que es falso. aca va un ejemplo para que entiendas mejor

digamo que la mamá de pedrito es muy estricta y le dice a pedrito “pedrito ve a comprar al almacén 5 huevos y 2 tomates, lleva estos 2 dólares”
Pedrito va al almacén y le dice al vendedor, “quiero 5 huevos y 2 tomates tengo 2 dolares”
El señor del almacén le dice, con esos 2 dolares solo te alcanza para 2 tomate y 2 huevos y pedrito decide aceptar la oferta, e ir donde la mamá, llegado a casa la mamá lo regaña porque le pidió que trajera 5 huevos y 2 tomates exactamente, así que pedrito le dice que no pudo comprar más porque le faltaba dinero, así que la mamá de pedrito le entrega más dinero, pedrito va al almacén, compra lo que faltaba y ahora la mamá acepta la compra de pedrito.

esto es más fácil escribirlo en código que en palabras, mira este ejemplo:

.. code-block:: python

    huevo = 2
    tomate = 2

    if huevo == 5 and tomate == 2:
        # Se acepta la compra de pedrito
    else:
        # no se acepta la compra

si analizas este pequeño programa la cantidad de huevos debe ser exactamente 5 y además la cantidad de tomates exactamente 2 si alguno no se cumple entonces la mamá no acepta la compra.

pero si la mamá de pedrito le hubiese dicho traeme 5 huevos o 2 tomates, lo que le está diciendo la mamá a pedrito es que si trae 5 huevos acepta la compra o si trae 2 tomates tambien acepta la compra y si trae ambos mucho mejor acepta la compra, el caso anterior seria asi

.. code-block:: python

    huevo = 2
    tomate = 2

    if huevo == 5 or tomate == 2:
        # Se acepta la compra de pedrito
    else:
        # no se acepta la compra

En este caso 2 huevos no es igual a 5 huevos así que eso es falso, no se cumple esta condición, pero lleva 2 tomates así que en este caso se cumple una de las condiciones y por consecuencia la mama si acepta la compra.

Puedes mezclar muchas expresiones, pero debes tener en cuenta algo muy importante, la computadora siempre resolverá primero todas las expresiones que están unidas por and y luego todas las expresiones unidas por un or, es igual que la regla multiplicación y suma en la jerarquía de operaciones, primero las multiplicaciones y luego las sumas.

Condiciones
######

las condiciones en programación es lo que le llamamos en los artículos anteriores a las decisiones, la palabra adecuada es esta y aca veremos algo más interesante de ellas

usando condiciones podemos hacer varias evaluaciones a la vez, por ejemplo digamos que tenemos una nave espacial que se puede mover en varias direcciones pero solo en una direcciona a la vez, arriba, abajo, izquierda y derecha, en programación podemos hacer esto 
para asegurar que se cumpla ese comportamiento

.. code-block:: python

    if tecla == 'arriba':
        # mover nave hacia arriba
    elif tecla == 'abajo':
        # mover nave hacia abajo
    elif  tecla == 'izquierda':
        # mover nave hacia la izquierda
    elif  tecla == 'derecha':
        # mover nave hacia la derecha

como puedes ver si presionas cualquier otra tecla no se va a mover, si no presionas ninguna tecla tampoco se va a mover, si presionas 2 teclas o más en combinacion de arriba, abajo, izquierda, derecha; tampoco se moverá, solo se moverá si presionas 1 de esas teclas específicas 1 cada vez, si te haz dado cuenta esto ya parece estar programando un juego. la palabra elif nos permite evaluar otra condición totalmente distinta y revisar si la expresión es verdadera y ejecutar la porción de código que está dentro de ella.


Asignación
######

las asignaciones en programación es darle un valor a una varible

.. code-block:: python

    variable = 1

así de simple no tiene mayor complejidad, pero podemos aprovechar esta asignación para hacer algunas cosas interesantes en videojuegos, como por ejemplo llevar un puntaje y cada vez que el player recoja una moneda valla sumando 10 puntos al puntaje

.. code-block:: python

    puntaje = 0

    if recoje_moneda:
        puntaje = puntaje + 10

    print(puntaje)

A esto se le llama contador y permite ir incrementando la variable puntaje en un valor fijo, también existe una notación más simple que te ayuda a escribir más rápido

.. code-block:: python

    puntaje += 10 # incrementa en 10 el valor actual de puntaje
    puntaje -= 10 # decrementa en 10 el valor actual de puntaje
    puntaje *= 10 # multiplica por 10 el valor actual de puntaje
    puntaje /= 10 # divide en 10 el valor actual de puntaje


Ahora digamos que tenemos 2 tipos de monedas de 10 de color amarillo y de 50 de color azul, esto quedaría así:

.. code-block:: python

    puntaje = 0
    valor = 0
    if recoje_moneda_amarilla:
        valor = 10
    elif recoje_moneda_azul:
        valor =  50

    puntaje = puntaje + valor
    print(puntaje)

A esta asignación se le llama sumador o acomulador porque permite ir incrementando la variable puntaje con respecto al valor de otra variable.

La forma abreviada sería así

.. code-block:: python

    puntaje += valor # incrementa el actual puntaje en la cantidad almacenada en la variable valor
    puntaje -= valor # decrementa el actual puntaje en la cantidad almacenada en la variable valor
    puntaje *= valor # multiplica el actual puntaje por la cantidad almacenada en la variable valor
    puntaje /= valor # divide el actual puntaje en la cantidad almacenada en la variable valor



¿Qué es una cadena?
######

Las cadenas no son más que las palabras y siguen la regla del tipo de dato string, pero nos vamos a detener a explicar por qué se llaman así.
Se llaman cadenas por que las palabras son un conjunto unido de letras, llamadas en programación caracteres, pero un caracter no solo es una letra, puede ser cualquier símbolo, letra o número de tu teclado, incluso el espacio. Al ir juntos un caracter tras de otro, asemejan una cadena de metal donde un eslabón va junto uno de tras de otro. es simplemente eso y justamente la palabra string en inglés significa en español cadena.

Operaciones con cadenas

Las cadenas de texto pueden tener algunas operaciones especiales como por ejemplo podemos usarla con algunas operaciones matemáticas para hacer cosas entretenidas

**Concatenar**

.. code-block:: python

    frase = 'el pirata' + ' ' + 'es muy malo y hace arr!'
    print(frase)

El resultado sería:

.. code-block:: python

    el pirata es muy malo y hace arr!


En este ejemplo el símbolo + permite unir las 3 cadenas y guardarla en la variable frase

También puedes repetir una cadena varias veces, usando la multiplicación

.. code-block:: python

    frase = 'el pirate hace ' + 'arr! ' * 3
    print(frase)

El resultado sería:

.. code-block:: python

    el pirata hace arr! arr! arr!

Acá vemos que la cadena arr! se ha repetido 3 veces ya que lo multiplicamos por 3.

¿Qué son las tuplas y las listas?
######

Las tuplas y listas nos permiten almacenar varios valores en una sola variable, son muy parecidas entre sí pero tienen algunas diferencias.

esto es una tupla:

.. code-block:: python

    valores = (1,2,3,4,5,6,7,8,9)

las tuplas tienen la característica que no podemos cambiar sus valores una vez ya están definidos, es decir, son elementos de solo lectura, pero si podemos seguir agregando elementos a ellas, pero no quitarlos.
las listas por el contrario permiten todas las operaciones de agregar quitar mover insertar entre otras mas, esto seria una lista

.. code-block:: python

    valores = [1,2,3,4,5,6,7,8,9]

como puedes ver la diferencia es muy sutil, no son (), sino [] y con tan solo eso ya podemos hacer todas estas operaciones

si queremos convertir una una tupla en una lista puedes hacer esto

.. code-block:: python

    lista = list(tupla)

y si quieres lista en una tupla puedes hacer esto

.. code-block:: python

    tupla = tuple(lista)

Conjuntos
######

Podemos trabajar con conjuntos usando el comando set, podemos saber si existe una intersección entre 2 conjuntos o unirlos, 
ejemplos:

.. code-block:: python

    # Definimos conjunto A y B
    a = (1,2,3,4,5,6)
    b = (5,6,7,8,9,10)

    print(set(a) | set(b)) # El resultado es la unión de a y b (1,2,3,4,5,6,7,8,9,10)
    print(set(a) & set(b)) # El resultado es la intersección entre a y b (5,6)

¿Qué son los diccionarios?
######

Diccionario es una palabra muy rara en programación para comprenderla fácilmente, lo que primero se nos viene a la mente un 
diccionario de palabras con significados, pero un diccionario en programación es más parecido a un inventario, te muestro 
un ejemplo:

.. code-block:: python

    inventario = {
        'medicina' : 10,
        'municiones': 40,
        'pistola': 1,
        'granada': 3,
        'manzana': 0
    }

Operaciones con diccionarios
######

Como puedes ver es muy útil para el inventario de tu personaje en un videojuegos. Imaginemos que tu personaje encuentra una 
manzana, es tan fácil como hacer esto:

.. code-block:: python

    inventario['manzana'] += 1

Ahora tendrás una manzana en tu inventario.

te comes una manzana

.. code-block:: python

    inventario['manzana'] -= 1

Te ganas un bonus que multiplica tus medicinas al doble

.. code-block:: python

    inventario['medicina'] *= 2

Este artículo ya tiene bastante información que tendrás que estudiar, pero ya nos estamos acercando más a cómo desarrollar un 
videojuego, lo bueno que está todo en una sola página y te sirve de referencia rápida si se te olvida algo. aun así, si tienes 
dudas y necesitas una guía más personalizada contáctanos a través de 
nuestra `página de facebook Rdckgames <http://facebook.me/rdckgames>`_.

