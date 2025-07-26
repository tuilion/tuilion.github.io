---
layout: page
title: "Post Archive"
permalink: /post-archive/
---

<h1>Post Archive</h1>

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <span>— {{ post.date | date: "%B %d, %Y" }}</span>
    </li>
  {% endfor %}
</ul>
