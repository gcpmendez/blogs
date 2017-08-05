---
layout: post
title: Metadatos del documento
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
    <td>&lt;head&gt;</td>
    <td>Representa una <b>colección de metadatos</b> acerca del documento, incluyendo enlaces a, o definiciones de, scripts y hojas de estilo.</td>
  </tr>
  <tr>
    <td>&lt;title&gt;</td>
    <td>Define el título del documento, el cual se muestra en la barra de título del navegador o en las pestañas de página. Solamente puede contener texto y cualquier otra etiqueta contenida no será interpretada.</td>
  </tr>
  <tr>
    <td>&lt;base&gt;</td>
    <td>Define la URL base para las URLs relativas en la página.</td>
  </tr>
  <tr>
    <td>&lt;link&gt;</td>
    <td>Usada para enlazar JavaScript y CSS externos con el documento HTML actual.</td>
  </tr>
  <tr>
    <td>&lt;meta&gt;</td>
    <td>Define los metadatos que no pueden ser definidos usando otro elemento HTML.</td>
  </tr>
  <tr>
    <td>&lt;style&gt;</td>
    <td>Etiqueta de estilo usada para escribir CSS en línea.</td>
  </tr>
</table>

<br/>
<!-- Ejemplo -->
# Ejemplo
En el siguiente ejemplo indicamos algunos metadatos de un documento HTML5:

<script markdown="1" src="https://gist.github.com/gcpmendez/956dce20721862b869a772761580d37b.js"></script>