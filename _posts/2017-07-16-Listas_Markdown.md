---
layout: post
title: Listas
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
# Explicación
Empleamos el carácter almohadilla `#` para crear las cabeceras en **Markdown**. En la siguiente tabla se pueden ver como vamos añadiendo una almohadilla por cada nivel existente:


<table>
  <tr>
    <th>Etiqueta HTML</th>
    <th>Sintaxis Markdown</th>
    <th>Salida HTML</th>
  </tr>
  <tr>
    <td>H1</td>
      <td id="h1"># Esto es un H1</td>
        <td><h1>Esto es un H1</h1></td>
  </tr>
   <tr>
    <td>H2</td>
      <td>## Esto es un H2</td>
        <td><h2>Esto es un H2</h2></td>
  </tr>
   <tr>
    <td>H3</td>
      <td>### Esto es un H3</td>
        <td><h3>Esto es un H3</h3></td>
  </tr>
    <tr>
    <td>H4</td>
      <td>#### Esto es un H4</td>
        <td><h4>Esto es un H4</h4></td>
  </tr>
     <tr>
    <td>H5</td>
      <td>##### Esto es un H5</td>
        <td><h5>Esto es un H5</h5></td>
  </tr>
     <tr>
    <td>H6</td>
      <td>###### Esto es un H6</td>
        <td><h6>Esto es un H6</h6></td>
  </tr>
</table>

<br/>

> **Información:**
> También puedes cerrar las cabeceras con el mismo número de almohadillas, por ejemplo escribiendo `### Esto es un H3 ###`. Pero la única finalidad de esto es un **motivo puramente estético**.



Existe otra manera de crear los dos primeros niveles de las cabeceras como podemos ver en la siguiente tabla:

<table>
  <tr>
    <th>Etiqueta HTML</th>
    <th>Sintaxis Markdown</th>
    <th>Salida HTML</th>
  </tr>
  <tr>
    <td>H1</td>
      <td id="h1">Esto es un H1 <br> 
      =============</td>
        <td><h1>Esto es un H1</h1></td>
  </tr>
   <tr>
    <td>H2</td>
      <td>Esto es un H2   <br>    
      -------</td>
        <td><h2>Esto es un H2</h2></td>
  </tr>

 

</table>

<br/>

> **Información:**
> No existe un número concreto de caracteres `=`'s o `-`'s que necesites escribir para que esto funcione, bastaría simplemente con uno.




<br/>

