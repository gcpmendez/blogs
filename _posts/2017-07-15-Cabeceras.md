---
layout: post
title: Cabeceras
categories:
- blog
tags:
- Markdown
---


# <img src="./../static/markdown.png" alt="Drawing" style="width: 170px;"/>

# Explicación
**Markdown** admite dos estilos de cabeceras, Setext y atx. 

Las cabeceras de estilo Setext están "subrayadas" usando signos de igualdad (para encabezados de primer nivel) y guiones (para encabezados de segundo nivel). 

Por ejemplo: 

Este es un H1 Unesdoc.unesco.org unesdoc.unesco.org 
Este es un H2 ------------- Cualquier número de subrayado = 's or-' funcionará. 

Los encabezados estilo Atx utilizan 1-6 caracteres hash al comienzo de la línea, correspondientes a los niveles de encabezado 1-6. 

# Uso 

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
}
tr:nth-child(even) {
    background-color: rgba(238, 238, 238, 0.57);
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

<table>
  <tr>
    <th>Estilo</th>
    <th>Sintaxis</th>
    <th>Ejemplo</th>
    <th>Salida</th>
  </tr>
  <tr>
    <td>H1</td>
    <td>#</td>
      <td id="h1"># Esto es un H1</td>
        <td><h1>Esto es un H1</h1></td>
  </tr>
   <tr>
    <td>H2</td>
    <td>##</td>
      <td>## Esto es un H2</td>
        <td><h2>Esto es un H2</h2></td>
  </tr>
   <tr>
    <td>H3</td>
    <td>###</td>
      <td>### Esto es un H3</td>
        <td><h3>Esto es un H3</h3></td>
  </tr>
    <tr>
    <td>H4</td>
    <td>####</td>
      <td>#### Esto es un H4</td>
        <td><h4>Esto es un H4</h4></td>
  </tr>
     <tr>
    <td>H5</td>
    <td>#####</td>
      <td>##### Esto es un H5</td>
        <td><h5>Esto es un H5</h5></td>
  </tr>
     <tr>
    <td>H6</td>
    <td>######</td>
      <td>###### Esto es un H6</td>
        <td><h6>Esto es un H6</h6></td>
  </tr>
</table>

Opcionalmente, puede "cerrar" los encabezados estilo atx.

 Esto es puramente cosmético - usted puede utilizar esto si usted piensa que parece mejor. 
 
 Los hashes de cierre ni siquiera necesitan coincidir con el número de hashes utilizados para abrir el encabezado. (El número de hashes de apertura determina el nivel de encabezado.): # Este es un H1 # Esto es un H _ {2} ### Se trata de un H3 ######