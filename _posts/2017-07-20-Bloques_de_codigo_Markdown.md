---
layout: post
title: Bloques de código
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
  vertical-align: baseline;
    border: 1px solid #dddddd;
    text-align: left;
    padding: 8px;
}

th {
    text-align: center;
    width: 33.3%;
}
tr:nth-child(even) {
    background-color: rgba(238, 238, 238, 0.57);
}
td:first-child {
    font-family: 'Inconsolata', monospace;
}

td:nth-child(2) {
   
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
Los **bloques de código** pre-formateados se usan para escribir sobre el código fuente de programación o marcado. En lugar de formar párrafos normales, las líneas de un bloque de código se interpretan literalmente. Markdown envuelve un bloque de código con las etiquetas `<pre>` y `<code>`. 

Para producir un **bloque de código** en **Markdown**, <ins>simplemente indente cada línea del bloque por al menos 4 espacios o 1 tabulación</ins>. Por ejemplo, dada esta entrada:



<table>
  <tr>
    <th>Sintaxis Markdown</th>
    <th>Salida HTML</th>
  </tr>
  <tr>
    <td>This is a normal paragraph:<br/>
    &nbsp;&nbsp;&nbsp;&nbsp;This is a code block.</td>
    <td><p>This is a normal paragraph:</p><pre><code>This is a code block.
</code></pre></td>
  </tr>
</table>

<br/>


Se quita el primer nivel de identación - 4 espacios o 1 tabulación - de cada linea del bloque de código. Vemos un ejemplo de esto:

<table>
  <tr>
    <th>Sintaxis Markdown</th>
    <th>Salida HTML</th>
  </tr>
  <tr>
    <td>Here is an example of AppleScript:<br/>
<br/>
     &nbsp;&nbsp;&nbsp;&nbsp;tell application "Foo"<br/>
         &nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;beep<br/>
     &nbsp;&nbsp;&nbsp;&nbsp;end tell</td>
    <td><p>Here is an example of AppleScript:</p>

<pre><code>tell application "Foo"
     beep
end tell
</code></pre></td>
  </tr>
</table>

<br/>


> **Información:** un **bloque de código** continúa hasta que alcanza una línea que no está identada (o el final del artículo). 


Dentro de un **bloque de código**, <ins>los signos ampersand `&` y los corchetes angulares `<` y `>` se convierten automáticamente en entidades HTML</ins>. Esto hace que sea muy fácil incluir código fuente HTML de ejemplo con Markdown - sólo pegarlo y identarlo, y Markdown se encargará de la molestia de codificar los signos y los corchetes angulares. Veamoslo con un ejemplo:

<table>
  <tr>
    <th>Sintaxis Markdown</th>
    <th>Salida HTML</th>
  </tr>
  <tr>
    <td>&lt;div class="footer">
        &copy; 2004 Foo Corporation
    &lt;/div></td>
    <td><pre><code>&lt;div class="footer"&gt;
    &amp;copy; 2004 Foo Corporation
&lt;/div&gt;
</code></pre></td>
  </tr>
</table>

<br/>

> **Información:** la **sintaxis de Markdown** <ins>no se procesa dentro de los bloques de código</ins>. Por ejemplo, los asteriscos son sólo asteriscos literales dentro de un bloque de código. Esto significa que también es fácil de usar Markdown para escribir sobre la propia sintaxis de Markdown.

