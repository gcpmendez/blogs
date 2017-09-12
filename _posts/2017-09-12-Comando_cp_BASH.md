---
layout: post
title: cp
categories:
- blog
tags:
- Bash
status: notFinished
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
    width: 20%;
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


#### NOMBRE
cp - copia archivos y directorios

#### ESQUEMA
```
       cp [OPTION]... [-T] SOURCE DEST  
       cp [OPTION]... SOURCE... DIRECTORY  
       cp [OPTION]... -t DIRECTORY SOURCE...  
```
#### DESCRIPCIÓN
  Copia FUENTE a DESTINO, o multiples FUENTE(s) a un DIRECTORIO.

  Los argumentos obligatorios para las opciones largas son obligarios también para las opciones cortas.


|Opción|Descripción|
|--|--|
|-a, --archive|same as -dR --preserve=all|
|--attributes-only| don't copy the file data, just the attributes|
|--backup[=CONTROL]|make a backup of each existing destination file|
|-b|like --backup but does not accept an argument|
|--copy-contents|copy contents of special files when recursive|
|-d|same as --no-dereference --preserve=links|
|-f, --force|if an existing destination file cannot be opened, remove it and try again (this option is ignored when the -n option is also used)|
|-i, --interactive|prompt before overwrite (overrides a previous -n option)|

       -H     follow command-line symbolic links in SOURCE

       -l, --link
              hard link files instead of copying

       -L, --dereference
              always follow symbolic links in SOURCE

       -n, --no-clobber
              do not overwrite an existing file (overrides a previous -i option)

       -P, --no-dereference
              never follow symbolic links in SOURCE

       -p     same as --preserve=mode,ownership,timestamps

       --preserve[=ATTR_LIST]
              preserve the specified attributes (default: mode,ownership,timestamps), if possible additional attributes: context, links, xattr, all

       --no-preserve=ATTR_LIST
              don't preserve the specified attributes

       --parents
              use full source file name under DIRECTORY

       -R, -r, --recursive
              copy directories recursively

       --reflink[=WHEN]
              control clone/CoW copies. See below

       --remove-destination
              remove each existing destination file before attempting to open it (contrast with --force)

       --sparse=WHEN
              control creation of sparse files. See below

       --strip-trailing-slashes
              remove any trailing slashes from each SOURCE argument

       -s, --symbolic-link
              make symbolic links instead of copying

       -S, --suffix=SUFFIX
              override the usual backup suffix

       -t, --target-directory=DIRECTORY
              copy all SOURCE arguments into DIRECTORY

       -T, --no-target-directory
              treat DEST as a normal file

       -u, --update
              copy only when the SOURCE file is newer than the destination file or when the destination file is missing

       -v, --verbose
              explain what is being done

       -x, --one-file-system
              stay on this file system

       -Z     set SELinux security context of destination file to default type

       --context[=CTX]
              like -Z, or if CTX is specified then set the SELinux or SMACK security context to CTX

       --help display this help and exit

       --version
              output version information and exit

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


<!-- Ejemplos post -->
# Ejemplos