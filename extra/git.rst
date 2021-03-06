Git y la gestión del cambio
###########################

.. image:: https://git-scm.com/images/branching-illustration@2x.png

En este artículo te explicaremos que es **git** y una forma práctica para
usarlo.

¿Qué es **git**?
================

GIT es un sistema que permite llevar el control de cambio del código fuente de
cualquier aplicación. En nuestro caso nos permitirá llevar el control de
cambios de nuestro videojuego.

¿Qué es control del cambio?
+++++++++++++++++++++++++++

Para explicar mejor este concepto, considera la siguiente situación: Tú y tu
grupo de amigos deciden llevar a cabo un videojuego, en donde todos trabajan
programando el código del videojuego. Tú como integrante principal decides
crear los primeros archivos del código de tu videojuego, avanzas en el
desarrollo y ya tienes algo funcionando. ahora es momento de compartirlo con
tus amigos, así que decides enviarles un correo electrónico con el avance,
ya que son varios archivos, decides comprimir y adjuntar los al correo,
agregas a cada uno de tus amigos y les envías el archivo, entonces a cada
amigo le llega una copia de lo que hiciste, Luego continúas desarrollando
más características de tu videojuego. Hasta aquí parece todo normal, pero
de pronto te llega un correo electrónico de uno de tus amigo diciendo que
agregó nuevas características al videojuego para que las revises, entonces
descomprimes el archivo que te mandó y te das cuenta que hay un montón de más
archivos, el código de los archivos que estabas trabajando ha cambiado mucho,
y mientras tanto en el código que tu estas trabajando tienes un montón de
cambios más y otros tantos archivos más, incluso hay archivos que tienes en tu
código que se llaman igual que los que te mando tu amigo pero tiene cosas
totalmente distintas, entonces es hora de ponerse manos a la obra y mezclar el
trabajo de tu amigo con el tuyo. Creo que notarás hasta aquí que ya es algo
insoportable, tedioso y que lo más probable es que estropees todo intentando
hacerlo, tu esfuerzo como el de tu amigo están seriamente comprometidos.

Git es la herramienta que te salvará del problema en el que te haz metido, ya
que **git** hace todo esto en un par de segundos y mezcla los cambios de tu
amigo con los tuyos sin que esto provoque un error.

Explicar el problema fue tan largo como solucionarlo y la respuesta tan corta
como la solución con **git**.

¿Cómo empezar a usar **git**?
=============================

Para usar **git** debemos dejar de pensar que somos los únicos que trabajamos
en el código y pensar más como un equipo unido, es más, si eres un solo
desarrollador de todas formas existen 3 desarrolladores en ti; está el tú del
pasado, que hizo cambios que no te acuerdas hoy; está el tú actual, que añade
las nuevas ideas; y está el tú del futuro, que recibirá todos los cambios que
hagas hoy. Siendo conscientes de esta situación entonces debes asegurarte de
que el tú del pasado haya sido un buen aporte ya que el tú actual tendrá que
arreglar esos errores que se hayan provocado y el tú del futuro te lo
agradecerá. Antes de iniciar **git** debes descargar esta herramienta desde su
sitio oficial.

https://git-scm.com/

Esta herramienta debes instalarla como cualquier otro programa. una vez hayas
instalado **git** debes ir al directorio donde se encuentra tu proyecto e
iniciar allí una terminal, es importante que conozcas como funciona **git**
por dentro antes de usar una herramienta gráfica, pero no te preocupes es muy
simple.

Ya en el directorio de tu proyecto debes ejecutar el siguiente comando:

.. code-block:: sh

    git init

Este comando permite que **git** tome control inmediato de tu proyecto. Una vez
hecho esto **git** reconocerá todos los archivos de tu proyecto y necesitará
que crees el primer control de cambios del proyecto. para poder ver qué cosas
debes incluir en tu primer control de cambios debes ejecutar este comando:

.. code-block:: sh

    git status

Este comando te mostrará una lista de todos los archivos que han sido cambiados
y la lista de los archivos nuevos que debes agregar al control de cambios.
Al ser un control de cambios inicial verás que todos los archivos son nuevos,
así que debemos agregarlos. Para hacer esto debes ejecutar el siguiente
comando:

.. code-block:: sh

    git add *

Este comando te permite agregar cualquier archivo nuevo al control de cambios,
``*`` significa que queremos incluir todos los archivos y directorios. Una vez
agregados estos archivos al control de cambios, debemos confirmar que estamos
conformes con el resultado. para esto usamos el comando:

