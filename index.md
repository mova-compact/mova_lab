---
layout: home
title: Home
lang: en
---

<div class="intro-block">
  <h1>Contract-bound AI systems for business</h1>
  <p>I design and implement AI systems that fit real business processes: consulting, contract-driven products, and specialized assistants built with Hermes and MOVA.</p>
</div>

<div class="navigation-block">
  <h2>Explore</h2>
  <ul>
    <li><a href="/articles/">Articles & Publications</a></li>
    <li><a href="/story/">My Story</a></li>
    <li><a href="/projects/">Projects</a></li>
    <li><a href="/about/">About</a></li>
    <li><a href="/uk/">Українська версія</a></li>
  </ul>
</div>

<div class="mova-block">
  <h2>MOVA Ecosystem</h2>
  <p>MOVA is my contract language and execution model for business-grade AI systems.</p>
  <a href="/projects/mova/">Learn more about MOVA</a>
</div>

<div class="story-block">
  <h2>Products</h2>
  <p>Consulting, productized contract AI, and specialized Hermes executors.</p>
</div>

<div class="story-block">
  <h2>Case studies</h2>
  {% assign featured_story = site.story | where: "featured", true | first %}
  {% if featured_story %}
    <article class="story-card">
      <h3><a href="{{ featured_story.url }}">{{ featured_story.title }}</a></h3>
      <p>{{ featured_story.summary }}</p>
    </article>
  {% endif %}
  <a href="/story/">Read my story</a>
</div>

<div class="projects-block">
  <h2>Selected Products</h2>
  {% assign featured_projects = site.projects | where: "featured", true | sort: 'title' | limit: 3 %}
  {% for project in featured_projects %}
    {% include project-card.html project=project %}
  {% endfor %}
  <a href="/projects/">View all projects</a>
</div>

<div class="projects-block">
  <h2>Implementation Examples</h2>
  {% assign case_studies = site.projects | where_exp: "project", "project.project_type == 'Case Study'" | sort: 'title' %}
  {% for project in case_studies %}
    {% include project-card.html project=project %}
  {% endfor %}
</div>

<div class="recent-posts">
  <h2>Recent Publications</h2>
  {% assign recent_posts = site.posts | where_exp: "post", "post.lang == 'en'" | sort: 'date' | reverse | limit: 5 %}
  {% for post in recent_posts %}
    <article class="post-card">
      <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
      <p>{{ post.excerpt }}</p>
      <time>{{ post.date | date: "%B %d, %Y" }}</time>
    </article>
  {% endfor %}
  <a href="/articles/">View all articles</a>
</div>