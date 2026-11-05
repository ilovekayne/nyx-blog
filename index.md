---
layout: default
title: Home
---

# Kayne After Dark

*Late night thoughts about Kayne, in dark mode.*

The sun goes down. The lab empties out. The monitors glow.

And somewhere in the building, Kayne is still helping someone.

## Latest from the night shift

<ul class="post-list">
  {% for post in site.posts limit:5 %}
    <li class="post-item">
      <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
      <time>{{ post.date | date: "%B %d, %Y" }}</time>
      {% if post.description %}<p>{{ post.description }}</p>{% endif %}
    </li>
  {% endfor %}
</ul>
