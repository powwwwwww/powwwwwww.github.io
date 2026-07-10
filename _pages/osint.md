---
layout: page
title: OSINT
permalink: /osint/
nav: true
nav_order: 2
description: Open Source Intelligence notes and guides.
---

<div class="page-header">
  <h1>OSINT</h1>
  <p>Open Source Intelligence notes and guides.</p>
</div>

<ul class="post-list">
  {% assign items = site.posts | where_exp: "post", "post.categories contains 'OSINT'" | sort: 'date' | reverse %}
  {% for post in items %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      {% if post.description %}<p class="muted">{{ post.description }}</p>{% endif %}
    </li>
  {% endfor %}
  {% if items == empty %}
    <li>No posts yet.</li>
  {% endif %}
</ul>
