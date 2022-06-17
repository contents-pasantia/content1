# Comandos bash LINUX - UBUNTU
- La forma en como se organizan los elementos en el sistema operativo es a travez del arbol de directorios, este está conformado por carpetas (directorios) y archivos (binarios y no binarios).
- es recomendable crear los nombres de las carpetas y los archivos en minusculas y sin acentuación para que así sea mas facíl moverse en el directorio del pc.
- comando para listar archivos.
    - ls || ls <path> : lista los elementos (no ocultos) en el directorio seleccionado, si no se agrega path se listan los elementos en el directorio actual (en el que se encuentra ubicado).
    - la || ls -a <path>: lista todos los elementos de un directorio, incluido los ocultos.
    !nota¡: los elementos ocultos son todos lo elementos que tiene un punto inicial en su nombre; en todo directorio existen dos directorios ocultos que son directorios virtuales, estos apuntan a el directorio actual (.) o a el directorio anterior (..)
    - ls -d */ : lista todos los directorios dentro del path presente.
    - ls -d *<ext>: lista todos los elementos terminados con la extención especificada.
    - ls -d <ini>*: lista todos los elementos que inicien con las letras especificadas.
    - ll || ls -l: lista todos los archivos en formato largo mostrando sus permisos y demas caracteristicas.
    - ls -lh || ll -h: imprime el tamaño de los archivos de forma entendible, con acotaciones.
    - ls -d: imprime solo el nombre del subdirectorio, sin mostrar los aarchivos internos.
    - ls -lt || ll -t: lista los elmentos del directorio ordenados por la fecha de modificación, del mas reciente a el menos reciente (con -r se invierte este orden).
    - ls .1: lista los elementos del directorio en forma de columna.
    - ls -i: muestra el numero de i-nodo antes del nombre del elemento.
    !nota¡: el numero de i-nodo: es un identificador para el inodo del elemento, el inodo contiene las caracteristicas de in archivo regular o directorio o cualquier otro elemento que se pueda obtener en el sistama de ficheros.
    - ls -m: muestra todos los elementos de un directorio separados por una coma.
    - ls -R: hace un listado recursivo (muestra los elementos dentro de los elementos).
    - ls -s: muestra delante del nombre el tamaño en kilobytes del elemento.
- cambiar de directorio.
    !nota¡: de forma predeterminada existen 2 acotamientos de directorios importantes, el directorio raiz es (/) y el directorio home (~); el home es el directorio predeterminado del usuario y el directorio raiz el el directorio inicial.
    - cd <path>: (change directory) permite movernos en la terminal cambiando de directorio, existen dos maneras de moverse, absoluta (se coloca el path completo), relativa (se va avanzando carpeta por carpeta).
    - cd ~: lleva al directorio home.
    - cd /: lleva al directorio raiz.
    - cd -: lleva al ultimo directorio visitado.
- mostrar la ubicación actual.
    - pwd : (print working directory) muestra la direccion actual.
- crear elementos.
    - mkdir <name directory> : crea carpetas o directorios.
    - touch <name file> : crea archivos vacios.
    - nano <name file>: crea archivos utilizando el editor de texto nano.
    - vim <name file>: crea archivos utilizando el editor de texto vim.
- copiar elementos.
    - cp <path file origin> <path destiny>: copia un archivo o elemento a el directorio destino seleccionado. 
    - cp -r <path file origin> <path destiny>: copia un archivo o elemento de forma recursiva a el destino seleccionado.
- eliminar elementos.
    - rm <name file>: se utiliza principalmente para eliminar archivos.
    - rm -f <name file>: elimina un archivo de forma forzada.
    - rmdir <name directory>: elimina solo los directorios vacios.
    - rm -rf <name directory>: elimina el directorio especificado con los elementos que contenga (de forma recursiva).
- mover elementos:
- el comando mv también se puede utilizar para cambiar el nombre del archivo.
    - mv <name file> <new name file>: cambia el nomvre del archivo.
    - mv <path file origin> <parh file destiny>: mueve el archivo de una carpeta a otra.
- comando para imprimir en pantalla.
    - echo <word>: imprime la palabra en la consola.
