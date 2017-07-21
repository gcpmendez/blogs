---
layout: post
title: Código
categories:
- blog
tags:
- Markdown
---

<!-- Estilo CSS del post-->
<style>
ul.b {list-style-type: disc;}

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
# <img src="./../static/markdown.png" alt="Drawing" style="width: 170px;"/>

<!-- Contenido post -->
# Contenido
Para indicar en **Markdown** una etiqueta de código envolvemos el texto con el símbolo de **acento grave** `` ` ``. A diferencia de un **bloque de código** preformateado, una etiqueta de código indica el código dentro de un párrafo normal. Veamos un ejemplo:

<table>
  <tr>
    <th>Sintaxis Markdown</th>
    <th>Salida HTML</th>
  </tr>
  <tr>
    <td>
    Use the `printf()` function.
    </td>
    <td>
    <p>Use the <code>printf()</code> function.</p>
    </td>
  </tr>  
</table>

<br/>
Para incluir un símbolo de **acento grave literal** dentro de un intervalo de código puedes usar múltiples acentos graves como delimitadores al comienzo y al final, lo cual enseñamos a continuación:

<table>
  <tr>
    <th>Sintaxis Markdown</th>
    <th>Salida HTML</th>
  </tr>
  <tr>
    <td>
    ``Hay un acento grave literal (`) aquí.``
    </td>
    <td>
    <p><code>Hay un acento grave literal (`) aquí.</code></p>
    </td>
  </tr>  
</table>

<br/>

<ins>Los delimitadores del **acento grave** que rodean un intervalo de código pueden incluir espacios, uno después de la apertura y uno antes del cierre.</ins> Esto le permite colocar caracteres literales de acento grave al principio o al final de un intervalo de código:

<table>
  <tr>
    <th>Sintaxis Markdown</th>
    <th>Salida HTML</th>
  </tr>
  <tr>
    <td>
    Un simple acento grave en un intervalo de código: `` ` ``
    </td>
    <td>
    <p>Un simple acento grave en un intervalo de código: <code>`</code></p>
    </td>
  </tr>  
  <tr>
    <td>
    Una cadena delimitada por acentos graves en un intervalo de código: `` `foo` ``
    </td>
    <td>
    <p>Una cadena delimitada por acentos graves en un intervalo de código: <code>`foo`</code></p>
    </td>
  </tr> 
</table>

<br/>

<ins>En un intervalo de código, los signos ampersand y los corchetes angulares se codifican automáticamente como entidades HTML, lo que facilita incluir ejemplos de etiquetas html</ins>. Lo vemos a continuación:

<table>
  <tr>
    <th>Sintaxis Markdown</th>
    <th>Salida HTML</th>
  </tr>
  <tr>
    <td>
    Please don't use any `<blink>` tags.
    </td>
    <td>
    <p>Please don't use any <code>&lt;blink&gt;</code> tags.</p>
    </td>
  </tr>  
  <tr>
    <td>
    `&#8212;` is the decimal-encoded equivalent of `&mdash;`.
    </td>
    <td>
    <p><code>&amp;#8212;</code> is the decimal-encoded equivalent of <code>&amp;mdash;</code>.</p>
    </td>
  </tr> 
</table>


