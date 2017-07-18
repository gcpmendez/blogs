---
layout: post
title: ¿Qué es Markdown?
categories:
- blog
tags:
- Markdown
status: favorite
---


<!-- Estilo CSS del post-->
<style>
table {
    font-family: arial, sans-serif;
    border-collapse: collapse;
    width: 100%;
}

td {
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
# <img src="./../static/markdown.png" alt="Drawing" style="width: 170px;"/>

<!-- Contenido post -->
# Contenido
**Markdown** fue creado por *John Gruber* en *2004*. <ins>Su propósito es ser una sintaxis fácil de leer y escribir que se convierta fácilmente a HTML</ins> (y, actualmente, a otros formatos también). Para ello hace uso de caracteres especiales delante y después de las lineas de texto a las que deseas darles formato especial. 

**Markdown** está basado en HTML, <ins>así que cualquier archivo HTML es Markdown
válido</ins>, eso significa que <ins>podemos usar elementos HTML en Markdown como, por
ejemplo, el comentario y no serán afectado por un parseador Markdown</ins>. Aún 
así si creas un elemento HTML en tu archivo Markdown no podrás usar sintaxis
Markdown dentro de él.

<ins>La implementación de **Markdown** cambia de acuerdo al parseador.</ins>

En resumen podemos decir que HTML añade mucho ruido al texto haciéndolo sumamente difícil de leer, especialmente para gente que no esta familiarizada con él. Markdown nos permite escribir en texto sencillo con pocos adornos y lo convierte a HTML automáticamente sin necesidad de aprender un millón de instrucciones de formato.

<br/>

# Sintaxis Markdown

* Bloques de elementos
  * [Párrafos y saltos de línea](/Parrafos_y_saltos_de_linea_Markdown/)
  * [Cabeceras](/Cabeceras_Markdown/)
  * [Citas](/Citas_Markdown/)
  * [Listas](/Listas_Markdown/)
  * Code Blocks
  * Horizontal Rules
* Span Elements
  * Links
  * Emphasis
  * Code
  * Images
* Miscellaneous
  * Backslash Escapes
  * Automatic Links

<br/>

# Documentación oficial

https://daringfireball.net/projects/markdown/syntax