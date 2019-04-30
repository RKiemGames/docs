Formalizando la programación
======

.. image:: https://upload.wikimedia.org/wikipedia/commons/5/59/Programmer_writing_code_with_Unit_Tests.jpg
    :align: center

Hasta ahora, hemos tratado de no ser tan técnicos con los temas de programación, para que los puedas entender y llegar 
hasta acá con el conocimiento adecuado, pero ahora te vamos a enseñar conceptos y términos ocupados en programación, 
para que te sientas desde ya desarrollador.

Conceptos de programación
######

En programación existen muchísimos conceptos que debemos conocer antes de programar códigos, pero para hacerte esto más fácil
y no tengas que estar memorizando cosas. te las vamos a explicar aquí de una forma simple.

**Lenguaje**: Un lenguaje en programación es lo que permite a la computadora entender que queremos que ella haga, normalmente 
se les llama lenguajes formales, porque son estrictos y limitados con definiciones específicas, es decir, no le puedes escribir 
como si fuera una carta para tu amigo que está lejos, los computadores no entienden así, por eso hay que escribirlo en una 
forma que el computador entienda. existen muchos lenguajes, pero son tan parecidos entre ellos que si aprendes uno, es fácil 
aprender los demás, hay excepciones pero así como son excepciones también son poco usados.

**Sintaxis**: La sintaxis es la forma en cómo se escribe en un lenguaje, es decir, que símbolos de puntuación debemos usar, 
como se deben crear las variables, como se escribe un programa en general, cuando tu programa arroja un error de sintaxis 
te está diciendo que está mal escrito algo, es como cometer una falta ortográfica o una falta gramatical.

**Programa**: El programa es lo que resulta de ejecutar el código escrito con palabras. también las personas les suelen llamar 
aplicaciones o simplemente apps.

**Código**: También llamado código fuente, es la versión de texto de tu programa escrito en el lenguaje formal de tu elección. 
es fácil de transportar ya que no pesa tanto como el programa, pues son solo archivos de texto.

**Compilador**: Es una herramienta que nació con los lenguajes de programación y es el encargado de convertir ese 
archivo de **código fuente** a un programa para ejecutarlo.

**Ejecutable**: Es el programa que te permite iniciarlo la aplicación para usarlo.

**Intérprete**: Es parecido a un compilador, pero con la diferencia que no te genera un ejecutable, sino que lee 
el **código fuente** y lo va ejecutando línea a línea y a medida que hace eso, puedes usar el programa.


Terminología
######

Ya con lo anterior en mente, puedes entender un poco más sobre programación, ahora vamos a algo más específico, que es la 
terminología usada por los programadores, esto te ayudará a entender cómo un programador piensa y habla cuando está 
en un proceso de producción de desarrollo de un programa o de un videojuegos. Estos son algunos términos que podrás escuchar.

**Ticket**: Conjunto de especificaciones que detalla cómo se debe crear alguna funcionalidad o característica del videojuego
o programa.

**Bug**: Un error inesperado que el videojuego o programa tiene y que no deja seguir jugándolo u usandolo.

**Error**: Sinónimo de bug.

**Git**: Es un software open source que te permite llevar un control de los cambios que haces en tu codigo, una de las 
ventajas es que no te tienes que preocupar de estar haciendo copias actualizada de tus archivos, git te permite volver a un
atras en el timpo de tu código, cuando este fue distinto y compararlo con lo actual. tiene un conjunto de herramientas que te
facilitan este proceso. 

**Commit**: Es cuando un programador guarda el progreso de su trabajo  en el código con **git** y cree que tiene una 
funcionalidad estable y probada.

**Tag**: Es cuando queremos poner una etiqueta de versión a algún **commit** del código del videojuego.

**Push**: Es cuando el desarrollador sube a un repositorio remoto de **git** sus trabajo para compartirlo con los demás 
desarrolladores.

