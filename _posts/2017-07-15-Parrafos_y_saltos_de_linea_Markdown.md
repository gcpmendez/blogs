---
layout: post
title: Párrafos y saltos de línea
categories:
- blog
tags:
- Markdown
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

Un **párrafo** consiste simplemente <ins>en una o más líneas consecutivas de texto separadas por una o más líneas en blanco</ins>. Los párrafos normales no deberían sangrarse con espacios o tabulaciones.

**Markdown** se diferencia significativamente de la mayoría del resto de formateadores de texto a HTML, ya que estos traducen cada carácter de salto de línea en un párrafo encerrado en una marca `<br/>`.

Si usted desea realmente insertar una marca `<br/>` de **salto de línea** usando **Markdown**, sólo tiene que <ins>**finalizar una línea con dos o más espacios**, y a continuación pulsar la tecla de retorno.</ins>

De acuerdo a esto último resulta más costoso crear un `<br/>`, pero la regla sencilla "cada salto de línea es un `<br/>`" no funciona en **Markdown**. *El estilo de Markdown posee mejor apariencia cuando usted formatea con saltos de línea duros.*