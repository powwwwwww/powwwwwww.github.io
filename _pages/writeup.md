---
layout: page
title: Writeup
permalink: /writeup/
nav: true
nav_order: 4
description: Technical writeups and notes.
---

<div class="page-header">
  <h1>Writeup</h1>
  <p>Technical writeups and reproducible notes.</p>
</div>

<ul class="post-list">
  {% assign items = site.posts | where_exp: "post", "post.categories contains 'Writeup'" | sort: 'date' | reverse %}
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
