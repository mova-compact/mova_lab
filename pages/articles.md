---
layout: archive
title: Articles
lang: en
permalink: /articles/
---

<h1>Publications</h1>

<p>This section brings together articles, notes, and working texts about artificial intelligence, business processes, contract-based systems, automation, and the practical use of agents.</p>

<p>This is not a blog about AI news for the sake of news. What interests me is something else: which changes actually affect business, which approaches can be applied in practice, and where there is more noise around a technology than useful value.</p>

<h2>What These Texts Are About</h2>

<h3>AI in Business</h3>

<p>How to use artificial intelligence not as a fashionable feature, but as a tool for specific work: analysis, reporting, decision preparation, data processing, and support for client processes.</p>

<h3>Contract-Based Approach</h3>

<p>When AI works with data, clients, money, or external services, it needs boundaries.</p>

<p>In these texts, I explain how a contract helps describe allowed actions, rules, checks, responsibility, and result.</p>

<h3>Agents and Control</h3>

<p>Agents can be useful when they have a clear role and a clear process.</p>

<p>I examine where an agent genuinely helps and where it is better to keep a normal automation, a simple script, or a human decision.</p>

<h3>Practical Cases</h3>

<p>Some of these texts are analyses of real or experimental scenarios: local business, marketing, content, reporting, client data, media, and service processes.</p>

<p>What matters to me is not only describing an idea, but showing how it can be turned into a verifiable working loop.</p>

<h2>How to Read</h2>

<p>These texts are better read not as final truths, but as working materials of a lab.</p>

<p>Each publication should help answer at least one practical question:</p>

<ul>
  <li>what here is a real signal and what is noise;</li>
  <li>where AI is genuinely useful;</li>
  <li>what boundaries are needed for safe work;</li>
  <li>what can already be built now;</li>
  <li>what is better not to build at all.</li>
</ul>

<p>The main criterion is simple: after reading the text, it should be clearer what to do next.</p>

{% assign sorted_posts = site.posts | where_exp: "post", "post.lang == 'en'" | sort: 'date' | reverse %}
{% for post in sorted_posts %}
  {% include content-card.html item=post %}
{% endfor %}
