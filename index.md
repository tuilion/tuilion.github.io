---
layout: custom_home
---

<ul>
  {% for post in site.posts limit:5 %}
    <li>
      <h3>{{ post.title }}</h3>
      <p><small>{{ post.date | date: "%B %d, %Y" }}</small></p>
      <p>
        {{ post.excerpt }}
      </p>
    </li>
  {% endfor %}
</ul>
 
