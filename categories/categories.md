---
layout: page
title: Категории
---

<h1>Категории</h1>

<ul>
  {% assign all_categories = site.posts | map: 'categories' | uniq | sort %}
  {% for cat in all_categories %}
    <li><a href="/categories/{{ cat | first }}.html">{{ cat | capitalize }}</a></li>
  {% endfor %}
</ul>
