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
ul.b {list-style-type: disc;}

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
# Contenido
Existen dos tipos de **listas** en **Markdown**, *ordenadas y desordenadas*. Para distinguir los tipos y como se crean, nada mejor que verlo con ejemplos:

<table>
  <tr>
    <th>Sintaxis Markdown</th>
    <th>Salida HTML</th>
  </tr>
  <tr>
    <td>
      Lista numerada (ordenada) <br/>
      <br/>
      1. Este es el primer elemento<br/>
      2. Este es el segundo elemento<br/>
      3. Este es el tercer elemento
    </td>
    <td>
      Lista numerada (ordenada) <br/>
      <br/>
      <ol>
        <li>Este es el primer elemento</li>
        <li>Este es el segundo elemento</li>
        <li>Este es el tercer elemento</li>
      </ol>
    </td>
  </tr>
  <tr>
      <td>
          Lista de puntos (desordenada)<br/>
          <br/>
          * Un elemento de la lista<br/>
          * Otro elemento de la lista<br/>
          * El tercer elemento de la lista
      </td>
      <td>
        Lista de puntos (desordenada)<br/>
        <br/>
        <ul class="b">
          <li>Un elemento de la lista</li>
          <li>Otro elemento de la lista</li>
          <li>El tercer elemento de la lista</li>
        </ul>
      </td>
  </tr>
  <tr>
      <td>### Esto es un H3</td>
      <td><h3>Esto es un H3</h3></td>
  </tr>
  <tr>
      <td>#### Esto es un H4</td>
      <td><h4>Esto es un H4</h4></td>
  </tr>
</table>

<br/>