.. code-block:: sh

    git commit

`Este comando te permite guardar el cambio que ha tenido el proyecto.`

.. code-block:: sh

    git commit -m "primer control de cambios del videojuego"

`Adicionalmente este comando te permite especificar un mensaje para describir`
`el cambio que haz hecho`

Una vez hayas ejecutado este comando puedes seguir trabajando en tu código, una
vez que ya quieras guardar más cambios en el control de versiones solo debes
seguir la secuencia: **git status**,**git add**, **git commit -m 'mensaje'**.

Trabajando con con **git add**
++++++++++++++++++++++++++++++

Este comando te da la flexibilidad de agregar archivos de forma individual o
mediante comodines, Ej.

.. code-block:: sh

    git add ruta/a/un/archivo.gd

`Agrega el **archivo.gd** al control de cambios en la ruta donde se encuentra.`

.. code-block:: sh

    git add /una/ruta

`Agrega un directorio completo y su contenido al control de cambios.`

.. code-block:: sh

    git add /otra/ruta/*.gd

`Agrega todos los archivos con extensión **gd** al control de cambios en la`
`ruta donde se encuentran.`

Trabajando con **git commit**
+++++++++++++++++++++++++++++

Este comando tiene un atajo muy útil para evitar estar ejecutando **git add**,
este atajo es útil cuando quieres agregar todos los archivos que has cambiado
(no aplica a archivos nuevos que hayas creado) es tan simple como agregar una
a como parámetro:

.. code-block:: sh

    git commit -am "Descripción del cambio"

`Este comando automáticamente ejecuta **git add** a todos los archivos que`
`están preparados para el control de cambios y los guarda.`

¿Qué pasa entonces con mis archivos nuevos? estos no fueron agregados.
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

Para cada archivo nuevo, **git** debe saber que están preparados para el
control de cambios, así que deberás ejecutar manualmente **git add** para
cada uno de ellos. puedes apoyarte con la herramienta **git status** que te
entrega una lista de los archivos nuevos que no han sido agregados al control
de cambios.

Este es todo el flujo de trabajo para ir haciendo cambios en tus archivos.

Ahora debes compartir estos cambios con tus amigos
++++++++++++++++++++++++++++++++++++++++++++++++++

Para realizar esto existen varias plataforma que puedes elegir, pero acá te
mencionaremos 3, el que elijas una u otra es cosa de gustos ya que todas
funcionan igual.

**Github**: Es una de las plataformas más extendidas y usadas por todos los
desarrolladores, te permite tener repositorios públicos y privados. La empresa
detrás de este sitio es **Microsoft**.

**Gitlab**: Es la versión open source de github y tiene las mismas
características, la diferencia radica en que puedes opcionalmente usarla para
hacer tu propio servidor.  La empresa detrás de este sitio es **GitLab Inc**.

**Bitbucket**: Plataforma usada principalmente por grandes empresas, dispone de
su servicio gratuito igual que **Github** y **Gitlab**, permite crear
repositorios públicos y privados. La empresa detrás de este sitio es
**Atlassian**.

Una vez hayas creado una cuenta en alguno de estos servicios debes crear en él
un repositorio, este repositorio es el lugar donde se aloja tu código para ser
compartido, una vez hayas creado el repositorio debes ejecutar el siguiente
comando para conectar el código en tu computadora personal con el repositorio
remoto. Para los ejemplos usaremos Github.

.. code-block:: sh

    git remote add origin https://github.com/username/repositorio.git

`Este comando tiene varias partes que debemos explicar`

**git remote** es el comando para trabajar con un repositorio remoto, el
parámetro add que le sigue es para indicarle que queremos agregar un
repositorio remoto a nuestro proyecto, luego de **add** debemos
especificarle el nombre que le queremos dar a ese repositorio remoto, en
este caso es **origin** (se usa **origin** por conversión), luego debemos
especificar la **url** donde se encuentra este repositorio, aca debes
copiar la url que te entrega **github** (o del servicio que hayas preferido)
en el navegador.

Una vez has realizado la vinculación debes enviar tu control de cambio guardado
(después de realizar **git commit**) al repositorio remoto con el siguiente
comando:

.. code-block:: sh

    git push -u origin master

Este comando envía los cambios de tu repositorio local al repositorio remoto,
aca hay algunas cosas que explicar, el parámetro **-u** permite adicionalmente
enviar las referencias de registro que estén en tu repositorio local.
**origin** es el nombre del repositorio a donde queremos enviar los cambios
(esto es para no tener que escribir la url completa, aunque si colocas la url
también funciona) **master** es la rama principal de nuestro proyecto que se
creó cuando ejecutamos **git init**.

¿Qué es una rama?
+++++++++++++++++

**Git**, para controlar los cambios que realizamos en nuestro código los
organiza en ramas, cuando vas guardando cambios con **git commit** estos se
hacen en la rama donde te encuentras en ese momento. La rama por defecto
siempre es **master** (el nombre **master** es por convención). También
puedes crear tus propias ramas, estas te permiten hacer una imagen de la
rama actual y hacer cambios sin que estos afecten a la rama desde donde
hiciste esa imagen, es muy recomendable trabajar todos tus cambios en ramas,
más adelante te explicaremos como hacer uso de ramas para trabajar.

¿Como puedo descargar los cambios realizados por mis amigos?

**Git** permite  mediante el siguiente comando descargar cualquier cambio
realizado por tus amigos:

.. code-block:: sh

    git pull

este comando permite descargar los cambios de tu repositorio remoto por defecto
(en este caso **origin**) de la rama en la cual estamos actualmente (en este
caso **master**) este comando es muy especial ya que no tan solo descarga los
cambios realizado por otros sino que también los combina con los cambios que
hayas realizado en tu código. también puedes usar el comando de forma más
explícita ejecutando:

.. code-block:: sh

    git pull origin master

Que en este caso hace lo mismo que el anterior, pero más adelante te ayudará a
trabajar con ramas de una forma más segura.

Trabajando con **git**
======================

Ahora te explicaremos un proceso de trabajo con **git** que puedes aplicar a
cualquiera de tus proyectos.

Cuando estés trabajando en tu proyecto, siempre es bueno establecer que la rama
**master** siempre tenga los cambios estables y que sabes que están probados y
funcionando correctamente, solo modificarás **master** si estas seguro de que
los cambios que modificarán **master** están probados y funcionando
correctamente. La idea detrás de esto es que si por algún motivo debes partir
de nuevo desde un punto donde puedes estar seguro que no hay errores, eso
sería **master**.

Entonces como sabemos ya que no tienes ninguna otra rama en tu proyecto debes
estar actualmente en la rama **master** de tu código, antes de crear tu primera
rama, para empezar a hacer cambios, debemos asegurarnos de tener la versión más
actualizada de nuestro código, para ello debemos ejecutar:

.. code-block:: sh

    git pull

Esto descargará todos los cambios que en el momento no tenemos en nuestro
código. A continuación vamos a crear una imagen de **master** con un nombre de
rama nuevo:

.. code-block:: sh

    git checkout -b nueva_rama

Este comando permite crear una nueva rama llamada 'nueva_rama' con el parámetro
**-b** permite crearla y cambiarse a ella inmediatamente, esta nueva rama será
una imagen fiel de **master**.

Una vez estando en la nueva rama, puedes verificar esto con el comando
**git status**, la forma de trabajar en esta rama es igual a la explicada
anteriormente, la secuencia; **git status**,**git add**, **git commit**.

Creando una rama para hacer pruebas
+++++++++++++++++++++++++++++++++++

Es recomendable tener una rama dedicada exclusivamente a realizar pruebas,
esto es para poder mezclar los cambios que hayas realizado con una imagen de
**master** y así probar el comportamiento de tu código antes de mezclar con
master. Así que para crear esta imagen de prueba debemos primero cambiarnos a
la rama master. pero antes, si tiene cambios que no has guardado,
ejecuta **git commit**

.. code-block:: sh

    git checkout master

Una vez estés en la rama **master** debes ejecutar los siguientes comandos:

.. code-block:: sh

    git pull
    git checkout -b test

Esto creará una imagen de **master** llamada **test**.
 ..

Ahora es recomendable subir **test** al repositorio remoto

.. code-block:: sh

    git push origin test

Una vez que estés en la rama **test** podrás mezclar tus cambios con esta rama
y así probar que todo esté funcionando correctamente, para ello debes ejecutar
el siguiente comando.

.. code-block:: sh

    git merge nueva_rama

Esto mezclará los cambios realizados en **nueva_rama** dentro de la rama
**test**.

Una vez hecho esto y hayas probado que la integración quedó correctamente,
puedes mezclar tus cambios con **master**.

.. code-block:: sh

    git checkout master
    git merge nueva_rama

Si por el contrario se encontraron errores, no debes preocuparte solo cambiate
a la rama donde están los cambios (nueva_rama), corrige los errores,
guarda esos cambios con **git commit** y vuelve a mezclar con **test**.

.. code-block:: sh

    git checkout nueva_rama

En este punto estás haciendo los cambios en tus archivos.
 ..

.. code-block:: sh

    git status
    git commit -am "Corrección de errores"
    git checkout test
    git merge nueva_rama

Se prueban los cambios y todo funciona correctamente.
 ..

.. code-block:: sh

    git checkout master
    git merge nueva_rama

Como puedes ver, solo pasa a la rama **master** si no se han encontrado errores
, esto te permite estar muy seguro que **master** siempre tendrá el código más
estable posible (ya que no es posible eliminar todos los errores, pero si
evitarlos lo más posible). Luego que ya estás en la rama **master** (con
**git status** puedes asegurarte de esto) comparte los cambios con tus amigos.

.. code-block:: sh

    git push origin master

Creando versiones de la aplicación
++++++++++++++++++++++++++++++++++

Como recomendación siempre es útil crear versiones de los cambios que realices
en **master**, para ello usaremos el siguiente comando:

.. code-block:: sh

    git tag -a 1.0.0 -m “Descripción de esta versión”
    git push origin 1.0.0

**git tag** te permite colocar un nombre al último cambio realizado sobre una
rama, en este caso **master**. Esto es útil porque si queremos volver a una
versión anterior no tenemos que estar buscando los cambios dentro de la enorme
historia de cambios que crea **git**, sino que lo hacemos por medio de
versiones que es más fácil de entender por humanos.

Explicando las partes de este comando, tenemos **-a** que permite crear un
nuevo número de versión, en este caso el parámetro que le sigue: **1.0.0**;
luego el parámetro **-m** permite establecer una descripción de esta versión
seguido del texto que queremos escribir.

Luego **git push**, permite enviar la versión al repositorio remoto, en este
caso hemos enviado al repositorio remoto **origin** la versión **1.0.0** de
nuestro código.

¿Cómo puedo descargar las versiones enviadas por mis amigos?

Para descargar las nuevas versiones que no tengas en tu código solo basta
ejecutar estos comandos:

.. code-block:: sh

    git pull origin master
    git fetch --tags

Es muy importante que hagas esto antes de crear tu versión del código ya que
así sabrás la última versión publicada y poder crear versiones incrementales.


¿Qué son las versiones incrementales?
+++++++++++++++++++++++++++++++++++++

Cuando queremos crear una versión de nuestro código siempre es bueno seguir una
convención, en este caso hemos creado la versión **1.0.0**, ¿qué significan
estos números?.

El primer número (1) indica la versión de nuestro videojuego, si en un futuro
quieres hacer una segunda parte del videojuego con nuevas gráficas, nuevos
personajes, nueva historia; será tiempo de cambiarlo por 2. También se le suele
llamar **versión mayor** o **major version**.

El segundo número (0) indica los cambios que se le han hecho a la versión mayor
de nuestro videojuego, esto puede ser un nuevo contenido, nuevas
características; pero manteniendo el mismo videojuego. También se le suele
llamar **versión menor** o **minor version**.

El tercer y último número (0) indica los cambios que se han realizado desde la
último **versión menor**, normalmente relacionado con la corrección de bugs,
glitches, o fallos de seguridad. También se le suele llamar
**versión de construcción** o **build version**.

Estos números van separados por puntos por convención.

Recomendaciones finales
=======================

Si cada integrante del equipo realiza este procedimiento tal como está
definido, la posibilidad de mantener un código distribuido estable es
altamente confiable.

Siempre que te cambies con **git checkout** a una rama existente es
recomendable ejecutar **git pull** para descargar los cambios que no
tengas en tu copia local del código.

Ya con este conocimiento adquirido puedes usar cualquiera de las
herramientas visuales que te ayudarán a trabajar de una forma más integrada
con **git** y tu editor de códigos:

https://git-scm.com/downloads/guis/

Puedes usar la que más se acomode a tu forma de trabajar. También muchos
editores de código ya vienen integrados con **git**, como
**Visual Studio Code**.

Si quieres conocer **git** más a fondo te recomendamos esta lectura:

https://git-scm.com/book/es/v2
