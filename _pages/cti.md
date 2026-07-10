---
layout: page
title: CTI
permalink: /cti/
nav: true
nav_order: 1
description: Cyber Threat Intelligence writings and analysis.
---

<div class="post-list">
  {% assign ctis = site.posts | where_exp: "post", "post.categories contains 'CTI'" | sort: 'date' | reverse %}
  {% if ctis.size > 0 %}
    {% for post in ctis %}
      <div>
        <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
        {% if post.description %}<p>{{ post.description }}</p>{% endif %}
      </div>
    {% endfor %}
  {% else %}
    <p>No posts yet.</p>
  {% endif %}
</div>
