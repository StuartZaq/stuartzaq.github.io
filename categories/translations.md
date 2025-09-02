---
layout: page
---

<h1>Мои переводы</h1>

<ul>
  {% for post in site.posts %}
    {% if post.categories contains "translations" %}
      <li><a href="{{ post.url }}">{{ post.title }}</a> ({{ post.date | date: "%Y-%m-%d" }})</li>
    {% endif %}
  {% endfor %}
</ul>
