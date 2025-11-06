---
title: Research
layout: default
permalink: /projects/
---

<h1>Research</h1>
<p>Our research spans field robotics, perception and learning for environmental monitoring, and human‑robot interaction for sustainability.</p>

<div class="features">
  {% for prj in site.data.projects %}
  <section class="feature-row {% if forloop.index0 % 2 == 1 %}reverse{% endif %}">
    <div class="feature-image">
      {% if prj.image %}
        <img src="{{ prj.image | relative_url }}" alt="{{ prj.title }}">
      {% endif %}
    </div>
    <div class="feature-text">
      <h3>{{ prj.title }}</h3>
      <p>{{ prj.summary }}</p>
      {% if prj.link %}<a class="feature-link" href="{{ prj.link }}" target="_blank" rel="noopener">Learn more →</a>{% endif %}
    </div>
  </section>
  {% endfor %}

  {% if site.data.projects == nil %}
    <p>Coming soon.</p>
  {% endif %}
</div>