- expandir el contenido de una variable.
    - $<var>: con este antecesor se puede expandir el contenido de una variable.

# editores de texto en la consola de linux
- vim: es el editor de texto por defecto en todos los sitemas operativos basados en UNIX, vim se caracteriza por tener 3 modos de manejo principales, estos modos de manejo son:
    - Modo comando: permite al usuario navegar por el documento y así introducir comandos a ejecutar dentro del archivo, por defecto cuando se abre un archivo con vim se entra en este modo, si se cambia de modo con ESC se regresa al modo de comandos.
    - Modo insercion: para entrar en modo de inserción de texto se preciona la tecla (i), en este modo se puede ingresar texto en el archivo y editarlo.
    - modo Ex: en este modo se manipula el estado del arhcivo (guardar, cerrar, etc) para entrar en este modo de debe ingresar (:).
- comandos de vim:
    - H: desplazamiento a la parte superior de la pantalla.
    - L: desplazamiento a la parte inferior de la pantalla.
    - G: desplazamiento hasta el final del documento.
    - w: desplazamiento una palabra a la derecha.
    - b: desplazamiento una palabra a la izquierda.
    - 0: desplazamiento al incio de la linea actual.
    - $: desplazamiento al final de la linea actual.
    - i: activa el modo inserción de texto.
    - I: modo inserción de texto al inicio de la linea donde se encuentra el cursor.
    - O: insertar una linea en blanco antes de la linea actual.
    - o: insertar una linea en blanco despues de la lina actual.
    - r: sustituye el caracter en la posicion actual del cursor.
    - R: sobreescribe desde la posicion aztual del cursor.
    - x: borrar el caracter de la posicion actual del cursor.
    - X: borrar el caracter siguiente al de la posicion actual del cursor.
    - dd: corta la linea actual (queda disponible en el portapapeles).
    - D: cortar desde la posicion actual del cursor hasta el final de la linea.
    - yy: copiar la linea completa donde se encuentra el cursor.
    - y#: copia el numero de caracteres desde la posicion actual del cursor.
    - P: pegar en la linea anterior a la que se encuentre el cursor.
    - p: pegar en la linea siguiente a la que se encuentre el cursor actualmente.
    - .: repite el ultimo comando.
    - u: deshace el ultimo comando.
    - :w: guarda el estado actual del archivo.
    - :wq: guardar y salir.
    - :q: salir sin guardar.
    - ZZ: guardar y salir.
    - :x: guardar y salir.

# batch
- procesamiento por lotes o batch, son programas que procesan texto y emiten un resultado.
- utilidades batch:
    - cat: muestra todo el contenido de un archivo de texto.
    - head: muestra las primeras 10 lineas de un archivo de texto.
    - tail: muestra las ultimas 10 lineas de un archivo de texto.
    - head || tail -n <number>: muestra el numero de lineas especificadas.
- utilidades avanzadas de batch:
    - grep <word> <file name>: busca la palabra en el archivo y muestra las lineas de texto que contienen esa palabra.
    - grep -i <word> <file name>: busca la palabra sin tomar en cuenta las mayusculas o minusculas.
    - grep "<word>$" <file name>: busca una lina del archivo que temine con la palabra especificada.
    - sed 's/<word>/<sustitute>/g': sustituye una palabra por otra de forma global en el documento. (este comando no modifica el archivo)
    - sed '$d': elimina la ultima linea del documento. (este comando no modifica el archivo)
    - awk: es un comando que nos permite trabajar archivos de texto estructurados (separados por comas, etc.).

# redireccionar salidas y entradas en los comandos de la terminal
- el redireccionar las salidas o las entradas los resultados de los comandos se utiliza para utilizar un archivo como fuente de los comandos (redireccionar la etrada) o utilizar un archivo para almacenar los resultados (redireccionar la salida)
    - <command> < <name file>: redirecciona la entrada del comando.
    - <ommand> >> <name file>: agrega el resultado del comando a el archivo indicado.
    - <command> > <name file>: redirecciona la salida del comando.
    - <command> | more: muestra la salida del comando en secciones. (con enter muestra una linea mas, con space bar muestra una pagina extra)
    - <command> | wc: muestra cuantos caracteres, palabras o lineas hay en el resultado.
    - <command> | wc -l: muestra cuantas lineas hay en el resultado.

