---
layout: page
title: CTI
permalink: /cti/
nav: true
nav_order: 1
description: Cyber Threat Intelligence writings and analysis.
---

<div class="page-header">
  <h1>CTI</h1>
  <p>Cyber Threat Intelligence writings and analysis.</p>
</div>

<ul class="post-list">
  {% assign ctis = site.posts | where_exp: "post", "post.categories contains 'CTI'" | sort: 'date' | reverse %}
  {% for post in ctis %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      {% if post.description %}<p class="muted">{{ post.description }}</p>{% endif %}
    </li>
  {% endfor %}
  {% if ctis == empty %}
    <li>No posts yet.</li>
  {% endif %}
</ul>
