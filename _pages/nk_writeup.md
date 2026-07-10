---
layout: page
title: NK
permalink: /nk/
nav: true
nav_order: 3
description: North Korea-focused investigations.
---

<div class="page-header">
  <h1>NK</h1>
  <p>North Korea-focused investigations and notes.</p>
</div>

<ul class="post-list">
  {% assign items = site.posts | where_exp: "post", "post.categories contains 'NK'" | sort: 'date' | reverse %}
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

Content coming soon.
