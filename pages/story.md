---
layout: archive
title: My Story
lang: en
permalink: /story/
---

<h2>My Story Chapters</h2>

<p>How the work evolved, what changed, and what became reusable.</p>

{% assign sorted_story = site.story | where_exp: "chapter", "chapter.lang == 'en'" | sort: 'sequence' %}
{% for chapter in sorted_story %}
  {% include story-card.html chapter=chapter %}
{% endfor %}