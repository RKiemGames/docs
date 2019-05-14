Introducción a la programación
######

Creando un formulario de registro

Quizás un formulario de registro no tiene mucha relación con videojuegos
pero, te puede servir de mucho si luego quieres aplicarlo para que tus gamers
ingresen sus datos en un registro de récords o ingresen su seudónimo para iniciar 
una partida en una crew.

¿Qué aprenderé?
======

 1. Conocer qué son las variables.
 2. Maneras de ingresar información.
 3. Mostrar la información.

¿Qué necesito?
======

Para empezar a programar necesitas una aplicación que pueda interpretar 
tus programas, en esta guía de ejemplo usaremos un programa llamado **Thonny** 
y lo puedes descargar desde https://thonny.org, es gratuito y no necesitas 
nada más, está disponible para **Windows**, **Mac** o **Linux**.

.. image:: https://lh3.googleusercontent.com/PxjHlTnLQ69aecmR5E856Mj_ybfASOlvrXvByHf4ZTGaskj646exYfZk57dAkkpQaZJOBaoRJ63GQv_UBnkS7FseqD7w8V5J1ecAUpGMPGH6wYc4VQ-JMgxSivb20M1dqMCeD9qvklr4pQFRggYRcq0LobFoyk2ZHTCoYcioJNlC7vLhSiqR16shhKkiG5jOLPh03IGfekgUo6MjfpQO77sNpD0H-SNy8zStFOBNl7UbQWkJI042BU-Zg0W1T8wsdMkVQ0VAOxOsr59da6mfPKqUlSCmh0ClveeCVJk3Ov5HgCyRvz5pScuBxEz1VOof1JoJMA5XKgQjErGKRW_hNMuIehKxmxUjUubM5hWoi_idawa6nEMeuxy44_YVvguBfmq-8u_B5L2f-XD9hqlLnjTWwIaeh9dQLxIAoRe3GLKdE4K64TQ3w8WsdoqQVI46kMMQbCA2VtNhJflesgoKuc1e37Ryl5O_oFUluY96X22ubzHXBxZH9b542VnVCky9OttYsIafwKUSaRhLiJQKGpDrgD5y7r6OoMux_MXCzivfj8WmzxU7j07d8nqdtaAD6peG2OQYC5djWaLVk0urae3ZjyslFhbf3szETxo-rx9G1SsTr60ORusSXlgvWzjcs-c-fcIS--U8Cl9YgRgo-Ulqn5eKzuUgnFqFIwp8T5ppsGrcfLLfOkpMaypwQ6lZLoGxSc3NrpzCsQ6c6w8JVeZl=w479-h405-no?pageId=102396338536413597633

La interfaz de **Thonny** es muy simple, como puedes ver en la parte superior 
tienes una barra de herramientas, que te permitirán: crear, guardar y ejecutar 
el programa, entre otras opciones no importantes en este punto.

Se divide en 2 partes, la parte superior donde escribiremos el programa que 
lleva como título ``<untitled>`` que indica que el archivo aún no ha sido 
guardado con un nombre, luego que guardemos el archivo aparecerá aquí su nombre.

En la parte inferior tenemos una ventana llamada **Shell** donde mostrará la 
ejecución de nuestro programa y podremos interactuar con él a través de ella.

¿Qué son las variables?
======

En programación una **variable** es como una caja pequeña donde podemos guardar 
una cosa, existen de distintos tamaños, para guardar distinto tipo de cosas. 
Imagina ahora que esas cajas las etiquetamos para poder saber qué tienen en su 
interior, esto es el **nombre de la variable**.

**En resumen**, una **variable** es donde podemos guardar **algo** y tiene un 
**nombre** para reconocerla. Ese **algo** que podemos guardar podría ser una 
**palabra** o un **número**.

¿Cómo se crea una variable?
======

Esto es muy sencillo, debes escoger que vas a aguardar en la variable y luego 
definir un nombre. Veamos un ejemplo: digamos que queremos guardar un **número**,
los años de edad de una persona, entonces nombraremos a la variable **edad**

.. code-block:: python

    edad = 21

Así es como se escribe en programación. Ahora te estarás preguntando 
¿Por qué el símbolo **igual**?, esto es confuso al principio, ya que 
naturalmente ocupamos el símbolo **igual** para dar un resultado, pero en 
programación el símbolo **igual** nos sirve para indicar que queremos guardar 
**algo** en la **variable**, En este caso, **algo** es el número **21**, que 
representa la edad de una persona y la estamos guardando en la variable 
llamada **edad**.

Continuando con el ejercicio, imagina qué otros datos debería tener una persona, 
empecemos por **nombre** y **apellido**, ¿Qué otros más se te ocurren?.

El **nombre** o **apellido** de una persona es como una palabra, ya que está 
compuesto de letras. en programación para indicar que es una palabra, debemos 
encerrar esa palabra entre comillas.

.. code-block:: python

    nombre = 'Arturo'

