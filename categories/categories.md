---
layout: page
title: Категории
---

<ul>
  {% assign cats = site.posts | map: "categories" | uniq | sort %}
  {% for cat in cats %}
    {% assign cat_slug = cat | slugify %}
    <li><a href="/categories/{{ cat_slug }}/">{{ cat }}</a></li>
  {% endfor %}
</ul>
