---
layout: archive
title: Articles
lang: en
permalink: /articles/
---

<h2>All Articles</h2>

<p>Notes, essays, and working materials on contract AI, Hermes, MOVA, and business process design.</p>

{% assign sorted_posts = site.posts | where_exp: "post", "post.lang == 'en'" | sort: 'date' | reverse %}
{% for post in sorted_posts %}
  {% include content-card.html item=post %}
{% endfor %}