| CUIDADO: Para estos ejemplos, evita usar letras con tilde o ñ

y hacemos esto para distinguirlo de una **variable**.

Ahora abre la aplicación **thonny** y por cada línea, empieza a crear las 
variables para los datos de una persona cualquiera (por ejemplo, pueden ser tus 
datos).

.. code-block:: python

    nombre = 'Arturo'
    apellido = 'Lara'
    edad = 21

Guarda el archivo con el nombre **example01.py** en tu escritorio.

.. image:: https://lh3.googleusercontent.com/Wycr7bJwFLZf-pK_ttdgxWMXF-oTeWtHste6GZcw3NjFfA8ncXX54SlHp-Osm-PIGNrTFyEumWpso7iPBD4xFcXif4GHvrOc7C6Twt3VUGYpPggYPZlVMwF0SZIBGiiGa4bbcWT0DjuIy4RdFtfiIUuHdTWEpTVG5G8nz-GZ5MVW2dqJ1ZYSoOD0tXqRGZwuatnKxF9aC7EHEDE483dbsbl_Im8l-WY8YVtVsyaFtWUZ8_fBv-RUBXULLzKKbQFmmCiUSckt4-nm7mxpaxbM1cDzBuZO7T4QpojojFq0yb517WEekiCwB6B86yPwg_faTKDqkIckkehsaxBCsgATAMxuaYZNj5EFpRXKXKJ9yqtqCxrQbdJeluz2MJMjWX4Up9ZDDxOaGNS6QHaptVOJq_kcsGb7CI51G6iqkMkpfK0VlvCwvWnym8W01LG7DtQLhyLCZ_0v0m9uVYIOc7cC6KdoXp9uutmZU7u-FRE0dFFLE-lmzcb8envjHP_FLMznSXi8XXoPqv_ClWVRhxhhq6Nn_tx50jEAoUBwNcFigwG5u1BmyTpVtW_z0qjTbJbtHPy4R8kFAVJ1cpMmPv5qZzWlp0f-eoaGw7HOCVyyKuE3LmObx17tOQs6XfAvRa855R62y4CO_VPk2XgQUTRuF1jDFIWbVdzDG1hr1yKfJbEhiFI1VbzohwKjDm8vA40ZhUTUsOcJuNC-YkZvIczq2lKT=w476-h65-no

¿Cómo hago ahora que el programa funcione?
======

Luego que ya escribiste tus variables vamos a mostrar los datos en pantalla, 
esto es lo que hacen los programas comúnmente, para ello los programadores más 
experimentados han trabajado arduamente para ayudarnos a hacer esta tarea y que 
sea muy fácil, han creado los **comandos** que son herramientas, así como un 
carpintero tiene un martillo para clavar clavos, los comandos son herramientas 
para usar con nuestras variables. el comando que vamos a usar en este caso está 
pensado para **imprimir en la pantalla** y se llama:

.. code-block:: python

    print()

Los comando se distinguen de las variables porque llevan **paréntesis** y dentro 
de esos paréntesis vamos a colocar nuestra variable para que el comando actúe. 
Ahora te mostraremos como usar **print()**

**print()** acepta que le mandes a imprimir varias cosas a la vez, mientras las 
separes por medio de **comas**

.. code-block:: python

    print('Nombre:', nombre)

En este ejemplo le estamos indicando al comando **print()** que mande a la 
pantalla la palabra **'Nombre:'** seguido del contenido de la variable **nombre**

El resultado será mostrado en pantalla de la siguiente forma:

.. code-block:: python

    Nombre: Arturo

Ahora en cada línea del archivo agrega los comandos **print()** para tus otras 
variables, al finalizar deberías tener algo similar a esto:

.. code-block:: python

    nombre = 'Arturo'
    apellido = 'Lara'
    edad = 21
    print('Nombre:', nombre)
    print('Apellido:', apellido)
    print('Edad:', edad)

presiona el botón **play** de **thonny**.

.. image:: https://lh3.googleusercontent.com/yJpuwv9r0YYW4CYfEU0kaLeV34IGAqfQWC72rB_n4qiCld13tlv87e1yHTHQpm6px5cvmx-N5FqO48VQCeRU3tw_hd9SrBPnprN-pmMUIIYzmOcXTATeYvbIfm6PSpGmk2PwBAQEbOQjXSQcGuEpqW2NQwiDZ1iubKWFg_e414eM38_qIw6mL90XZSxfhwdI2Yl3VAlrk5dDwX73UXgund6vDArhb1lES5DTs11cm3YFCMSF2B92FOEJuByjD5oAVqnBAar7wPy27cxnZCfwsN84voChDjOHy3gQmN1GmK8v9isEvcme_QIiFX7nVnjNW9az1l_u8ZfxxK9kkzOAAMp77YObQIJUnLr8HnYuiGne5DlUEpfrrYveFiFtZqB1nUZtok_fmRHQXQXF4ZskGttGeuvZ4Q3Esz3sLS01kILlaLS5d8SHo2cgWR14YeoxeBZvDHFPmR6Lzab7mRqnUKb-W5DUVQrQELgncBxTOgQ9e62qEz8A5M4Sq5-6xfogSaUOgfUrujH0eA5HZuUbKjs9NgZyoXud7ob7OewxJ9OPAoRVsM24QsdbSGXlu4nM6scUrgQdx-jG8zQSjgXYT3629g1LggUcWpzQeFGcKbeYZgUfYnXDDnabCrsVztUTM4Wsg5tFOa5sgb-_QC9mH3FXFT6HuVqKQ7WGNIhCmxQP7PHFnAKuelhfSdTe4daLgcitMou-e44LGvGUhKAZGg1d=w478-h68-no?pageId=102396338536413597633

