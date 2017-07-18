---
layout: page
title: Archivos
date: "2017-07-10"
---


{% assign totalwords = 0 %}
{% for post in site.posts %}
  {% assign wordcount = post.content | number_of_words %}
  {% assign totalwords = totalwords | plus: wordcount %}
{% endfor %}

{% assign months = "Enero|Febrero|Marzo|Abril|Mayo|Junio|Julio|Agosto|Septiembre|Octubre|Noviembre|Diciembre" | split: "|" %}
{% assign m = site.posts.last.date | date: "%-m" | minus: 1 %}
{% assign day = site.posts.last.date | date: "%d" %}
{% assign month = months[m] %}
{% assign year = site.posts.last.date | date: "%Y" %}

Desde el <ins>{{ day }} de {{ month }} de {{ year }}</ins> he escrito <ins>{{ totalwords }} palabras</ins> sobre desarrollo web, desarrollo de software, herramientas de desarrollo, entre otras cosas. Espero que hayas disfrutado leyendo algunas de esas palabras. He destacado mis publicaciones favoritas añadiendole el <b>formato de negrita</b>.


<div id="archive">
{% for post in site.posts %}
  {% assign currentdate = post.date | date: "%Y" %}
  {% if currentdate != date %}
    {% unless forloop.first %}</ul>{% endunless %}
<h2>{{ currentdate }}</h2>
<ul>
    {% assign date = currentdate %}
  {% endif %}
  <li {% case post.status %}{% when 'favorite' %}class="favorite"{% when 'notFinished' %}class="notFinished"{% endcase %}>
    <a href="{{ post.url }}">{{ post.title }}{% if post.layout == "writeup" %} (Book Writeup){% endif %}</a>
  </li>
  {% if forloop.last %}</ul>{% endif %}
{% endfor %}
</div>


