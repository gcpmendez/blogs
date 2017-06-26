---
layout: post
title: Archivos
skip_related: true
---

{% assign totalwords = 0 %}
{% for post in site.posts %}
  {% assign wordcount = post.content | number_of_words %}
  {% assign totalwords = totalwords | plus: wordcount %}
{% endfor %}

Desde {{ site.posts.last.date | date: "%B %d, %Y" }}, he escrito {{ totalwords }} palabras sobre desarrollo web, herramientas de desarrollo, desarrollo de sofware, ... . Espero que te hayas disfrutado leyendo algunas de esas palabras. Mis publicaciones favoritas se encuentran en negrita en la página principal.


<div id="archive">
{% for post in site.posts %}
  {% assign currentdate = post.date | date: "%Y" %}
  {% if currentdate != date %}
    {% unless forloop.first %}</ul>{% endunless %}
<h2>{{ currentdate }}</h2>
<ul>
    {% assign date = currentdate %}
  {% endif %}
  <li {% if post.favorite and post.layout != "writeup" %}class="favorite"{% endif %}>
    <a href="{{ post.url }}">{{ post.title }}{% if post.layout == "writeup" %} (Book Writeup){% endif %}</a>
  </li>
  {% if forloop.last %}</ul>{% endif %}
{% endfor %}
</div>


