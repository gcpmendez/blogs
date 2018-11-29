---
layout: post
title: Día 0
categories:
- blog
tags:
- Jekyll
status: notFinished
comments: true
---


<!-- Estilo CSS del post-->
<style>
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
# <img src="./../static/jekyll.png" alt="Drawing" style="width: 270px;"/>

<!-- Contenido post -->
# Contenido

Actualmente estamos trabajando en Ubuntu 18.04. 


# Instalando JEKYLL en Ubuntu 18.04

Empezaremos actualizando todo los paquetes del sistema a sus últimas versiones:

<table>
  <tr>
    <td>
    $ sudo apt update <br>
    $ sudo apt upgrade
    </td>
  </tr>  
</table>
<br>

**Jekyll** requiere un entorno de desarrollo de **Ruby** trabajando con sus librerías incluidas. Usa el siguiente comando para instalar **Jekyll** y las herramientas de contrucción requerias:

<table>
  <tr>
    <td>
    $ sudo apt install make build-essential <br>
    </td>
  </tr>  
</table>
