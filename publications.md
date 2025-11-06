---
title: Publications
layout: default
permalink: /publications/
---

<h1>Publications</h1>
<ul class="list">
  {% assign pubs = site.data.publications | sort: 'year' | reverse %}
  {% for pub in pubs %}
    <li>
      {{ pub.authors | join: ", " }} ({{ pub.year }}). <strong>{{ pub.title }}</strong>.
      {% if pub.venue %} <em>{{ pub.venue }}</em>.{% endif %}
      {% if pub.links and pub.links.doi %} <a href="https://doi.org/{{ pub.links.doi }}" target="_blank">DOI</a>{% endif %}
      {% if pub.links and pub.links.pdf %} <a href="{{ pub.links.pdf }}" target="_blank">PDF</a>{% endif %}
    </li>
  {% endfor %}
  {% if pubs == empty %}
    <li>Coming soon.</li>
  {% endif %}
</ul>

