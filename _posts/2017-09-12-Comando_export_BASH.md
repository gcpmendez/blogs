---
layout: post
title: $ export (Variables de entorno)
categories:
- blog
tags:
- Bash
---


<!-- Estilo CSS del post-->
<style>
table {
    font-family: arial, sans-serif;
    border-collapse: collapse;
    width: 100%;
}

td {
  vertical-align: baseline;
    border: 1px solid #dddddd;
    text-align: left;
    padding: 8px;
}

th {
    text-align: center;

}

th:first-child {
    width: 25%;
}
tr:nth-child(even) {
    background-color: rgba(238, 238, 238, 0.57);
}

td:first-child {
   font-family: 'Inconsolata', monospace;
}

table h1 {
  font-size: 2em;
  font-weight: normal;
  color: #000;
}

h2 {
  font-size: 1.5em;
  font-weight: normal;
}

h3 {
  font-size: 1.17em;
  font-weight: normal;
}

h4 {
  font-size: 1.00em;
  font-weight: normal;
}

h5 {
  font-size: 0.83em;
  font-weight: normal;
}

h6 {
  font-size: 0.67em;
  font-weight: normal;
}
</style>

<!-- Imagen Markdown -->
# <img src="./../static/bash.png" alt="Drawing" style="width: 270px;"/>

<!-- Contenido post 
# Contenido-->

<br>
# Regla mnemotécnica
export = <b>export</b> to environment


<br>
# Descripción
Las llamadas **variables de entorno** se definen a nivel de sistema operativo para el correcto o mejor funcionamiento del mismo. Muchas de ellas son predefinidas pero cada usuario puede definir también sus propias variables para su entorno. El funcionamiento de las variables de entorno es el mismo que las variables normales. <ins>Se suelen diferenciar usando normalmente letras mayúsculas para definirlas</ins>.

El comando `export` es el que nos permite crear o modificar variables de entorno.

<br>
# Esquema
```
export [-fn] [name[=value] ...] 
export -p
```


<br>
# Opciones 

|Opción|Descripción|
|--|--|
|`-f`|refer to shell functions|
|`-n`|remove the export property from each NAME|
|`-p`|Muestra una lista de todas las variables y funciones exportadas.|




<br>
<!-- Ejemplos post -->
# Ejemplos



 Así

export VARIABLE-NAME

nos exporta VARIABLE-NAME o

export VARIABLE-NAME=valor

nos define y exporta VARIABLE-NAME como variable en entorno al mismo tiempo que el asigna un valor. Si no usásemos el comando export, VARIABLE-NAME se mantendría como una variable normal.
Ejemplos
USER 	Contine el nombre del usuario.
HOSTNAME 	Contine el nombre de la máquina.
HOME 	Indica cual es el directorio home del usuario.
PATH 	Contine los lugareres o paths del sistema donde se buscarán programas y comandos.
SHELL 	Indica cual es el intérprete de comando que se esta usando.

Es importante por ejemplo la variable PATH que nos dice donde se encuentran comandos tipo ls, cp, if, etc para su ejecución. Podemos mostrar su valor con

$ echo $PATH

Como veis cada path diferente viene separado por “:“. Podemos modificarla para que busque comandos y programas en la carpeta bin de nuestro home, donde podremos poner nuestros propios programas y scripts para poder ejecutarlos fácilmente desde cualquier directorio sin necesidad de copiarlos.

$ PATH=$PATH:$HOME/bin
$ export PATH
$ #Que es equivalente a ejecutar directamente
$ export PATH=$PATH:$HOME/bin
$ echo $PATH

Como veis hemos añadido al final a la variable PATH la carpeta $HOME/bin, y hemos usado la variable de entorno $HOME. Hay que tener cuidado de añadir y no sustituir con:

$ export PATH=$HOME/bin
$ echo $PATH

donde el comando echo no funcionará pues nuestro PATH será únicamente $HOME/bin, no puede ejecutar el comando echo ni ningún otro porque no va a buscar comandos a ningún otro sitio. Lo más sano en este caso es cerrar la terminal y abrir otra.







>**Nota:** Cuando no sepas cómo usar un comando en Linux, hay un manual al que puede referirse escribiendo:
`man [insert command here]` en una terminal.

