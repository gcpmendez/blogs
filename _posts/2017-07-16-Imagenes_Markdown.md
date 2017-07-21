---
layout: post
title: Imágenes
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
  vertical-align: middle;
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
Claramente resulta bastante difícil idear una sintaxis "natural" para poner **imágenes** en un formato de documento de texto.

**Markdown** utiliza una sintaxis de **imagen** que se asemeja a la sintaxis de los **enlaces**. <ins>Sólo deberás añadir un símbolo de exclamación `!` al principio y el enlace no será otro que la *ubicación de la imagen*</ins>. Permite al igual que el **enlace** dos estilos: *en línea y referencia*

La sintaxis de **imagen** en estilo *en línea* es la siguiente:

<table>
  <tr>
    <th>Sintaxis Markdown</th>
    <th>Salida HTML</th>
  </tr>
  <tr>
    <td>![Alt text](/path/to/img.jpg)</td>
    <td><img src="./../static/markdownExample.png" alt="Alt text" style="width: 170px;"/></td>
  </tr>
  <tr>
    <td>![Alt text](/path/to/img.jpg "Optional title")</td>
    <td><img src="./../static/markdownExample.png" alt="Alt text" style="width: 170px;" title="Optional title"/></td>
  </tr>
</table>

<br/>
La sintaxis de **imagen** con estilo *referencia* es la siguiente:


<table>
  <tr>
    <th>Sintaxis Markdown</th>
    <th>Salida HTML</th>
  </tr>
  <tr>
    <td>
    ![Alt text][id]<br/>
    [id]: url/to/image  "Optional title attribute"
    </td>
    <td><img src="./../static/markdownExample.png" alt="Alt text" title="Optional title attribute" style="width: 170px;"/></td>
  </tr>
</table>

<br/>

<ins>Se definen las referencias de la imagen usando una sintaxis idéntica a las referencias de los enlaces.</ins>  

>**Información:** por el momento, **Markdown** *carece de sintaxis para especificar las dimensiones de una imagen*; si esto es importante para usted, puede utilizar las etiquetas normales `<img></img>` de HTML.