---
layout: page
title: Категории
---

<ul>
  {% assign cat_map = "guides:Гайды,contests:Конкурсы,otchety-s-igr:Отчёты с игр,news:Новости,pictures:Картинки,projects:Мои проекты,reposting:Перепосты,reviews:Мои обзоры,thoughts:Мои мысли,translations:Мои переводы" | split: "," %}
  {% assign all_categories = site.posts | map: 'categories' | flatten | uniq | sort %}

  {% for cat in all_categories %}
    {% assign cat_name = cat %}
    {% for pair in cat_map %}
      {% assign key_value = pair | split: ":" %}
      {% if key_value[0] == cat %}
        {% assign cat_name = key_value[1] %}
      {% endif %}
    {% endfor %}
    <li><a href="/categories/{{ cat }}.html">{{ cat_name }}</a></li>
  {% endfor %}
</ul>
