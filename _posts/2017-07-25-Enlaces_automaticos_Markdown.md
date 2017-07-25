---
layout: post
title: Enlaces automáticos
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
}

th:first-child {
    text-align: center;
    width: 25%;
}

th:nth-child(2) {
    text-align: center;
    width: 25%;
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
**Markdown** admite un estilo de acceso directo para crear **enlaces "automáticos"** para direcciones URL y direcciones de correo electrónico: <ins>simplemente rodee la dirección URL o la dirección de correo electrónico con corchetes angulares</ins>. Lo que esto significa es que si desea mostrar el texto real de una URL o dirección de correo electrónico y también que se haga clic en un vínculo, puede hacer lo siguiente:

<table>
  <tr>
    <th>Sintaxis Markdown</th>
    <th>Salida HTML</th>
  </tr>
  <tr>
    <td><http://example.com/></td>
    <td><a href="http://example.com/">http://example.com/</a></td>
  </tr>
</table>

<br/>

Los **enlaces automáticos** para direcciones de correo electrónico funcionan de manera similar, excepto que <ins>**Markdown** también realizará un poco de codificación aleatoria de entidades decimales y hexadecimales para ayudar a ocultar su dirección a los bots de recolección de direcciones</ins>. Por ejemplo, **Markdown** actuará así:

<table>
  <tr>
    <th>Sintaxis Markdown</th>
    <th>Salida HTML</th>
  </tr>
  <tr>
    <td><address@example.com></td>
    <td><a href="&#x6D;&#x61;i&#x6C;&#x74;&#x6F;:&#x61;&#x64;&#x64;&#x72;&#x65;
&#115;&#115;&#64;&#101;&#120;&#x61;&#109;&#x70;&#x6C;e&#x2E;&#99;&#111;
&#109;">&#x61;&#x64;&#x64;&#x72;&#x65;&#115;&#115;&#64;&#101;&#120;&#x61;
&#109;&#x70;&#x6C;e&#x2E;&#99;&#111;&#109;</a></td>
  </tr>
</table>

<br/>

<table>
  <tr>
    <th>Código HTML de salida</th>
  </tr>
  <tr>
<td><code>&lt;a href=&quot;&amp;#x6D;&amp;#x61;i&amp;#x6C;&amp;#x74;&amp;#x6F;:&amp;#x61;&amp;#x64;&amp;#x64;&amp;#x72;&amp;#x65;
&amp;#115;&amp;#115;&amp;#64;&amp;#101;&amp;#120;&amp;#x61;&amp;#109;&amp;#x70;&amp;#x6C;e&amp;#x2E;&amp;#99;&amp;#111;
&amp;#109;&quot;&gt;&amp;#x61;&amp;#x64;&amp;#x64;&amp;#x72;&amp;#x65;&amp;#115;&amp;#115;&amp;#64;&amp;#101;&amp;#120;&amp;#x61;
&amp;#109;&amp;#x70;&amp;#x6C;e&amp;#x2E;&amp;#99;&amp;#111;&amp;#109;&lt;/a&gt;</code></td>
  </tr>
</table>
<br/>

 > **Información:** Este tipo de truco de codificación de entidad engañará a muchos, si no a la mayoría, de los bots de recolección de direcciones, pero definitivamente no los engañará a todos. Es mejor que nada, **pero una dirección publicada de esta manera probablemente comenzará a recibir correo no deseado**.
