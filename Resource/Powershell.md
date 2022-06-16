# Powershell

## Comandos básicos e imprescindibles
Una vez que hemos conocido más sobre PowerShell os pasamos a mostrar una serie de comandos básicos e imprescindibles que debemos de conocer para trabajar con esta consola en línea de comandos. A medida que vayamos dominándolos podemos ir profundizando en ellos.

### Ayuda para usar cualquier comando
Es posible que a la hora de usar comandos de PowerShell nos encontremos con que nos sepamos cómo poder utilizarlos. Para ello podemos usar el comando Get-Help con el cual obtendremos diferentes tipos de ayuda. Ya sea una ayuda genérica, sobre un comando en concreto o saber cómo funciona cualquier comando:

```
Get-Help Get-Help <comando> 
```
```
Get-Help <comando> -Full 
```
```
Get-Help <comando> -Example 
```
```
Get-Help *
```

### Buscar y abrir archivos

En el caso de que necesitamos buscar un directorio concreto desde esta consola, el comando Get-Item que se encargará de mostrarnos su contenido en cuestión. Para ello escribiremos:

```
Get-Item <ruta>
```
Si lo que queremos es abrir un archivo desde esta consola, debemos de usar un comando similar al anterior como es:
```
Get-Content <ruta al archivo con su extensión>
```

### Buscar un comando
Es probable que en el momento de querer ejecutar cualquier comando puede que no nos acordemos exactamente de su sintaxis por lo que PowerShell cuenta con la posibilidad de buscarlos con sólo acordándonos de una parte de este.

Para poder encontrar comandos de un tipo similar o que contengan una frase en particular es posible usar el cmdlet Get-Command. Sin embargo, no enumera todos los cmdlet en PowerShell, por lo que se encarga de usar algunos filtros. Es posible usar los comandos:
```
Get-Comand – Name <nombre> 
```
```
Get-Commad – CommandType <tipo>
```
### Crear un nuevo directorio
Con PowerShell también podemos crear un nuevo directorio utilizando el comando mkdir. Es importante que a la hora de darle el nombre evitemos usar los espacios.

Por ejemplo, podemos crear el directorio DocumentoSoftZone

```
mkdir DocumentoSoftZone
```
También podemos evitar el uso de espacios insertando un guion o guion bajo como, por ejemplo:

```
mkdir DocumentoSoftZone
```

### Copiar y borrar archivos o directorios
Otra de las funciones de la consola de Windows es la posibilidad de copiar y borrar archivos o directorios, para lo cual podemos usar los comandos Copy-Item o Remove-Item en función de lo que necesitemos.

Para copiar un archivo o directorio usamos:
```
Copy-Item «ruta al archivo de origen con extensión» -Destination «ruta de destino»
```
En el caso de que lo que queramos sea borrarlo debemos optar por:
```
Remove-Item «ruta al archivo con extensión»
```

### Listado de todos los archivos dentro de una carpeta
Si queremos ver todos los elementos que se encuentran dentro de una carpeta podemos hacerlo a través del comando:
```
Get-ChildItem
```
Le podemos añadir el parámetro Force para mostrar también los elementos ocultos del sistema, por ejemplo, de la unidad C:.

```
Get-ChildItem -Path C: -Force
```
### Crear archivos y carpetas
Con PowerShell también tenemos la posibilidad de crear elementos nuevos en función del tipo de elemento. En caso de que tenga más de un tipo de elemento será necesario especificar el tipo de elemento.

Este comando crea una nueva carpeta:
```
New-Item -Path 'C:tempNueva carpeta' -ItemType Directory
```
Este comando crea un nuevo archivo vacío:

```
New-Item -Path 'C:tempNueva carpetafile.txt' -ItemType File
```
### Saber todo el contenido de un archivo
Si necesitamos saber todo el contenido de un archivo de texto en una ruta concreta podemos usar el comando Get-Content, para poder examinarlo sin necesidad de abrirlo. Si se utiliza Get-Content solo, no ofrece mucha utilidad, pero se puede mezclar con cmdlets más específicos con el objetivo de obtener resultados más precisos

Por ejemplo, podemos ver el contenido del archivo softzone.htm
```
Get-Content "C:/softzone.txt"
```
También podemos ver 10 líneas de texto incluidos en softzone.htm

```
Get-Content "C:/softzone.txt" – TotalCount 20
```

### Cambiar la política de ejecución
Si bien PowerShell cuenta con soporte para crear y ejecutar scripts, También dispone de restricciones para cada uno de ellos como parte de medidas de seguridad. Es posible cambiar el nivel de seguridad a cualquiera en cuatro niveles de restricciones. Para ello es posible usar el comando Set-ExecutionPolicy seguido de cualquiera de los niveles de seguridad que veremos a continuación:

```
Set-ExecutionPolicy Unrestricted 
```
```
Set-ExecutionPolicy All Signed 
```
```
Set-ExecutionPolicy Remote Signed 
```
```
Set-ExecutionPolicy Restricted
```
En esta lista, las políticas de seguridad van desde el menos restrictivo hasta el más restrictivo.

### Ver, iniciar, detener, suspender o reiniciar un servicio o proceso
Windows cuenta con determinados servicios que son pequeños procesos de aplicaciones utilizados que siempre se ejecutan en segundo, como, por ejemplo, para mantenerse siempre en alerta para ejecutarse o buscar actualizaciones en segundo plano.

### Lista de servicios en ejecución
Si queremos ver en PowerShell una lista completa de los servicios que se están ejecutando debemos usar el comando Get-Service. Con la ayuda de otros comandos podemos realizar determinadas acciones como:
```
Start-Service <nombre del servicio>
``` 
```
Stop-Service <nombre del servicio>
``` 
Suspend-Service <nombre del servicio>
```
Resume-Service <nombre del servicio> 
```
```
Restart-Service <nombre del servicio>
```
Los comandos mostrados en orden descendente podemos realizar acciones como iniciar un nuevo proceso, detener uno en ejecución, suspender, reanudar o reiniciarlo.

PowerShell Get-Service
Lista de los procesos abiertos
De forma similar podemos trabajar con los procesos de Windows. Para ver una lista con todos los procesos abiertos podemos utilizar el comando Get-Process. Con él podemos realizar determinadas acciones como:

```
Start-Process <nombre del proceso>
```
```
Stop-Process <nombre del proceso> 
```
```
Wait-Service <nombre del proceso>
```
En la lista en orden descendente, podemos iniciar un proceso nuevo, detenerlo o ponerlo en espera.

### Ejecutar aplicaciones UWP en Windows
Una de las finalidades de PowerShell es la posibilidad de ejecutar aplicaciones UWP de manera rápida, por lo que podemos usar para abrir determinadas aplicaciones o crear nuestros propios scripts. Para ello usamos el comando Star-Process.

Por ejemplo, si queremos abrir la Configuración de Windows usamos:
```
Start-Process «ms-settings:»
```

Si lo que queremos es usar una aplicación UWP como Spotify el comando a escribir sería
```
Start-Process «spotify:»
```