**Pull**: Es cuando el desarrollador descarga el trabajo que han subido al repositorio remoto de 
**git** sus otros compañeros.

**Merge**: Es cuando el desarrollador combina su trabajo con el de los demás desarrolladores usando **git**.

**QA**: Es el proceso de hacer pruebas a un programa o videojuego, con el objetivo de **asegurar la calidad** de este.

**Deploy**: Es cuando se disponibiliza las actualizaciones del programa o videojuego para tu clientes o gamers o se sube
a una tienda de aplicaciones de forma pública.

**Sistema**: Un conjunto de aplicaciones que funcionan para un objetivo en común.

**Conexión**: Cuando un programa establece una comunicación con otra aplicación o el exterior como internet, en los juegos 
online es muy común esto.

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

Listado de variables válidas.

* variable_1
* variable1
* variable_uno

Listado de variables erróneas.

* 1_variable (Empieza por número, esto no se puede hacer)
* 1variable (También empieza por un número, mal!)
* variable 1 (Tiene un espacio, no debes hacer esto)
* ñandu (Tiene una ñ, no sirve como variable)
* camión (Tiene una tilde, tampoco nos sirve como variable)
* @correo (Tiene un símbolo, los símbolos no los puedes usar)

Inicializar variables
######

Una de las buenas prácticas que todo programador debería seguir es definir antes sus variables y cuales van a ser sus valores 
iniciales, a esto se le llama inicializar variables, si crees que necesitas una variable debes inicializarla antes de usarla 
con un valor inicial, como por ejemplo en este código:

.. code-block:: python

    puerta_cerrada = True
    ventanas_cerradas = True
    alarma_activada = True
    luces_apagadas = True


Como puedes ver en el código anterior, parece ser que es el sistema de seguridad de una casa,
lo ideal es que esté asegurada siempre, así que inicializamos las variables para la seguridad de la casa, quedando todas 
activadas (True), para evitarnos problemas como que un ladrón entre a robar a la casa sin que el sistema esté activado. 
Luego podemos usar estas variables para hacer comprobaciones.

.. code-block:: python
    
    sistema_asegurado = False

    if puerta_cerrada and ventanas_cerradas and alarma_activada and luces_apagadas:
        sistema_asegurado = True

    if sistema_asegurado:
        print("Su sistema esta asegurado, puede ir tranquilo")
    else:
        print("Debe revisar la seguridad algo no esta bien cerrado")

Si notas cosas nuevas en este código no te preocupes más adelante te las explicaremos en detalle, pero lo que trata de 
transmitir el ejemplo es que inicializando variables tienes el control total de cómo se va a comportar desde un principio 
tu programa.

¿Qué son los Tipos de datos?
######

En el primer artículo hablamos que una variable puede almacenar números y palabras, ahora, para que la computadora diferencie 
un número de una palabra u otra cosa ocupa los **tipos de datos**. Los **tipos de datos** te permiten, como programador, decidir 
cómo se va a ocupar una variable, es decir, si queres que se ocupe para números, si quieres que se ocupe para almacenar palabras, 
o por ejemplo algo más específico seria que un número permita llevar decimales, o si una variable va a tener 2 valores solamente,
**verdadero** o **falso**. A continuación vamos a listar algunos tipos de datos que normamente se usan al programar videojuegos:

**int**: El tipo de dato **int**, significa que almacena números enteros, los números enteros son aquellos que les llaman números 
del conjunto Z, o los números positivos y negativos. para ser mas gráficos te daremos uno ejemplo:

.. code-block:: python

    ... , -9 ,-8 ,-7, -6 , -5, -4, -3 , -2, -1, 0 , 1, 2, 3, 4, 5, 6, 7, 8, 9, ...

.. code-block:: python

    variable_numero = 1
    variable_otro_numero = 10000

Y así, hasta el infinito negativo hacia la izquierda e infinito positivo hacia la derecha. Nos son útil para contar cosas, como 
por ejemplo cantidad de enemigos en pantalla, cantidad de artículos en un bolso, etc...

