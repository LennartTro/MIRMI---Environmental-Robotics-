---
title: News
layout: default
permalink: /news/
---

<h1>News</h1>
<ul class="list">
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <span class="muted"> — {{ post.date | date: "%b %d, %Y" }}</span>
    </li>
  {% endfor %}
  {% if site.posts == empty %}
    <li>Coming soon.</li>
  {% endif %}
</ul>

