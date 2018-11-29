---
layout: post
title: Énfasis
categories:
- blog
tags:
- Markdown
comments: true
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
**Markdown** usa los símbolos asterisco `*` y guion bajo `_` como indicadores de **énfasis**. <ins>El texto envuelto con un `*` o `_` será envuelto con una etiqueta HTML `<em>`; y con dobles `*’s` o `_’s` será envuelto con una etiqueta HTML `<strong>`,</ins> como vemos en la siguiente tabla:

<table>
  <tr>
    <th>Sintaxis Markdown</th>
    <th>Salida HTML</th>
  </tr>
  <tr>
    <td>
    *single asterisks*<br/><br/>
    _single underscores_<br/><br/>
    **double asterisks**<br/><br/>
    __double underscores__
    </td>
    <td>
    <em>single asterisks</em><br/><br/>
    <em>single underscores</em><br/><br/>
    <strong>double asterisks</strong><br/><br/>
    <strong>double underscores</strong>
    </td>
  </tr>  
</table>



<br/>




Puedes usar el estilo que prefieras, **la unica restricción es que se debe usar el mismo símbolo para abrir y cerrar el énfasis.**


> Información: el **énfasis** puede ser usado en medio de una palabra: en*mediodeuna*palabra. Pero si  rodea un `*` o `_` con espacios ese será mostrado como un asterisco literal o un guion bajo.

Para producir un asterisco literal o un guion bajo literal en una posición donde ha sido usado para delimitar un énfasis deberemos escaparlos como vemos a continuación:

<table>
  <tr>
    <th>Sintaxis Markdown</th>
    <th>Salida HTML</th>
  </tr>
  <tr>
    <td>
    \*this text is surrounded by literal asterisks\*
    </td>
    <td>
   *this text is surrounded by literal asterisks*
    </td>
  </tr>  
</table>