# comandos interactivos (ctrl)
- son comandos que se pueden ejecutar sin importar que un proceso este en ejecución
    - ctrl+z: manda un proceso en ejecucion a ejecutarse en segundo plano (bakground)
    - ctrl+c: termina un proceso en ejecucion.
    - ctrl+l: limpiar la consola.

# background and foreground
- !nota¡ un proceso daemon: es un proceso que se ejecuta en segundo plano para no ser interactivo (no es controlado directamente por el usuario)
    - <command> &: enviar el proceso del comando en sedungo plano.
    - fg: traer al primer plano (foreground) el proceso que se esté ejecutando en segundo plano.
    - ps: muestra los procesos que estan el ejecucion
    - ps ax: muestra de forma extensa los procesos que se encuentran en ejecución.
    - top: muestra de forma interactiva y en tiempo real los procesos que se están ejecutando.
        - q: salir del comando top.
    - kill -<number priority> <number process>: mata un proceso por medio de la emición de una señal.

# permisos dobre los archivos
- los archivos contiene distintas caracteristicas estas caracteristicas se dividen en:
    - usuarios: existen 3 tipos de usuarios, dueño, grupo, otros.
    - permisos: existen 3 operaciones que se pueden hacer con los archivos leer, escribir, ejecutar.
- como leer los permisos de los archivos:
    - (-): indica que hay un permiso que está negado.
    - r: significa lextura (read).
    - w: significa escritura (write).
    - x: significa ejecución, en caso de directorio indica que se puede ingresar.
    - d: indica que es un directorio.
    - l: indica que es un link.
- !nota¡ tambien se pueden modificar los permisos ingresando valores numericos en la base binaria o en la decimal.
    - 7: todos los permisos otorgados a el grupo especificado.
    - 6: solo permisos de lectura y escritura.
    - 5: solo lectura y ejecucion.
    - 4: solo lectura.
    - 3: solo escritura y ejecución.
    - 2: solo escritura.
    - 1: solo ejecución.
    - 0: ningun permiso habilitado.
- existe una serie de comandos que nos permiten visualizar estos permisos y editarlos:
    - ls -l: nos muestra los permisos que contienen los archivos.
    - chmod: cambia los permisos que contiene el archivo.
        - chmod <tipo de usuario><operación><permiso> <name file>.
    - chown: cambia quien es el propietario.
        - chown <nombre de usuario> <name file>.
    - chgrp: cambia cual es el grupo perteneciente al archivo.
        - chgrp <tombre de grupo> <name file>.
- !nota¡ el usuario root es el super usuario del sistema, esto significa que puede realizar escritura y lectura de cualquier archivo, para ingresar un comando como usuario root se debe agregar la palabra sudo.

# administradores de paquetes
- los administradores de paquetes son los programas que vienen en los sitemas operativos encargados de descargar e instalar aquellos programas que deseemos que no se encuentren en nuestro sistema.
    - apt: es el administrador de paquetes para distribuciones de linux basadas en debian.(Advance package tool)
    - zypper: es el administrador de paquetes para distribuciones linux basdas en suse.
    - rpm: es como el administrador de paquetes "universal".

# compirmir archivos
- en ocaciones es necesarios comprimir los archivos ya sea porque se necesita enviar o para liberar un poco mas de espacio en el disco, en estos casos se puede utilizar el siguiente comando:
    - gzip <name file>: comprime el archivo.
    - gzip -d <name file>: descomprime el archivo
- tar es una herramienta que nos permite agrupar distintos arhivos en uno solo, se puede utilizar de la siguiente manera:
    - tar cf <name new file> <directory files>: comprime los distintos archivos ubicados en un directorio en un solo archivo.
    - tar xf <name file>: descomprime los archivos agrupados y los coloca en una carpeta con el nombre del archivo comprimido.