<br>
## 1. Crea una **variable de entorno sin definir**

Este es un uso muy básico del comando `export`. 
```
$ export VAR_NAME
```

<br>
## 2. Crea una **variable de entorno definida**
Este es un uso muy básico del comando `export`. 
```
$ export VAR_NAME=valor
```
## 3. Muestra la **variable de entorno** que contiene el **nombre del usuario**



> **Nota:** Linux es sensible a mayúsculas y minúsculas además de necesitar el carácter `/` después de cada directorio para saber que no trabaja con un archivo.

> **Nota:** `~` es un carácter especial en el terminal que se evalúa automáticamente como el directorio inicial del usuario actual.

> **Nota:** Si necesita saber en qué directorio se encuentra, utilice el comando `pwd`.

> **Nota:** Además, para completar automáticamente las rutas de archivo largas al escribir en el terminal, puede pulsar `tab` después de haber empezado a escribir la ruta y se le presentarán opciones para elegir, o insertará la parte restante de la ruta.

<br>
## 2. Copiamos **múltiples archivos** al mismo tiempo


Para copiar multiples archivos en el mismo tiempo podemos solamente poner los archivos al comienzo del comando `cp` separados por espacios. Aquí tenemos el ejemplo:
```
$ cp file_1.txt file_2.txt file_3.txt ~/Documents/
```

<br>
## 3. Copiamos un **directorio**

Copiar un directorio es un poco complicado. Debe agregarse la opción `-r` o `-R` que significa recursividad. <ins>Esta opción es obligatoria tanto si el directorio esta vacío como si no lo esta</ins>. Aquí tenemos un ejemplo:
```
$ cp -r directory_1/ ~/Documents/
```
<br>
## 4. Crea **enlace duro** a un archivo en lugar de copiarlo

Copiar archivos significa que debes tener algo de espacio de almacenamiento para guardar estos archivos copiados. A veces, por alguna razón, es posible que quieras crear un "acceso directo" o enlace a los archivos en lugar de copiarlos. Para hacer esto puedes usar la opción `l`:
```
$ cp -l file_4.txt ~/Documents/
```
Esto hará que el archivo copiado tenga el mismo inodo, básicamente si modificas el archivo copiado estarás modificando el archivo original. Si borras uno de los dos archivos tendrás el otro como copia de seguridad. <ins>Tenga en cuenta que los enlaces duros no se pueden crear en directorios</ins>. 

<br>
## 5. Crear **enlace simbólico** en un archivo

Este es otro tipo de enlace llamados enlaces suaves o enlaces simbólicos. Usamos la opción `-s` para hacer esto. Aquí tenemos un ejemplo del comando:
```
$ cp -s /home/user/Documents/file_6.txt file_6.txt
```
<ins>La creación de enlaces simbólicos sólo se puede hacer en el directorio actual</ins>. 

A continuación, al listar el archivo copiado con detalle, verá que **file_6.txt** apunta al archivo original. <ins>Estará marcado con un signo de flecha después del nombre del archivo</ins>.

<br>
## 6. Copiar sin seguir los **enlaces simbólicos en la ORIGEN**
Para hacer esto podemos usar la opción `-P`. Cuando el comando cp encuentra un archivo con un enlace simbólico lo copiará como está. Echa un vistazo al ejemplo siguiente:
```
$ cp -P file_6.txt ~/movies/
```

Como verás el comando cp copiará el archivo **file_6.txt** como está. El tipo de archivo sigue siendo enlace simbólico.

<br>
## 7. Copiar siguiendo los **enlaces simbólicos en la ORIGEN**

Ahora podemos hacer esto con la opción `-L`. Básicamente, esta es la opción opuesta a la opción `-P` anterior. Aquí tenemos el ejemplo:
```
$ cp -L file_6.txt ./movies/
```

Con esta opción, el archivo copiado es el mismo archivo que el archivo origen **file_6.txt**. Esto se conoce con el tamaño del archivo. <ins>El archivo copiado tendrá un tamaño de archivo mayor de 33 bytes mientras que el archivo file_6.txt como enlace simbólico tiene un tamaño de archivo de 33 bytes</ins>.

<br>
## 8. Archivar los archivos

