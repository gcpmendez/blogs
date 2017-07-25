---
layout: post
title: Reglas horizontales
categories:
- blog
tags:
- Markdown
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
    width: 33.3%;
}
tr:nth-child(even) {
    background-color: rgba(238, 238, 238, 0.57);
}
td:first-child {
    text-align: center;
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

hr {
      border-bottom: 1px solid #000;
}
</style>

<!-- Imagen Markdown -->
# <img src="./../static/markdown.png" alt="Drawing" style="width: 170px;"/>

<!-- Contenido post -->
# Contenido
Puedes crear una etiqueta de **regla horizontal** `<hr />` <ins>colocando tres o más guiones, guiones bajos o asteriscos</ins>. Si lo desea puede utilizar espacios entre los guiones o asteriscos. Cada una de las líneas siguientes producirá una regla horizontal:

<table>
  <tr>
    <th>Sintaxis Markdown</th>
    <th>Salida HTML</th>
  </tr>
  <tr>
    <td>* * *</td>
    <td><hr/></td>
  </tr>
  <tr>
    <td>****</td>
    <td><hr/></td>
  </tr>
    <tr>
    <td>- - -</td>
    <td><hr/></td>
  </tr>
    <tr>
    <td>---------------------------------------</td>
    <td><hr/></td>
  </tr>
</table>
