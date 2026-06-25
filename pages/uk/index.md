---
layout: home
title: Головна
lang: uk
permalink: /uk/
---

<div class="intro-block">
  <h1>Контрактний ШІ для бізнесу</h1>
  <p>Я проєктую і впроваджую AI-системи, які вбудовуються в реальні бізнес-процеси: консалтинг, продуктові контрактні рішення та спеціалізовані асистенти на базі Hermes і MOVA.</p>
</div>

<div class="navigation-block">
  <h2>Перейти</h2>
  <ul>
    <li><a href="{{ '/uk/articles/' | relative_url }}">Статті та публікації</a></li>
    <li><a href="{{ '/uk/story/' | relative_url }}">Моя історія</a></li>
    <li><a href="{{ '/uk/projects/' | relative_url }}">Проєкти</a></li>
    <li><a href="{{ '/uk/about/' | relative_url }}">Про мене</a></li>
    <li><a href="{{ '/' | relative_url }}">English version</a></li>
  </ul>
</div>

<div class="mova-block">
  <h2>Екосистема MOVA</h2>
  <p>MOVA — це моя мова контрактів і модель виконання для бізнесових AI-систем.</p>
  <a href="{{ '/projects/mova/' | relative_url }}">Дізнатися більше про MOVA</a>
</div>

<div class="story-block">
  <h2>Продукти</h2>
  <p>Консалтинг, продуктований контрактний ШІ та спеціалізовані виконавці Hermes.</p>
</div>

<div class="story-block">
  <h2>Кейси</h2>
  {% assign featured_story = site.story | where: "featured", true | first %}
  {% if featured_story %}
    <article class="story-card">
      <h3><a href="{{ featured_story.url }}">{{ featured_story.title }}</a></h3>
      <p>{{ featured_story.summary }}</p>
    </article>
  {% endif %}
  <a href="{{ '/uk/story/' | relative_url }}">Читати історію</a>
</div>

<div class="projects-block">
  <h2>Вибрані продукти</h2>
  {% assign featured_projects = site.projects | where: "featured", true | sort: 'title' | limit: 3 %}
  {% for project in featured_projects %}
    {% include project-card.html project=project %}
  {% endfor %}
  <a href="{{ '/uk/projects/' | relative_url }}">Усі проєкти</a>
</div>

<div class="projects-block">
  <h2>Приклади реалізації</h2>
  {% assign case_studies = site.projects | where_exp: "project", "project.project_type == 'Case Study'" | sort: 'title' %}
  {% for project in case_studies %}
    {% include project-card.html project=project %}
  {% endfor %}
</div>

<div class="recent-posts">
  <h2>Останні публікації</h2>
  {% assign recent_posts = site.posts | where_exp: "post", "post.lang == 'uk'" | sort: 'date' | reverse | limit: 5 %}
  {% for post in recent_posts %}
    <article class="post-card">
      <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
      <p>{{ post.excerpt }}</p>
      <time>{{ post.date | date: "%d %B %Y" }}</time>
    </article>
  {% endfor %}
  <a href="{{ '/uk/articles/' | relative_url }}">Усі статті</a>
</div>
