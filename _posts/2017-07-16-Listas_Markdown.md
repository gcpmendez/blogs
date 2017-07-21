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
  vertical-align: baseline;
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
      <td>
          Se pueden emplear también + y - en vez de *<br/>
          <br/>
          * Un elemento de la lista<br/>
          + Otro elemento de la lista<br/>
          - El tercer elemento de la lista
      </td>
      <td>
        Se pueden emplear también + y - en vez de *<br/>
        <br/>
        <ul class="b">
          <li>Un elemento de la lista</li>
          <li>Otro elemento de la lista</li>
          <li>El tercer elemento de la lista</li>
        </ul>
      </td>
  </tr>
  <tr>
      <td>
      Se pueden mezclar distintos tipos de listas y anidar unas dentro de otras.<br/>
      <br/>
      1. Esto es una lista ordenada<br/>
      2. Segundo elemento de la lista ordenada<br/>
        <span style="padding-left:2em">1. Esta es una lista ordenada anidada dentro de otra</span><br/>
          <span style="padding-left:4em">* Lista desordenada anidada a tercer nivel</span><br/>
          <span style="padding-left:4em">* Segundo elemento de esta lista</span><br/>
        <span style="padding-left:2em">2. Este es el segundo elemento de la lista ordenada anidada</span>
      </td>
      <td>
      Se pueden mezclar distintos tipos de listas y anidar unas dentro de otras.<br/>
      <br/>
      <ol>
        <li>Esto es una lista ordenada</li>
        <li>Segundo elemento de la lista ordenada</li>
        <ol>
          <li>Esta es una lista ordenada anidada dentro de otra</li>
          <ul class="b">
            <li>Lista desordenada anidada a tercer nivel</li>
            <li>Segundo elemento de esta lista</li>
          </ul>
          <li>Este es el segundo elemento de la lista ordenada anidada</li>
        </ol>
      </ol>
</td>
  </tr>
</table>

<br/>
