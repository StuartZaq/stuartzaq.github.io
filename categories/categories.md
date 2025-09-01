---
layout: page
title: Категории
---

<ul>
  {% assign cats = site.posts | map: "categories" | uniq | sort %}
  {% for cat in cats %}
    <li><a href="/categories/{{ cat | slugify }}/">{{ cat }}</a></li>
  {% endfor %}
</ul>
