---
title: People
layout: default
permalink: /people/
---

<h1>People</h1>

<h2 class="section-title">Faculty and Staff</h2>
<ul class="list">
  {% for p in site.data.people | where: 'group', 'staff' %}
    <li>
      <strong>{{ p.name }}</strong>{% if p.role %}, {{ p.role }}{% endif %}
      {% if p.links and p.links.website %} · <a href="{{ p.links.website }}" target="_blank">Website</a>{% endif %}
      {% if p.links and p.links.scholar %} · <a href="{{ p.links.scholar }}" target="_blank">Scholar</a>{% endif %}
    </li>
  {% endfor %}
  {% if site.data.people == nil %}
    <li>Coming soon.</li>
  {% endif %}
  </ul>

<h2 class="section-title">Students</h2>
<ul class="list">
  {% for p in site.data.people | where: 'group', 'student' %}
    <li>
      <strong>{{ p.name }}</strong>{% if p.role %}, {{ p.role }}{% endif %}
    </li>
  {% endfor %}
</ul>

<h2 class="section-title">Alumni</h2>
<ul class="list">
  {% for p in site.data.people | where: 'group', 'alumni' %}
    <li>
      <strong>{{ p.name }}</strong>{% if p.next %} → {{ p.next }}{% endif %}
    </li>
  {% endfor %}
</ul>

