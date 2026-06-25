---
layout: archive
title: Статті
lang: uk
permalink: /uk/articles/
---

<h2>Усі статті</h2>

<p>Нотатки, есе та робочі матеріали про контрактний ШІ, Hermes, MOVA і дизайн бізнес-процесів.</p>

{% assign sorted_posts = site.posts | where_exp: "post", "post.lang == 'uk'" | sort: 'date' | reverse %}
{% for post in sorted_posts %}
  {% include content-card.html item=post %}
{% endfor %}
