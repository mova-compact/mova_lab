---
layout: home
title: Home
lang: en
---

<div class="intro-block">
  <h1>MOVA Lab</h1>
  <p><strong>MOVA Lab is a lab for contract-based AI systems for business.</strong></p>
  <p>I design and build AI solutions that do more than answer prompts. They execute specific business processes within controlled boundaries: with rules, result verification, an action log, and clear responsibility.</p>
  <p>The goal of MOVA Lab is to help businesses use artificial intelligence not as a chaotic chat assistant, but as a managed working tool.</p>
</div>

<div class="navigation-block">
  <h2>What I Do</h2>
  <h3>Business Process Consulting</h3>
  <p>I help break down a real process: where it contains manual routine, where human judgment is required, where AI can be used, and where automation would be unsafe or unnecessary.</p>
  <p>The result of this stage is not an abstract “AI idea”, but a clear operating scheme: what can be automated, what data is required, what actions are allowed, where human control must stay in place, and how the result should be checked.</p>

  <h3>Contract-Based AI Products</h3>
  <p>I build systems in which AI work is described through a contract: input data, allowed actions, limits, checks, outputs, and execution trace.</p>
  <p>This approach matters where personal data, money, client communication, external services, business reputation, or process repeatability are involved.</p>

  <h3>Specialized Assistants</h3>
  <p>I create narrow AI assistants for specific roles: marketing analysis, reporting, client classification, request handling, content preparation, and process control.</p>
  <p>The core principle is simple: an assistant should not have free power over the business. It operates inside a defined process and does not perform risky actions without permission.</p>
</div>

<div class="mova-block">
  <h2>Why This Matters</h2>
  <p>Most businesses do not need “magic AI”. They need a system that reliably performs simple but important work:</p>
  <ul>
    <li>collects data every day;</li>
    <li>analyzes changes;</li>
    <li>prepares a report;</li>
    <li>finds mistakes;</li>
    <li>reminds the team about required actions;</li>
    <li>supports decision-making;</li>
    <li>does not interfere where it was not asked to act.</li>
  </ul>
  <p>That is exactly why a contract-based approach is needed.</p>
  <p>A contract does not make an AI system unnecessarily complicated. It makes it suitable for real business work.</p>
</div>

<div class="story-block">
  <h2>MOVA</h2>
  <p>MOVA is a language and method for describing controlled AI actions.</p>
  <p>Its role is to connect intent, rules, execution, and verification into one clear chain:</p>
  <p><strong>intent → contract → policy → execution → verification</strong></p>
  <p>This makes it possible not just to ask a model to do something, but to define boundaries: what it can do, with what data, through which tools, under what conditions, and what outcome should count as correct.</p>
  <a href="{{ '/projects/mova/' | relative_url }}">Learn more about MOVA</a>
</div>

<div class="projects-block">
  <h2>Who This Is For</h2>
  <p>MOVA Lab is useful for founders, marketers, local businesses, service companies, and teams that want to introduce AI carefully, practically, and without unnecessary noise.</p>
  <p>Especially where AI needs to interact with real data, clients, money, external services, or recurring business reporting.</p>
</div>

<div class="recent-posts">
  <h2>Current Focus</h2>
  <p>The current focus is practical business automation:</p>
  <ul>
    <li>daily reports in Telegram;</li>
    <li>marketing and competitor data analysis;</li>
    <li>content preparation;</li>
    <li>control of recurring processes;</li>
    <li>safe work with client data;</li>
    <li>turning manual routine into a verifiable process.</li>
  </ul>
</div>

<div class="navigation-block">
  <h2>Principle</h2>
  <p>I do not sell “artificial intelligence for the sake of artificial intelligence”.</p>
  <p>I build systems with a clear task, clear boundaries, a concrete result, and verification.</p>
  <p>If a process can be automated simply, it should be automated simply.</p>
  <p>If a process is dangerous, it should be constrained by a contract.</p>
  <p>If automation does not create useful value, it should not be done.</p>
</div>

<div class="story-block">
  <h2>Featured Story</h2>
  {% assign featured_story = site.story | where: "featured", true | first %}
  {% if featured_story %}
    <article class="story-card">
      <h3><a href="{{ featured_story.url }}">{{ featured_story.title }}</a></h3>
      <p>{{ featured_story.summary }}</p>
    </article>
  {% endif %}
  <a href="{{ '/story/' | relative_url }}">Read the story</a>
</div>

<div class="projects-block">
  <h2>Featured Projects</h2>
  {% assign featured_projects = site.projects | where: "featured", true | limit: 3 %}
  {% for project in featured_projects %}
    <article class="project-card">
      <h3><a href="{{ project.url }}">{{ project.title }}</a></h3>
      <p>{{ project.summary }}</p>
    </article>
  {% endfor %}
  <a href="{{ '/projects/' | relative_url }}">View all projects</a>
</div>

<div class="recent-posts">
  <h2>Recent Publications</h2>
  {% assign recent_posts = site.posts | limit: 5 %}
  {% for post in recent_posts %}
    <article class="post-card">
      <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
      <p>{{ post.excerpt }}</p>
      <time>{{ post.date | date: "%B %d, %Y" }}</time>
    </article>
  {% endfor %}
  <a href="{{ '/articles/' | relative_url }}">View all articles</a>
</div>
