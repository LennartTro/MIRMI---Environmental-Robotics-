title: People
layout: default
permalink: /people/

<h1>People</h1>

<h2 class="section-title">Faculty and Staff</h2>
<div class="person-grid">
  {% assign staff = site.data.people | where: 'group', 'staff' %}
  {% for p in staff %}
    <div class="person">
      {% if p.image %}
        <img class="avatar" src="{{ p.image | relative_url }}" alt="{{ p.name }}">
      {% else %}
        <div class="avatar avatar-fallback">{{ p.name | slice: 0,1 }}</div>
      {% endif %}
      <div class="person-name">{{ p.name }}</div>
      {% if p.role %}<div class="person-role">{{ p.role }}</div>{% endif %}
      <div class="person-links">
        {% if p.links and p.links.website %}<a href="{{ p.links.website }}" target="_blank">Website</a>{% endif %}
        {% if p.links and p.links.scholar %}{% if p.links and p.links.website %} · {% endif %}<a href="{{ p.links.scholar }}" target="_blank">Scholar</a>{% endif %}
      </div>
    </div>
  {% endfor %}
</div>

<h2 class="section-title">Students</h2>
<div class="person-grid">
  {% assign students = site.data.people | where: 'group', 'student' %}
  {% for p in students %}
    <div class="person">
      {% if p.image %}
        <img class="avatar" src="{{ p.image | relative_url }}" alt="{{ p.name }}">
      {% else %}
        <div class="avatar avatar-fallback">{{ p.name | slice: 0,1 }}</div>
      {% endif %}
      <div class="person-name">{{ p.name }}</div>
      {% if p.role %}<div class="person-role">{{ p.role }}</div>{% endif %}
    </div>
  {% endfor %}
</div>

<h2 class="section-title">Alumni</h2>
<div class="person-grid">
  {% assign alumni = site.data.people | where: 'group', 'alumni' %}
  {% for p in alumni %}
    <div class="person">
      {% if p.image %}
        <img class="avatar" src="{{ p.image | relative_url }}" alt="{{ p.name }}">
      {% else %}
        <div class="avatar avatar-fallback">{{ p.name | slice: 0,1 }}</div>
      {% endif %}
      <div class="person-name">{{ p.name }}</div>
      {% if p.next %}<div class="person-role">→ {{ p.next }}</div>{% endif %}
    </div>
  {% endfor %}
</div>