# herramientas de busqueda.
- comandos y herramientas para realizar busquedas en la terminal.
    - locate: es un comando que nos permite buscar en nuestro pc los archivos que no encontremos, sin embargo para que locate funcione de forma correcta se le debe actualizar la base de datos.
        - sudo updatedb: actualiza la base de datos de locate.
        - locate <name file>: busca y muestra la dirección donde se encuentra el archivo.
    - whereis: es un buscador de archivos binarios, este nos permite encontrar la ubicación de comandos y archivos binarios en el pc:
        - whereis <command>: encuentra la ubicacion del comando ingresado.
    - find: es el comando mas complejo pero que nos permite realizar busquedas mas especificas y exaustivas en nuestro pc.
        - find <path> <expresion de busqueda> <acción>: nos permite buscar archivos con caracteristicas especificas en un directorio solicitado, ej: find . -user user -perm 644: busca documentos en la carpeta actual que tengan como usuario a user y que tengan los permisos 644.
        - find -type <type file> -mtime <time>: busca elementos de un tipo especifico que hayan sido modificados en un intervalo de tiempo, ej: find -type f -mtime +7: solo busca archivo (files) que hayan sido modificados hace mas de 7 dias.
        - find <command> -exec <command>: find también nos permite ejecutar una acción especifica sobre los archivos encontrados.

# herramientas para interactuar a través de HTTP.
- estas herramientas nos permiten hacer solicitudes http a un servidor, e interactuar con el.
    - curl: nos permite hacer peticiones http y recibir una respueta en "crudo" por parte del servidor, estas respuestas pueden ser json, html, etc.
    - wget: nos permite realizar descargar de archivos binarios que esten ubicados en servidores.

# herramienta para comunicacion tcp (mails)
- comandos para enviar mails.
    - mail -s <message> <mail>: envia un mensaje al correo especificado.

# conexiones seguras a servidores en remoto
- comandos para generar conexiones seguras con computadoras o servidores en remoto.
    - ssh: este es un protocolo de comunicación que se basa en crear 2 llaves, una publica y una privada. la idea se basa en compartir la llaves pueblicas que permiten a cada uno de los endpoint interpretar los mensaje emitidos y enriptados con las llaves privadas.
        - ssh-keygen: comando para gerenerar llaves.
            - -m PEM: formato de la llave como PEM
            - -t rsa: tipo de la llave creada rsa.
            - -b <bits>: define el numero de bits de la llave
            - -N: permite crear un passphrase (contraseña para acceder al ssh).
        - ssh-keygen -t rsa: genera un par de llaves de tipo rsa.
        - ssh-keygen -m PEM -t rsa -b 4096: genera un par de llaves de tipo PEM de 4096 bits, si ya existe una llave se reemplaza.
    
# variables de entorno.
- las variables de entorno son variables dinamicas (declaradas en el pc) que pueden afectar el comportamiento de ciertos procesos, esta variables utilizadas en la terminal se especifican para poder ejecutar o cambiar la forma en como se aplica un proceso. Es una definicion global a la que todos los procesos tiene acceso
    - export <var>=<valor>: asignacion de variable de forma global.
    - <var>=<valor>: asignacion de variable de forma particular.

# crear scripts para bash
- crear un script es crear una secuencia de una series de comandos que se ejecuten de forma automatica y nos faciliten o eviten realizar tareas repetitivas en la terminal de comando, estos archivos que se ejecutan en la termina o bash tienen la extension .sh
    - los archivos <name file>.sh: son archivos creados para contener comando que se ejecuten en la terminal o bash, este tipo de archivos se conocen como scripts, deben tener ciertas caracteristicas.
        - definir el interprete para ejecutar los comandos, ej: #!/bin/bash
- automatiación de los scripts.
    - at: es un comando que nos permite automatizar ciertas tareas en un determinado tiempo, ej: at now +2 minutes: pide que se ejecute un comando (que se especifica luego) dentro de 2 minutos.
    - cron: permite especificar la hora y de forma periodica como se ejecutan los comandos especificados.

# links
- ejecutar scripts en windows: http://www.cristalab.com/tutoriales/programacion-batch-con-archivos-.bat-c48410l/