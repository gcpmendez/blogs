---
layout: post
title: Escapes de barra invertida
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

.f {
    font-family: 'Inconsolata', monospace;
    font-size: 0.67em;
    color: #333;
}
</style>

<!-- Imagen Markdown -->
# <img src="./../static/markdown.png" alt="Drawing" style="width: 170px;"/>

<!-- Contenido post -->
# Contenido
**Markdown** nos permite usar **escapes de barra invertida** para generar carácteres literales que de otro modo tendrían un significado especial en la sintaxis de formato de **Markdown**. Por ejemplo, <ins>si desea rodear una palabra con asteriscos literales (en lugar de una etiqueta HTML <em>), puede utilizar barras invertidas antes de los asteriscos</ins>, como vemos a continuación:

<table>
  <tr>
    <th>Sintaxis Markdown</th>
    <th>Salida HTML</th>
  </tr>
  <tr>
    <td>\*literal asterisks\*</td>
    <td>*literal asterisks*</td>
  </tr>
</table>

<br/>

**Markdown** proporciona escapes de barra invertida para los siguientes caracteres:

``` html
\   backslash
`   backtick
*   asterisk
_   underscore
{}  curly braces
[]  square brackets
()  parentheses
#   hash mark
+   plus sign
-   minus sign (hyphen)
.   dot
!   exclamation mark
```




