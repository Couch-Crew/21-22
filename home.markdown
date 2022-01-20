---
title: home
layout: home
permalink: /
---
this is the home page for incubator comics

{% for comic in site.comics %}
  <h2>
    <a href='{{ comic.url | relative_url }}'>
      {{ comic.title }}
    </a>
  </h2>
{% endfor %}