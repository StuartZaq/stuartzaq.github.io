---
layout: page
---

<h1> Гайды</h1>

<ul>
  {% for post in site.posts %}
    {% if post.categories contains "guides" %}
      <li><a href="{{ post.url }}">{{ post.title }}</a> ({{ post.date | date: "%Y-%m-%d" }})</li>
    {% endif %}
  {% endfor %}
</ul>
