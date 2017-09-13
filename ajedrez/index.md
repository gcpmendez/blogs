---
layout: page
title: Ajedrez
date: "2017-08-05"
---

En está página iré indexando el conocimiento necesario para mejorar como ajedrecista. Para ello empezaré escribiendo sobre aperturas básicas, resolviendo problemas tácticos y comentando libros recomendables.


<div id="archive">

<h2>Aperturas y defensas</h2>
  <ul>
  {% for post in site.posts %}
    {% if post.layout == "chess_post" %}
      <li>
        <a href="{{ post.url }}">{{ post.title }}{% if post.layout == "writeup" %} (Book Writeup){% endif %}</a>
      </li>
    {% endif %}
  {% endfor %}
  </ul>
 
<h2>Táctica</h2>
<h2>Libros</h2>



</div>