**float**: El tipo de dato **float**, también almacena números pero este permiten llevar decimales, se les llaman números del 
conjunto R o reales. Recuerdas el valor de PI 3.14159..., bueno este tipo de números son del tipo de dato **float**. tienen alta 
precisión y nos sirven para mover un personaje por pantalla o hacer barras de energía para los enemigos. Crear un sistemas de vida
del personaje, donde podemos dividir en cuatro 1 corazón (0.25 cada parte de corazón), lo importante es que estos números van 
separados por un punto "." seguido del la porción decimal, esto es importante por que la coma "," acá no funciona para números.
Estos son ejemplos de variables **float**.

.. code-block:: python

    variable1 = 1.35
    variable2 = 2.0
    variable3 = float(3) # convertimos un numero **int** en **float**


**string**: el tipo de dato **string** es el que te permite guardar palabras, frases, o textos muy largos, en español **string**
significa cadena, pero el por qué se llama así, lo explicaremos más adelante. Los **string** deben ir siempre encerrados entre 
comillas (") o cremillas (') para que el programa los entienda como tal, si no se hace eso, el programa los tratará como variables
y arrojará un error o hara que tu programa o videojuego funcione mal.

.. code-block:: python

    variable_string1 = 'esto es un texto'
    variable_string2 = "esto es otro texto"

**bool**: Este tipo de dato tiene un nombre muy raro, cierto?, bueno su nombre proviene de George Boole, para resumir, 
el creador de este tipo de dato, a raíz de lo que se llama Álgebra Booleana, que solo acepta 2 valores, Verdadero (**True**) o 
falso (**False**), y para reconocer su obra, le llamaron **Boolean**, basándose en su apellido (Boole), y por 
consecuencia **bool**.

.. code-block:: python

    variable_booleana = True
    activo = False

Con estos cuatro **tipos de datos** podemos hacer casi cualquier programa o videojuego, por supuesto que hay otros, pero más 
adelante los iremos descubriendo.

Hasta ahora los programas que puedes construir funcionan bien sin problemas, pero hay algo que nos hace falta,
por ejemplo:

Digamos que queremos hacer un programa que haga correr a un personaje, ahora necesitamos que ese mismo programa haga correo a 
otros personajes también, lo lógico sería copiar el programa y agregarlo al otro personaje. pero qué pasa si tienes 1000 
personajes distintos copiar 1000 veces el mismo programa para los 1000 personajes ya parece algo engorroso, y peor, digamos 
que no te diste cuenta que el programa tenía un error y lo debes corregir, entonces ¿estás dispuesto a corregir 1000 veces 
lo mismo?, claro que no!. También podemos pensar que es una acción repetida, pero en realidad no lo es, porque no queremos que 
todos los personajes corran a la vez, sino que corran independientemente, así que te vamos a enseñar a como crear **funciones**.

¿Qué son las funciones?
######

Las funciones son porciones de código que las agrupar mediante un nombre y en vez de escribir ese código cada vez, solo usamos a 
la función por su nombre.

Usando funciones
++++++

Te vamos a mostrar y explicar cómo es una función:

.. code-block:: python

    def correr(personaje):
        # muchas linea de codigo que hacen correr a un personaje
        return True #termina de ejeutar la funcion y devuelve el valor **True**

    correr(personaje1) # hace correr al personaje 1
    correr(personaje2) # ahora hace corre al personaje 2

Lo importante de este ejemplo es que para que el programa sepa que quieres crear una funcion debe usar la palabra **def** 
seguida del nombre, y este nombre sigue la misma regla de nombrado de las variables, luego deben ir entre paréntesis 
parámetros de entrada de la función y finalizar con **:**, para luego colocar el código indentado que se ejecutará.

Esto es solo un ejemplo, hay cosas que debes saber también para usar funciones 

Parámetros formales y actuales
++++++

Los parámetros son la lista de variables que podemos usar con una función, además ellos nos dan una pista de qué cosas espera que
le entreguemos para que pueda trabajar.

existen 2 conceptos aquí

**Parámetros formales**: Son los parámetros que están explícitos en la función, en el ejemplo anterior la función correr, permite
1 parámetro llamado **personaje**, y los parámetros deben ir entre paréntesis, si decides que una función no necesita parámetros, 
entonces los paréntesis deben ir vacíos:

.. code-block:: python

    def correr(personaje):
        # hace correr al personaje
        return True

    def fin_del_juego():
        #cerrar el programa.
        return 0

**Parámetros actuales**: Son los parámetros que usamos para hacer trabajar a la función, un ejemplo de esto es cuando le pasamos 
la variable **personaje1** a la funcion **correr**:

.. code-block:: python

    # creando función correr con 1 parámetro llamado personaje
    def correr(personaje):
        # hace correr al personaje
        return True

    # llamando a la función con la variable personaje1 que representa a un personaje
    correr(personaje1)

Como puedes notar, hemos creado la función y luego la hemos llamado con el parámetro **personaje1**, a este parámetro se le 
llama **parámetro actual**.

Las funciones también tiene la posibilidad de devolver un resultado usando la palabra **return** seguido de el resultado que 
queramos enviar, este resultado lo podemos guardar en alguna variable para luego usarla más adelante en el programa.

.. code-block:: python

    esta_corriendo = correr(personaje1)
    if esta_corriendo:
        # usar la animación que muestra al personaje corriendo

¿Qué son los Operadores?
######

Ya habiamos hablado un poco de ellos en `Programando decisiones </prog_02.html#que-son-los-operadores>`_. esos operadores como
indicaba el artículo sirven para comparar.

En este apartado explicaremos en detalle sobre los demás:

**Matemáticos**: Estos operadores son los más comunes y de toda la vida, la suma, resta, multiplicacion y la división
Un ejemplo:

.. code-block:: python

    suma = 1 + 2
    resta = 10 - 7
    multiplicacion = 4 * 5
    division = 25 / 5

Tambien podemos ver otros operadores especiales muy usados

.. code-block:: python

    resto_de_la_division = 5 % 2 # esto da como resultado 1

.. code-block:: python

    elevado = 2 ** 5 # 2 elevado a 5

Existen otros operadores matemáticos más avanzados pero poco comunes, que no cubriremos aún.

**Booleanos**: Nos permiten comparar 2 variables **booleanas** o comparaciones, que le llamaremos expresión 
y saber si se cumple una condición verdadera o una condición falsa, los más comunes son **and** y **or**

El operador booleano **and** comparar 2 expresiones, si ambas son verdaderas entonces **and** nos dirá verdadero, pero si 
alguna de las expresiones es falsa **and** nos dirá que es falso. aca va un ejemplo para que entiendas mejor

Digamo que la Mamá de Pedrito es muy estricta y le dice a Pedrito "Pedrito vé a comprar al almacén 5 huevos y 2 tomates, lleva 
estos 2 dólares". Pedrito va al almacén y le dice al vendedor, "quiero 5 huevos y 2 tomates, tengo 2 dolares", el señor del 
almacén le dice, "con esos 2 dolares solo te alcanza para 2 tomate y 2 huevos" y Pedrito decide aceptar la oferta, e ir donde la 
Mamá. Llegado a casa la Mamá lo regaña porque le pidió que trajera 5 huevos y 2 tomates exactamente, así que Pedrito le dice que 
no pudo comprar más porque le faltaba dinero, así que la mamá de pedrito le entrega más dinero, Pedrito va al almacén, compra lo 
que faltaba y ahora la mamá acepta la compra de Pedrito.

Esto es más fácil escribirlo en código que en palabras, mira este ejemplo:

.. code-block:: python

    huevo = 2
    tomate = 2

    if huevo == 5 and tomate == 2:
        # Se acepta la compra de Pedrito
    else:
        # no se acepta la compra

Si analizas este pequeño programa la cantidad de huevos debe ser exactamente 5 y además la cantidad de tomates exactamente 2 
si alguno no se cumple entonces la Mamá no acepta la compra, pero si la mamá de pedrito le hubiese dicho traeme 5 huevos o 
2 tomates, lo que le está diciendo la Mamá a Pedrito es que si trae 5 huevos acepta la compra o si trae 2 tomates tambien acepta
la compra y si trae ambos mucho mejor, acepta la compra, este caso sería así:

.. code-block:: python

    huevo = 2
    tomate = 2

    if huevo == 5 or tomate == 2:
        # Se acepta la compra de pedrito
    else:
        # no se acepta la compra

En este caso 2 huevos no es igual a 5 huevos, así que eso es falso, no se cumple esta condición, pero lleva 2 tomates así que en 
este caso se cumple una de las condiciones y por consecuencia la Mamá si acepta la compra.

Puedes mezclar muchas expresiones, pero debes tener en cuenta algo muy importante, la computadora siempre resolverá primero todas
las expresiones que están unidas por **and** y luego todas las expresiones unidas por **or**, es igual que la regla multiplicación
y suma en la jerarquía de operaciones, primero las multiplicaciones y luego las sumas.

Existen otros operadores boleanos más avanzados pero poco comunes, que no cubriremos aún.

Condiciones
######

Las condiciones en programación es lo que le llamamos en los artículos anteriores **decisiones**. La palabra adecuada es esta y 
aca veremos algo más interesante de ellas.

Usando condiciones podemos hacer varias comparaciones a la vez, por ejemplo digamos que tenemos una nave espacial que se puede 
mover en varias direcciones pero solo en una direcciona a la vez, arriba, abajo, izquierda y derecha, en programación podemos 
hacer esto para asegurar que se cumpla ese comportamiento:

.. code-block:: python

    if tecla == 'arriba':
        # mover nave hacia arriba
    elif tecla == 'abajo':
        # mover nave hacia abajo
    elif  tecla == 'izquierda':
        # mover nave hacia la izquierda
    elif  tecla == 'derecha':
        # mover nave hacia la derecha

como puedes ver si presionas cualquier otra tecla no se va a mover, si no presionas ninguna tecla tampoco se va a mover, 
si presionas 2 teclas o más en combinacion de arriba, abajo, izquierda, derecha; tampoco se moverá, solo se moverá si presionas 
1 de esas teclas específicas 1 cada vez, si te haz dado cuenta esto ya parece estar programando un juego. la palabra **elif** nos 
permite evaluar otra condición totalmente distinta y revisar si la expresión es verdadera y ejecutar la porción de código que está
dentro de ella.


Asignación
######

Las asignaciones en programación, significa darle un valor a una varible

.. code-block:: python

    variable = 1

así de simple no tiene mayor complejidad, pero podemos aprovechar esta asignación para hacer algunas cosas interesantes en 
videojuegos, como por ejemplo llevar un puntaje y cada vez que el player recoja una moneda valla sumando 10 puntos al puntaje:

.. code-block:: python

    puntaje = 0

    if recoje_moneda:
        puntaje = puntaje + 10

    print(puntaje)

A esto se le llama **contador** y permite ir incrementando la variable puntaje en un valor fijo, ahora te explicamos como funciona
en este ejemplo iniciamos la variable **puntaje** en **0** luego cuando el programa intenta ejecutar `puntaje = puntaje + 10`
lo que hace primero es resolver el código que esta a la derecha del simbolo igual (=), para caso necesita tomar el valor que esta
en la variable **puntaje** y sumarlo con el numero 10, en ete punto la variable **puntaje** aun vale **0** entonces la suma que 
realiza es **0 + 10** dando como resultado **10**, luego cuando la computadora ya tiene el resultado lo asigna a la variable
**puntaje** quedando ahora el valor de la variable **puntaje** en **10**, si vuelves a recojer una moneda, como la variable
**puntaje** ahora vale **10** le sumara **10** y quedara con el valor **20** y asi si susivamente tantas monedas recojas.


También existe una notación más simple que te ayuda a escribir más rápido

.. code-block:: python

    puntaje += 10 # incrementa en 10 el valor actual de puntaje
    puntaje -= 10 # decrementa en 10 el valor actual de puntaje
    puntaje *= 10 # multiplica por 10 el valor actual de puntaje
    puntaje /= 10 # divide en 10 el valor actual de puntaje


Ahora digamos que tenemos 2 tipos de monedas de **10** de color **amarillo** y de **50** de color **azul**, esto quedaría así:

.. code-block:: python

    puntaje = 0
    valor = 0
    if recoje_moneda_amarilla:
        valor = 10
    elif recoje_moneda_azul:
        valor =  50

    puntaje = puntaje + valor
    print(puntaje)

A esta asignación se le llama **sumador** o **acomulador** porque permite ir incrementando la variable **puntaje** con respecto 
al valor de otra variable. la forma de resolver esto es igual siempre, primero lo que esta a la derecha del igual (=) y luego
lo asigna a la variable.

La forma abreviada sería así:

.. code-block:: python

    puntaje += valor # incrementa el actual puntaje en la cantidad almacenada en la variable valor
    puntaje -= valor # decrementa el actual puntaje en la cantidad almacenada en la variable valor
    puntaje *= valor # multiplica el actual puntaje por la cantidad almacenada en la variable valor
    puntaje /= valor # divide el actual puntaje en la cantidad almacenada en la variable valor


¿Qué es una cadena?
######

Las cadenas no son más que las palabras y siguen la regla del tipo de dato **string**, pero nos vamos a detener a explicar porqué 
se llaman así. Se llaman **cadenas** porque las palabras son un conjunto unido de letras, llamadas en programación caracteres, 
pero un caracter no solo es una letra, puede ser cualquier símbolo, letra o número de tu teclado, incluso el espacio. Al ir juntos
un caracter tras de otro, asemejan una cadena de metal donde un eslabón va junto uno de tras de otro. es simplemente eso y 
justamente la palabra **string** en inglés significa en español **cadena**.

Operaciones con Cadenas
++++++

Las cadenas de texto pueden tener algunas operaciones especiales como por ejemplo podemos usarla con algunas operaciones 
matemáticas para hacer cosas entretenidas:

Concatenar
++++++

.. code-block:: python

    frase = 'el pirata' + ' ' + 'es muy malo y hace arr!'
    print(frase)

El resultado sería:

.. code-block:: python

    el pirata es muy malo y hace arr!


En este ejemplo el símbolo + permite unir las 3 cadenas y guardarla en la variable **frase**

También puedes repetir una cadena varias veces, usando la multiplicación

.. code-block:: python

    frase = 'el pirate hace ' + 'arr! ' * 3
    print(frase)

El resultado sería:

.. code-block:: python

    el pirata hace arr! arr! arr!

Acá vemos que la cadena **arr!** se ha repetido **3** veces ya que lo multiplicamos por 3.

¿Qué son las tuplas y las listas?
######

Las tuplas y listas nos permiten almacenar varios valores en una sola variable, son muy parecidas entre sí pero tienen algunas 
diferencias.

esto es una tupla:

.. code-block:: python

    valores = (1,2,3,4,5,6,7,8,9)

Las tuplas tienen la característica que no podemos cambiar sus valores una vez ya están definidos, es decir, son elementos de solo
lectura, pero sí podemos seguir agregando elementos a ellas, pero no quitarlos.

Las listas por el contrario permiten todas las operaciones de agregar quitar mover insertar entre otras mas, esto seria una 
lista:

.. code-block:: python

    valores = [1,2,3,4,5,6,7,8,9]

Como puedes ver la diferencia es muy sutil, en las tuplas usas (), y en las listas usas [] y con tan solo eso ya podemos hacer 
todas las operaciones siguientes:

Si queremos convertir una una tupla en una lista puedes hacer esto

.. code-block:: python

    lista = list(tupla)

Y si quieres convertir lista en una tupla puedes hacer esto

.. code-block:: python

    tupla = tuple(lista)

Si queremos acceder a un valor dentro de una tupla o lista, debemos acceder al valor dependiendo de la posicion que se encuentre
dentro de la lista o tupla, en el ejemplo anterior tenemos números del 1 al 9 entonces podemos inferir que la pisición del 5 es
la quinta posición. Las tuplas y listas para cada posición les da un numero de índice que parte en 0, es decir a la posicion:
la posicion 1 es el índice 0, la 2 es el índice 1, la 3 es el índice 2, y asi susesivamente, asi que para acceder a la posicion 
5 debemos conocer su índice, como te puedes dar cuenta el índice siempre es 1 menos que su posición entonces la posicion 4, seria
el índice 4. ahora ya podemos acceder al valor 5 que es lo que queremos, y se hace de esta forma:

.. code-block:: python

    valor_lista = lista[4]
    valor_tupla = tupla[4]

Tambien podemos agregar elementos a una lista:

.. code-block:: python

    lista.append(10)

Quitar elementos de una lista:

.. code-block:: python

    lista.remove(10)

Sacar el último elemento de una lista y guardarlo en una variable:

.. code-block:: python

    elemento = lista.pop() # Al quitarlo este desaparece de la lista.

Sacar el primer elemento de una lista y guardarlo en una variable:

.. code-block:: python

    elemento = lista.pop(0) # Al quitarlo este desaparece de la lista.


Sacar el quinto elemento de una lista y guardarlo en una variable:

.. code-block:: python

    elemento = lista.pop(4) # Al quitarlo este desaparece de la lista.

Inserta un elemento en la quinta posicion:

.. code-block:: python

    valor = 5
    indice = 4
    lista.insert(indice, valor) # agrega el numero 5 en la posición del indice 4

Saber cuantos elementos tiene una lista o tupla:

.. code-block:: python

    contar_lista = len(lista)
    contar_tupla = len(tupla)

Invertir el orden de los elementos de una lista:

.. code-block:: python

    lista.reverse()

Ordenar los elementos de una lista de menor a mayor:

.. code-block:: python

    lista.sort()

Conjuntos
++++++

Usando listas o tuplas podemos trabajar con conjuntos usando el comando **set**, podemos saber si existe una intersección entre 
2 listas o tuplas o unirlas.

Ejemplos:

.. code-block:: python

    # Definimos conjunto A y B
    a = (1,2,3,4,5,6)
    b = (5,6,7,8,9,10)

    print(set(a) | set(b)) # El resultado es la unión de a y b (1,2,3,4,5,6,7,8,9,10)
    print(set(a) & set(b)) # El resultado es la intersección entre a y b (5,6)

Esta son las operaciones más comunes que puedes realizar en listas y tuplas, existen otras más avanzadas, pero no las 
cubriremos ya que no son tan frecuentemente utilizadas.

¿Qué son los Diccionarios?
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
++++++

Como puedes ver es muy útil para el inventario de tu personaje en un videojuego. Imaginemos que tu personaje encuentra una 
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

Como puedes notar, crear diccionarios es muy simple.

Este artículo ya tiene bastante información que tendrás que estudiar, pero ya nos estamos acercando más a cómo desarrollar un 
videojuego, lo bueno que está todo en una sola página y te sirve de referencia rápida si se te olvida algo. aun así, si tienes 
dudas y necesitas una guía más personalizada contáctanos a través de 
nuestra `página de facebook Rdckgames <http://facebook.me/rdckgames>`_.

