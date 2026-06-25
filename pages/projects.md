---
layout: archive
title: Projects
lang: en
permalink: /projects/
---

<h2>All Projects</h2>

<p>Selected systems, products, and case studies. Cut or Die and Marketing OS are implementation examples.</p>

{% assign sorted_projects = site.projects | sort: 'date' | reverse %}
{% for project in sorted_projects %}
  {% include project-card.html project=project %}
{% endfor %}