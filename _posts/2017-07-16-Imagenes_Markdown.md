---
layout: post
title: Imágenes
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
</style>

<!-- Imagen Markdown -->
# <img src="./../static/markdown.png" alt="Drawing" style="width: 170px;"/>

<!-- Contenido post -->
# Contenido
Claramente resulta bastante difícil idear una sintaxis "natural" para poner imágenes en un formato de documento de texto.

**Markdown** utiliza una sintaxis de imagen que se asemeja a la sintaxis de los enlaces, permitiendo dos estilos: *en línea y referencia*

La sintaxis de imagen en línea se muestra así:

![Alt text](/path/to/img.jpg)

![Alt text](/path/to/img.jpg "Optional title")
Esto es:

una etiqueta de exclamación: !;
seguida por un par de corchetes, que contienen el texto de la atributo alt de la imagen;
seguido por un par de paréntesis, que contienen la URL o la trayectoria a la imagen, y un atributo opcional de título (title) entre apóstrofes
La sintaxis de la imagen de estilo Referencia tiene esta apariencia:

![Alt text][id]
Donde "id" es el nombre la "identificación" de una referencia definida de la imagen. Se definen las referencias de la imagen usando la sintaxis idéntica a las referencias de los enlaces:

[id]: url/to/image  "Optional title attribute"
De momento, Markdown carece de sintaxis para especificar las dimensiones de una imagen; si esto es importante para usted, puede utilizar las etiquetas normales < img > de HTML.