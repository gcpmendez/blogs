---
layout: post
title: Scripting
categories:
- blog
tags:
- HTML
---


<!-- Estilo CSS del post-->
<style>
table {
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
}
tr:nth-child(even) {
    background-color: rgba(238, 238, 238, 0.57);
}

td:first-child {
  width: 20%;
  text-align: center;
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
# <img src="./../static/HTML5.png" alt="Drawing" style="width: 170px;"/>

<!-- Contenido post -->
# Contenido

<table>
  <tr>
    <th>Elemento HTML</th>
    <th>Descripción</th>
  </tr>
  <tr>
    <td>&lt;!DOCTYPE html&gt;</td>
    <td>Define que el documento esta bajo el estandar de HTML 5</td>
  </tr>
    <tr>
    <td>&lt;html&gt;</td>
    <td>Representa la raíz de un documento HTML o XHTML. Todos los demás elementos deben ser descendientes de este elemento.</td>
  </tr>
</table>

<br/>
<!-- Ejemplo -->
# Ejemplo
El DOCTYPE usado en el siguiente ejemplo indica que es un documento HTML5.

 <script markdown='1' src="https://gist.github.com/gcpmendez/4ae1c7c7c01ef7df1f251652f7028fb5.js"></script>