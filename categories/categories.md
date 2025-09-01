---
layout: page
title: Категории
---

<ul>
  {% assign cat_map = "guides:Гайды,contests:Конкурсы,otchety-s-igr:Отчёты с игр" | split: "," %}
  {% assign cat_hash = {} %}
  {% for pair in cat_map %}
    {% assign key_value = pair | split: ":" %}
    {% assign cat_hash = cat_hash | merge: {{ key_value[0] | strip }} => {{ key_value[1] | strip }} %}
  {% endfor %}

  {% assign all_categories = site.posts | map: 'categories' | flatten | uniq | sort %}
  {% for cat in all_categories %}
    {% assign cat_name = cat_hash[cat] | default: cat %}
    <li><a href="/categories/{{ cat }}.html">{{ cat_name }}</a></li>
  {% endfor %}
</ul>