Cuando vamos a copiar un directorio usamos la opción `-r` o `-R`. Pero también podemos usar la opción `-a` para archivar el archivo. <ins>Esto creará una copia exacta de los archivos y directorios incluyento los enlaces simbólicos si hay alguno</ins>. Aquí tenemos un ejemplo:

```
$ cp -a directory_1/ /home/Documents/
```


El comando anterior copiará un directorio denominado **directory_1** en la carpeta **/home/Documents/** manteniendo los enlaces simbólicos. 


<br>
## 9. Explique **qué se está haciendo**

De forma predeterminada, cuando la actividad de copia es un éxito, veremos el símbolo del sistema de nuevo `$`. Si desea saber qué sucede durante la copia de archivos, podemos usar la opción `-v`.

```
$ cp -v *.txt /home/Documents/
```

Cuando copiamos todos los archivos txt del directorio actual a `/home/Documents/`, la opción `-v` mostrará lo que se está haciendo. <ins>Está información adicional hará que te asegures sobre lo que se está copiando</ins>.



<br>
## 10. Copia sólo cuando el archivo de ORIGEN es más **reciente**

Para hacer esto podemos usar la opción `-u`. Mira el siguiente ejemplo:
```
$ cp -vu *.txt /home/Documents/
```

Si en un principio tenemos por ejemplo un archivo **file_1.txt** que tiene de tamaño 0 bytes y lo editamos agregángole contenido podemos ver que el tamaño de este cambiará. Además si realizamos la acción de copia de nuevo veremos que sólo este será copiado ya que se ha modificado y es más actual que el que se copio anteriormente, incluso con la opción `-v` nos dirá cual se ha actualizado.



<br>
## 11. Usa el **modo interactivo**

El modo interactivo te preguntará si desea sobreescribir el fichero en caso de que ya exista en el directorio destino. Para activar el modo interactivo usa la opción `-i`.

```
$ cp -ir directory_1/ /home/Documents/
```

<br>
## 12. Crea una fecha de **copia de seguridad** cada vez que un archivo es copiado

<ins>Cuando la carpeta de destino ya tiene el archivo, por defecto el comando `cp` sobrescribirá el mismo archivo en el directorio de destino</ins>. Usando la opción `--backup` evitamos esto ya que el comando `cp` con esta opción hará una copia de seguridad de cada archivo existente en el destino que tengamos para copiar. Aquí tenemos un ejemplo:

```
$ cp --backup=simple -v *.txt /home/Documents/
```

Como podrás ver, la opción `--backup=simple` creará un archivo de respaldo marcado con el símbolo `~` al final del archivo si existen previamente los archivos idénticos copiados otras veces anteriores. La opción `--backup` tiene algún control, sus posibilidades son:

+ `none, off`: nunca hace copia de seguridad.
+ `numbered, t`: copia de seguridad numerada.
+ `existing, nil`: copia de seguridad numerada si ya existe, simple en caso contrario.
+ `simple, never`: copia de seguridad simple.

<br>
## 13. Copia solo los **atributos del archivo**

El comando `cp` también nos proporciona la opción `--attributes-only`. Como podemos adivinar a partir de su nombre, esta opción sólo copiará un nombre de archivo y sus atributos sin copiar ningún dato. Lo enseñamos a continuación:
```
$ cp --attributes-only file_6.txt -v ../Documents/
```

Podremos ver que el archivo **file_6.txt** tendrá un tamaño mayor que 0 bytes ya que posee datos y al usar la opción `--attributes-only` veremos que el archivo copiado tendrá un tamaño de 0. Esto es por que el contenido del archivo no ha sido copiado, únicamente hemos copiado sus atributos.

<br>
## 14. **Forzando** la copia

El uso de la opción `-f` forzará la actividad de copia. Si los archivos de destino no se pueden abrir, entonces `-f` lo intentará de nuevo.
```
$ cp -f *.txt -v ../Documents/
```

<br>
## 15. **Eliminando el destino** antes de copiar

Para hacer esto, podemos usar la opción `--remove-destination`. Esta opción contrasta con la opción `-f` anterior. Si el comando `cp` encuentra el mismo nombre de archivo en la carpeta de destino, el comando `cp` quitará primero el archivo de destino y copiará el nuevo. Ejemplo:
```
$ cp --remove-destination *.txt -v ../Documents/
```
