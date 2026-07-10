---
layout: page
title: OSINT
permalink: /osint/
nav: true
nav_order: 2
description: Open Source Intelligence notes and guides.
---

<div class="post-list">
  {% assign items = site.posts | where_exp: "post", "post.categories contains 'OSINT'" | sort: 'date' | reverse %}
  {% if items.size > 0 %}
    {% for post in items %}
      <div>
        <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
        {% if post.description %}<p>{{ post.description }}</p>{% endif %}
      </div>
    {% endfor %}
  {% else %}
    <p>No posts yet.</p>
  {% endif %}
</div>
