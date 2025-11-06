---
title: Research
layout: default
permalink: /projects/
---

<h1>Research</h1>
<p>Our research spans field robotics, perception and learning for environmental monitoring, and human‑robot interaction for sustainability.</p>

<h2 class="section-title">Focus Areas</h2>
<ul class="list">
  {% for prj in site.data.projects %}
    <li>
      <strong>{{ prj.title }}</strong> — {{ prj.summary }}
      {% if prj.link %} · <a href="{{ prj.link }}" target="_blank">Learn more</a>{% endif %}
    </li>
  {% endfor %}
  {% if site.data.projects == nil %}
    <li>Coming soon.</li>
  {% endif %}
</ul>

