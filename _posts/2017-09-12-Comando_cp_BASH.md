---
layout: post
title: cp
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
# Descripción
Comando de referencia para **copiar archivos y directorios**. Su lógica consiste en copiar de FUENTE a DESTINO, o de multiples FUENTE(s) a un DIRECTORIO.

  Los argumentos obligatorios para las opciones largas son obligarios también para las opciones cortas.

<br>
# Esquema
```
       cp [OPTION]... [-T] SOURCE DEST  
       cp [OPTION]... SOURCE... DIRECTORY  
       cp [OPTION]... -t DIRECTORY SOURCE...  
```


<br>
# Opciones + usadas

|Opción|Descripción|
|--|--|
|`-f, --force`|Si no se puede abrir un archivo de destino existente, eliminalo y vuelve a intentarlo (esta opción se omite cuando también se utiliza la opción -n).|
|`-n, --no-clobber`|No sobreescribas un archivo existente(Anula la opción -i).|
|`-P, --no-dereference`|Nunca seguir los enlaces simbólicos en la FUENTE.|
|`-R, -r, --recursive`|Copia directorios recursivamente.|
|`-s, --symbolic-link`|Establecer un **link simbólico** en lugar de copiarlo.|
|`-u, --update`|Copia solo cuando los archivos FUENTE son más recientes que los archivos de DESTINO o cuando el archivo de DESTINO no existe.|
|`-v, --verbose`|Explicar lo que se está haciendo.|


<br>
# Opciones - usadas

|Opción|Descripción|
|--|--|
|`-a, --archive`|Los mismo que `-dR --preserve=all`.|
|`--attributes-only`| No copia los datos del archivo, sólo sus atributos.|
|`--backup[=CONTROL]`|make a backup of each existing destination file|
||The  backup  suffix is '~', unless set with --suffix or SIMPLE_BACKUP_SUFFIX.  The version control method may be selected via the --backup option or through the VERSION_CONTROL environment variable.<br>Here are the values:<br><br>one, off<br>never make backups (even if --backup is given)<br>numbered, t<br>make numbered backups<br>existing, nil<br>numbered if numbered backups exist, simple otherwise<br>simple, never<br>  always make simple backups<br>As a special case, cp makes a backup of SOURCE when the force and backup options are given and SOURCE and DEST are the same name for an existing, regular file.|
|`-b`|like --backup but does not accept an argument|
|`--copy-contents`|copy contents of special files when recursive|
|`-d`|same as --no-dereference --preserve=links|
|`-i, --interactive`|prompt before overwrite (overrides a previous -n option)|
|`-H`|follow command-line symbolic links in SOURCE|
|`-l, --link`|hard link files instead of copying|
|`-L, --dereference`|always follow symbolic links in SOURCE|
|`-p`|same as --preserve=mode,ownership,timestamps|
|`--preserve[=ATTR_LIST]`|preserve the specified attributes (default: mode,ownership,timestamps), if possible additional attributes: context, links, xattr, all|
|`--no-preserve=ATTR_LIST`|don't preserve the specified attributes|
|`--parents`|use full source file name under DIRECTORY|
|`--reflink[=WHEN]`|control clone/CoW copies. See below|
|`--remove-destination`|remove each existing destination file before attempting to open it (contrast with --force)|
|`--sparse=WHEN`|control creation of sparse files. See below|
|`--strip-trailing-slashes`|remove any trailing slashes from each SOURCE argument|
|`-S, --suffix=SUFFIX`|override the usual backup suffix|
|`-t, --target-directory=DIRECTORY`|copy all SOURCE arguments into DIRECTORY|
|`-T, --no-target-directory`|treat DEST as a normal file|
|`-x, --one-file-system`|stay on this file system|
|`-Z`|set SELinux security context of destination file to default type
|--context[=CTX]|like -Z, or if CTX is specified then set the SELinux or SMACK security context to CTX|
|`--help`|Muestra esta ayuda y sale|
|`--version`|Muestra información sobre la versión y sale|

       By default, sparse SOURCE files are detected by a crude heuristic and the corresponding DEST file is made sparse as well.  That is the behavior selected by --sparse=auto.  Specify --sparse=always to
       create a sparse DEST file whenever the SOURCE file contains a long enough sequence of zero bytes.  Use --sparse=never to inhibit creation of sparse files.

       When --reflink[=always] is specified, perform a lightweight copy, where the data blocks are copied only when modified.  If this is not possible the copy fails, or  if  --reflink=auto  is  specified,
       fall back to a standard copy.

       The  backup  suffix is '~', unless set with --suffix or SIMPLE_BACKUP_SUFFIX.  The version control method may be selected via the --backup option or through the VERSION_CONTROL environment variable.
       Here are the values:

       none, off
              never make backups (even if --backup is given)

       numbered, t
              make numbered backups

       existing, nil
              numbered if numbered backups exist, simple otherwise

       simple, never
              always make simple backups

       As a special case, cp makes a backup of SOURCE when the force and backup options are given and SOURCE and DEST are the same name for an existing, regular file.

