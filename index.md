---
layout: home
title: Tuilion Blog
---

## Latest Posts

<ul>
  {% for post in site.posts limit:3 %}
    <li>
      <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
      <p>{{ post.excerpt | strip_html | truncatewords: 40 }}</p>
    </li>
  {% endfor %}
</ul>

<p><a href="/archive.html">→ Full archive</a></p>
