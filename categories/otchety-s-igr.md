---
layout: page
---

<h1>Отчёты с игр</h1>

<ul>
  {% for post in site.posts %}
    {% if post.categories contains "Отчёты с игр" %}
      <li><a href="{{ post.url }}">{{ post.title }}</a> ({{ post.date | date: "%Y-%m-%d" }})</li>
    {% endif %}
  {% endfor %}
</ul>