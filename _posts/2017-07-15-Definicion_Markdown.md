---
layout: post
title: ¿Qué es Markdown?
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
# Explicación
Empleamos el carácter mayor que `>` para crear **bloques de cita**. En la siguiente tabla podemos ver las opciones para crearlos:


<table>
  <tr>
    <th>Sintaxis Markdown</th>
    <th>Salida HTML</th>
  </tr>
  <tr>
    <td id="h1">
      Esto es una línea normal <br/><br/>
      > Esto es parte de un bloque de cita.<br/>
      > Esto es parte del mismo bloque de cita.
    </td>
    <td>
      Esto es una línea normal <br/>
      <blockquote>Esto es parte de un bloque de cita. Esto es parte del mismo bloque de cita.</blockquote>
    </td>
  </tr>
  <tr>
      <td>
        > Esto es parte de un bloque de cita.<br/>
        Esto continúa el bloque incluso aunque no hay símbolo 'mayor que'.<br/><br/>

        La línea en blanco finaliza el bloque.
      </td>
      <td>
        <blockquote>Esto es parte de un bloque de cita. Esto continúa el bloque incluso aunque no hay símbolo 'mayor que'.</blockquote>

      La línea en blanco finaliza el bloque.</td>
  </tr>
  <tr>
    <td>
        Esto es una línea normal<br/><br/>
        > Esto es parte de un bloque de cita.<br/>
        > Esto es parte del mismo bloque de cita.<br/>
        ><br/>
        > > Esto es otro bloque de cita anidado.<br/>
        > > Esto es parte del bloque anidado.<br/>
        ><br/>
        > Esto es parte del bloque de cita de primer nivel.
    </td>
    <td>
        Esto es una línea normal
        <br/><br/>
        <blockquote>Esto es parte de un bloque de cita. Esto es parte del mismo bloque de cita.<br/>
        <blockquote>Esto es otro bloque de cita anidado. Esto es parte del bloque anidado.<br/></blockquote>
        <br/>
        Esto es parte del bloque de cita de primer nivel.</blockquote>
    </td>
  </tr>
</table>


<br/>
