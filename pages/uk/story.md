---
layout: archive
title: Моя історія
lang: uk
permalink: /uk/story/
---

<h2>Розділи історії</h2>

<p>Як розвивалася робота, що змінилося і що стало повторно використовуваним.</p>

{% assign sorted_story = site.story | where_exp: "chapter", "chapter.lang == 'uk'" | sort: 'sequence' %}
{% for chapter in sorted_story %}
  {% include story-card.html chapter=chapter %}
{% endfor %}
