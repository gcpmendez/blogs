---
layout: post
title: Enlaces automáticos
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
Existen dos maneras de crear **enlaces** en **Markdown**, *en línea* y *referenciado*. En ambos estilos el texto del enlace irá delimitado por corchetes `[]`. Podemos ver en la siguiente tabla la creación de este tipo de enlaces:


<table>
  <tr>
    <th>Sintaxis Markdown</th>
    <th>Salida HTML</th>
  </tr>
  <tr>
    <td>[Enlace con título](http://gcpmendez.github.io "Título del enlace")</td>
    <td><a href="http://gcpmendez.github.io" title="Título del enlace">Enlace con título</a></td>
  </tr>
  <tr>
    <td>[Enlace sin título](http://gcpmendez.github.io)</td>
    <td><a href="http://gcpmendez.github.io">Enlace sin título</a></td>
  </tr>
  <tr>
    <td>[Enlace 1][1], [Enlace 2][2], [Enlace 3][3] <br/><br/>

 [1]: http://gcpmendez.github.io/archivos <br/>
 [2]: http://gcpmendez.github.io/archivos "Archivos" <br/>
 [3]: http://gcpmendez.github.io/
 </td> 
    <td><a href="http://gcpmendez.github.io/archivos">Enlace 1</a>, <a href="http://gcpmendez.github.io" title="Archivos">Enlace 2</a>, <a href="http://gcpmendez.github.io">Enlace 3</a></td>
  </tr>
</table>

<br/>

> **Información:**
>Las siguientes tres definiciones de enlaces son equivalentes:  
><span class="f">[foo]: http://example.com/  "Optional Title Here"</span><br/>
><span class="f">[foo]: http://example.com/  'Optional Title Here'</span><br/>
><span class="f">[foo]: http://example.com/  (Optional Title Here)</span><br/>



> **Información:** El **enlace implícito** nos permite *omitir el nombre del enlace* en el caso en que el nombre del enlace sea el mismo que el usado como nombre. En este caso solo debes usar un conjunto vacio de corchetes `[]`. Por ejemplo: en enlace con la palabra "Google" referenciando el sitio web google.com se podría escribir de la siguiente manera:  
> <span class="f">[Google][]</span><br/><br/>
>Y entonces definimos en enlace como sigue:  
><span class="f">[Google]: http://google.com/</span><br/>

<br/>

