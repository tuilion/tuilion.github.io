---
layout: home
---

{% assign recent_posts = site.posts | slice: 0, 3 %}

{% for post in recent_posts %}
<div style="margin-bottom: 2em;">
  <h2 style="margin-bottom: 0.2em;">{{ post.title }}</h2>
  <p><small>{{ post.date | date: "%b %-d, %Y" }}</small></p>
  <div>
    {{ post.content | strip_html | truncatewords: 50 }}
  </div>
</div>
{% endfor %}
