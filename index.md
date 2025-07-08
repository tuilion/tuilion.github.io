---
layout: custom_home
---

<ul>
  {% for post in site.posts limit:3 %}
    <li>
      <h3>{{ post.title }}</h3>
      <p><small>{{ post.date | date: "%B %d, %Y" }}</small></p>
      <p>
        {{ post.content | strip_html | truncatewords: 100 }}
      </p>
    </li>
  {% endfor %}
</ul>
 