y el resultado debería ser algo similar a esto en la ventana **Shell** de 
**thonny**.

.. code-block:: python

    Nombre: Arturo
    Apellido: Lara
    Edad: 21

Ya en este punto tienes el 90% del programa terminado, puedes ver que funciona y 
muestra los resultados como se espera. pero sería más interesante si los datos 
pudiésemos ingresarlos por medio del teclado, que es lo que comúnmente hacemos 
cuando llenamos un formulario de registro. para esto vamos a usar otro 
comando llamado

.. code-block:: python

    input()

Este comando espera a que la persona escriba algo en el teclado y presione 
**ENTER**, este comando toma lo que ingresó la persona y lo podemos guardar en 
una **variable**, además podemos decirle al comando que imprima en pantalla 
algún mensaje para indicarle a la persona qué debe escribir, como por ejemplo:

.. code-block:: python

    nombre = input('Ingrese su Nombre: ')

El resultado en pantalla se mostrará:

.. code-block:: python

    Ingrese su Nombre: 

Se quedará el cursor esperando a que la persona escriba en el teclado su nombre 
y presione **ENTER**

Intenta hacer esto con tus otras variables, deberías lograr algo similar a esto:

.. code-block:: python

    nombre = input('Ingrese su Nombre:')
    apellido = input('Ingrese su Apellido:')
    edad = input('Ingrese su Edad:')
    print('Nombre:', nombre)
    print('Apellido:', apellido)
    print('Edad:', edad)

y haz clic en el botón **play** de **thonny**, podrás ingresar los datos 
directamente desde la ventana **Shell**.

.. image:: https://lh3.googleusercontent.com/LbcrSPVhErEtm4BpfCI6P1tCPiaVe7iNYf-kc0z6di0_Q6wXqNl8aGx_pTOkk8klPiiRPFqnoolNlpgZfSzfwNMbR4qHPui4f1Np1UeUvoKDV5eXfdTKDf3aAVnUAvZqKiZYlLQYSr2gFFz0mYezESgle1ISJkuRwSMZOZoVd83ZLd18xHtePqJc7bKCDK0zKN9c6yGPAS2P4WwhbLyIpoVtbFbB5ktDXb0m724Gxo4U0QF8kK5M8ynJvyOiGAPYFYXigInDDAlQULkZHkx4r_hjkutPRKE6Vyrl5VKB7kMuGEzIv01scV-gIvsuEzMzc3ha-CoTG3zGTi7-gl8tZNWtOdOBdejdT5ID4kEfbEXU8pZagFkdgwtRNPKQTRPp5m96nt7HvLmYw569TBzPNg0x4WRO37KR5b4GkOpLj0O2fQn9ICFgjEP-RPWc72mKfWHPeXL7g9OZZ7i0edscRiXMSkuyY34otMELK8gQ57k5MrCjJa9REXJAEF6CSMu_yMT2ZrwrUGenmGGxCPlz0fAOxWNqiOIY-JdzH95AwUmLZVNJ6HcmLCwIAeVJldZkAViHkUCaLWluD8mH1EQqFGOCJgGom-heqCKHtOGvGXqU1csLcwqtgvtPYt9U9QgrXZBfVbJ4K-npcG0BF5uxst6rDmC9EK0SzchsPH7nhBOL1OFHQIFF6_ZgiJG98VvSytGdE-vmy2yDK1AvOKaLU_vE=w469-h170-no?pageId=102396338536413597633

Como puedes ver, con saber estas 3 simples cosas ya puedes crear **variables** 
para almacenar tus datos, usar el **comandos** de entrada **input()** y el 
**comandos** de salida **print()**, con esto ya puedes practicar. En el próximo 
tutorial, te explicaremos cómo tomar decisiones usando tus **variables**.

Si queires darnos tu opinion sobre este articulo te invitamos a `contestar esta encuesta <https://forms.gle/WgxAGbshiTJATxaE9>`_

.. _página de facebook Rdckgames: http://facebook.me/rdckgames

Si tienes dudas o requieres una guía más personalizada contáctanos a través de 
nuestra `página de facebook Rdckgames`_.

