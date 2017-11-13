---
layout: post
title: $ du
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
    width: 50%;
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


<!-- Contenido post -->
# Contenido

<https://blog.desdelinux.net/du-ver-directorios-ocupan-espacio/>


<br>
# Regla mnemotécnica
du = <b>D</b>isk <b>U</b>sage

<br>
# Descripción
Comando de referencia que se usa para **verificar la información de uso de disco de archivos y directorios en una máquina**. Posee muchas opciones de parámetros que se pueden usar para obtener los resultados en muchos formatos. Muestra los archivos y tamaños de directorio de forma recursiva.

<br>
# Esquema
``` sh
 du [PARÁMETROS]... [ARCHIVO]...
```


>**Nota:** Cuando no sepas cómo usar un comando en Linux, hay un manual al que puede referirse escribiendo:
`man [insert command here]` en una terminal.


<br>
<!-- Ejemplos post -->
# Ejemplos
## 1. Ejecutamos **du** sin ninguna opción

Este es un uso muy básico del comando du. 

> **Nota:** Si no establecemos el directorio a partir del cual obtendrá el resumen de uso del disco el lo establece automáticamente con la ubicación en la que te encuentres. 

```
$ du
```
La salida del comando `du` mostrará el número de bloques en disco que ocupa el directorio actual con sus subdirectorios.

> **Nota:** Linux es sensible a mayúsculas y minúsculas además de necesitar el carácter `/` después de cada directorio para saber que no trabaja con un archivo.

> **Nota:** `~` es un carácter especial en el terminal que se evalúa automáticamente como el directorio inicial del usuario actual.

> **Nota:** Si necesita saber en qué directorio se encuentra, utilice el comando `pwd`.

> **Nota:** Además, para completar automáticamente las rutas de archivo largas al escribir en el terminal, puede pulsar `tab` después de haber empezado a escribir la ruta y se le presentarán opciones para elegir, o insertará la parte restante de la ruta.

<br>
## 2. Ejecutamos **du** con la opción **-h** 

Esto nos facilitará la lectura del tamaño del directorio ya que podrás ver los tamaños en Bytes, Kilobytes, Megabytes, Gigabytes, ... .

```
$ du -h ~/Documents/
```

La salida del comando `du -h ~/Documents/` mostrará el tamaño en disco del directorio y sus subdirectorios.

> **Nota:** por defecto el tamaño de bloque establecido en el comando `du` es de **1024 bytes** o lo que es lo mismo **1 Kilobytes**.

<br>
## 3. Ejecutamos **du** con la opción **-s** 

Para obtener un resumen del tamaño total en disco de un directorio usamos la opción `-s`:

```
$ du -sh ~/Documents/
```
La salida del comando `du -sh ~/Documents/` mostrará el tamaño en "formato humano" de ese directorio.


<br>
## 4. Ejecutamos **du** con la opción **-a** 

Esta opción <ins>muestra el tamaño usado en disco de todos los archivos, no sólo de los directorios</ins>. 

```
$ du -ha ~/Documents/
```
La salida del comando `du -ha ~/Documents/` mostrará el tamaño en "formato humano" de los archivos y directorios que se encuentran dentro del directorio dado.

<br>
## 5. Ejecutamos **du** con la opción **-k** 

Esta opción <ins>muestra el tamaño usado en disco en unidades de 1024 bytes</ins>. 
```
$ du -k ~/Documents/
```
La salida del comando `du -k ~/Documents/` mostrará el recuento de bloques usados en unidades de Kilobytes.

<br>
## 6. Ejecutamos **du** con la opción **-m** 

Esta opción <ins>muestra el tamaño usado en disco en unidades de 1024 bytes.</ins>. 
```
$ du -m ~/Documents/
```
La salida del comando `du -m ~/Documents/` mostrará el recuento de bloques usados en unidades de Megabytes.

<br>
## 7. Ejecutamos **du** con la opción **-c** 

Esta opción <ins>añade en la última línea el espacio de disco usado por el directorio.</ins>. 
```
$ du -m ~/Documents/
```
La salida del comando `du -m ~/Documents/` mostrará el recuento de bloques usados en unidades de Megabytes.



<br>
# Referencias
Wikipedia: <https://en.wikipedia.org/wiki/Du_(Unix)>  
Tecmint: <https://www.tecmint.com/check-linux-disk-usage-of-files-and-directories/>