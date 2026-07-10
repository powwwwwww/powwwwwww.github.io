---
layout: page
title: Writeup
permalink: /writeup/
nav: true
nav_order: 4
description: Technical writeups and notes.
---

<div class="post-list">
  {% assign items = site.posts | where_exp: "post", "post.categories contains 'Writeup'" | sort: 'date' | reverse %}
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
