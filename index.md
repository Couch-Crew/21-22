---
title: home
layout: default
permalink: /
---

<div class='content'>
  <div class='display-nav'>
    {% assign prev_id = site.comics.last.comic-id | minus: 1 %}
    {% assign prev_comic = site.comics | where: "comic-id", prev_id | first %}
    <a 
    class='link left'
    href='{{ prev_comic.url | relative_url }}'>
      <span class='arrow'>&lt;</span>
    </a>

    <h1 class='comic-title'>home | comics</h1>
    <span />
  </div>

  <img 
  class='comic' 
  src='comics/{{ site.comics.last.image }}' 
  alt="oops- there's supposed to be a comic here" />

  <div class='explanation'>
    {{ site.comics.last.content }}
  </div>
</div>