<br>
<!-- Ejemplos post -->
# Ejemplos


>Cuando no sepas cómo usar un comando en Linux, hay un manual al que puede referirse escribiendo:
`man [insert command here]` en una terminal.


## 1. Ejecutamos **cp** sin ninguna opción

Este es un uso muy básico del comando cp. Para copiar un archivo llamado file.txt desde un directorio a otro directorio, podemos escribir algo así: 
```
$ cp file.txt ~/Documents/
```
Si no escribimos una ruta absoluta, significa que estamos copiando un archivo del directorio actual. En el ejemplo anterior **file.txt** se encuentra en **/home/user/desktop/** y no hemos tecleado su ruta completa ya que nos encontramos en ese directorio. Mientras que **~/Documents/** es una carpeta donde se copiará el archivo.


> Linux es sensible a mayúsculas y minúsculas además de necesitar el carácter `/` después de cada directorio para saber que no trabaja con un archivo.

> `~` es un carácter especial en el terminal que se evalúa automáticamente como el directorio inicial del usuario actual.

> Si necesita saber en qué directorio se encuentra, utilice el comando `pwd`.

> Además, para completar automáticamente las rutas de archivo largas al escribir en el terminal, puede pulsar `tab` después de haber empezado a escribir la ruta y se le presentarán opciones para elegir, o insertará la parte restante de la ruta.

## 2. Copiamos **múltiples archivos** al mismo tiempo


Para copiar multiples archivos en el mismo tiempo podemos solamente poner los archivos al comienzo del comando `cp` separados por espacios. Aquí tenemos el ejemplo:
```
$ cp file_1.txt file_2.txt file_3.txt ~/Documents/
```
## 3. Copiamos un **directorio**

Copiar un directorio es un poco complicado. Debe agregarse la opción `-r` o `-R` que significa recursividad. <ins>Esta opción es obligatoria tanto si el directorio esta vacío como si no lo esta</ins>. Aquí tenemos un ejemplo:
```
$ cp -r directory_1/ ~/Documents/
```

## 4. Crea **enlace duro** a un archivo en lugar de copiarlo

Copiar archivos significa que debes tener algo de espacio de almacenamiento para guardar estos archivos copiados. A veces, por alguna razón, es posible que quieras crear un "acceso directo" o enlace a los archivos en lugar de copiarlos. Para hacer esto puedes usar la opción `l`:
```
$ cp -l file_4.txt ~/Documents/
```
Esto hará que el archivo copiado tenga el mismo inodo, básicamente si modificas el archivo copiado estarás modificando el archivo original. Si borras uno de los dos archivos tendrás el otro como copia de seguridad. <ins>Tenga en cuenta que los enlaces duros no se pueden crear en directorios</ins>. 

## 5. Crear **enlace simbólico** en un archivo

Este es otro tipo de enlace llamados enlaces suaves o enlaces simbólicos. Usamos la opción `-s` para hacer esto. Aquí tenemos un ejemplo del comando:
```
$ cp -s /home/user/Documents/file_6.txt file_6.txt
```
<ins>La creación de enlaces simbólicos sólo se puede hacer en el directorio actual</ins>. 

A continuación, al listar el archivo copiado con detalle, verá que **file_6.txt** apunta al archivo original. <ins>Estará marcado con un signo de flecha después del nombre del archivo</ins>.

## 6. Copiar sin seguir los **enlaces simbólicos en la FUENTE**
Para hacer esto podemos usar la opción `-P`. Cuando el comando cp encuentra un archivo con un enlace simbólico lo copiará como está. Echa un vistazo al ejemplo siguiente:
```
$ cp -P file_6.txt ~/movies/
```

Como verás el comando cp copiará el archivo **file_6.txt** como está. El tipo de archivo sigue siendo enlace simbólico.

## 7. Copy with following symbolic links in Source

Now we can do this with -L option. Basically, this is an opposite of -P option above. Here’s the sample.

    $ cp -L file_6.txt ./movie

Copy using -L option

With this option, the copied file is the same file with the source file of file_6.txt. This is known from the file size. The copied file has 50 bytes file size while the file_6.txt as symbolic link has 33 bytes file size.
8. Archive the files

When we are going to copy a directory, we will use -r or -R option. But we can also use -a option to archive file. This will create an exact copy of files and directories including symbolic links if any. Here’s a sample :

    $ cp -a directory_1/ /home/pungki/office

Copy using -a option

The above command will copy a directory named directory_1 into folder /home/pungki/office. As you can see, the file_6.txt still copied as symbolic links.
9. Explain what is being done

By default, when copying activity is success, we will see a command prompt again. If you want to know what happen during the copying file, we can use -v option.

    $ cp -v *.txt /home/pungki/office

Verbose option

When we copying all txt files in current directory to /home/pungki/office/ directory, -v option will show what is being done. This additional information will make us more sure about the copying activity.
10. Copy only when the source file is newer

To do this, we can use -u option. Take a look this example below.

    $ cp -vu *.txt /home/pungki/office

Copy only if newer

In the beginning, we see file_1.txt has 0 bytes file size. Then we edit it using vi, add some content and save it. Next, we see the file size has changed into 36 bytes.
Meanwhile in /home/pungki/office directory, we already have all *.txt files. When we use -u option, combine with -v option to see what is being done, cp command will only copy a file(s) which is newer from destination directory. As the result, we see that only file_1.txt is copied into /home/pungki/office directory.
11. Use interactive mode

Interactive mode will ask if the destination folder have already the file. To activate interactive mode, use -i option.

    $ cp -ir directory_1/ /home/pungki/office/

Interactive mode
12. Create backup date of each copied file

When the destination folder already have the file, by default cp command will overwrite the same file in the destination directory. Using --backup option, cp command will make a backup of each existing destination file. ../office will refer to /home/pungki/office. Here’s a sample :

    $ cp --backup=simple -v *.txt ../office

Backup option

As we can see, --backup=simple option will create a backup file which marked by a tilde sign (~) at the end of the file. --backup option has some Control, which are :

    none, off : never backups (even if --backup is given)
    numbered, t : make numbered backups
    existing, nil : numbered if numbered backup exist, simple otherwise
    simple, never : always make simple backups

13. Copy only file attributes

Cp command also provide us with --attributes-only option. As we can guess from its name, this option will only copy a file name and its attributes without copying any data. Here’s a sample.

    $ cp --attributes-only file_6.txt -v ../office

Copy attributes only

From screenshot above, the original file_6.txt file has 50 bytes file size. Using --attributes-only option, the copied file will have 0 bytes file size. This is because the content of file is not being copied.
14. Force copying

Using -f option will force the copying activity. If the destination files cannot be opened, then -f will try again.

    $ cp -f *.txt -v ../office

Copy with force
15. Remove destination before copy

To do this, we can use --remove-destination option. This option is contrast with -f option above. If the cp command find the same file name on the destination folder, cp command will remove destination file first, the copy the new one. Here’s an example.

    $ cp --remove-destination *.txt -v ../office

Remove destination option