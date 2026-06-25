---
layout: archive
title: Проєкти
lang: uk
permalink: /uk/projects/
---

<h2>Усі проєкти</h2>

<p>Вибрані системи, продукти та кейси. Cut or Die і Marketing OS — приклади реалізації.</p>

{% assign sorted_projects = site.projects | sort: 'date' | reverse %}
{% for project in sorted_projects %}
  {% include project-card.html project=project %}
{% endfor %}
