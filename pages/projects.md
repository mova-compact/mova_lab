---
layout: archive
title: Projects
lang: en
permalink: /projects/
---

<h1>Projects</h1>

<p>This section brings together MOVA Lab products, case studies, and working experiments.</p>

<p>I do not separate projects into “ideas” and “presentations”. What matters to me is whether they produce a verifiable result: a working prototype, a contract, a process, a report, an automation, or a real implementation case.</p>

<h2>Main Directions</h2>

<h3>Business Automation</h3>

<p>Practical systems that perform regular work for a small business or team:</p>

<ul>
  <li>daily reports;</li>
  <li>analytics preparation;</li>
  <li>control of recurring processes;</li>
  <li>data collection and structuring;</li>
  <li>support for client communication;</li>
  <li>preparation of decisions for a human.</li>
</ul>

<p>The main requirement is that the system must produce an observable result, not simply demonstrate AI capabilities.</p>

<h3>Contract-Based AI Systems</h3>

<p>Projects where AI work is constrained by a contract: defined input data, allowed actions, rules, checks, boundaries of responsibility, and an execution log.</p>

<p>This direction matters where a system works with client data, money, external services, recurring reports, or actions that can affect the business.</p>

<h3>Specialized Assistants</h3>

<p>Narrow assistants for specific roles and processes:</p>

<ul>
  <li>marketing analysis;</li>
  <li>competitor analysis;</li>
  <li>content preparation;</li>
  <li>client classification;</li>
  <li>work with internal knowledge;</li>
  <li>task execution control;</li>
  <li>decision support.</li>
</ul>

<p>Such an assistant is not a “universal employee”. It has a clear role, clear boundaries, and an expected result.</p>

<h3>MOVA</h3>

<p>MOVA is the foundation of the contract-based approach: a language, a method, and a set of rules for describing controlled AI actions.</p>

<p>Projects around MOVA show how to turn intent into a contract, a contract into execution, and execution into a verifiable result.</p>

<h2>How to Read This Section</h2>

<p>Each project should be evaluated not by the complexity of its architecture, but by three questions:</p>

<ol>
  <li>What real work does it perform?</li>
  <li>Where do the boundaries of AI actions lie?</li>
  <li>How is the result verified?</li>
</ol>

<p>If these three answers are clear, the project has practical value.</p>

<p>If not, it is not yet a system, but only an experiment.</p>

{% assign sorted_projects = site.projects | sort: 'date' | reverse %}
{% for project in sorted_projects %}
  {% include project-card.html project=project %}
{% endfor %}
