---
title: archive
layout: default
permalink: /archive
---

<div class='content'>
  {% assign items_grouped = site.comics | group_by: 'unit' | sort: 'name' %}

  {% for unit in items_grouped %}
    <h1> Unit {{ unit.name }} </h1>

    {% for comic in unit.items %}
      <a href='{{ comic.url | relative_url }}'>
        <p>{{ comic.title }}</p>
      </a>
    {% endfor %}
  {% endfor %}
</div>