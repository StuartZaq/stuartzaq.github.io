---
layout: page
---

<h1>Мои мысли</h1>

<ul>
  {% for post in site.posts %}
    {% if post.categories contains "thoughts" %}
      <li><a href="{{ post.url }}">{{ post.title }}</a> ({{ post.date | date: "%Y-%m-%d" }})</li>
    {% endif %}
  {% endfor %}
</ul>
