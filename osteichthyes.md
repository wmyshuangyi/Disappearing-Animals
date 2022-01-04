---
title: Osteichthyes
layout: nav
permalink: /Osteichthyes/
---
<div id = "animal_collection">
  {% assign sorted_exhibitosteichthyes = site.exhibitosteichthyes | sort: "title" %}
  {% for exhibitos in sorted_exhibitosteichthyes %}
    {% assign licence_url = site.data.licences | find: "licence", exhibitos.licence %}
    <div class = "grid_cell">
      <a href = " "><img src="{{ exhibitos.image-url }}" class="gallery_thumb" width="300" height="450"></a >
      <p class = "caption"><a href = "{{ exhibitos.url | relative_url }}">{{ exhibitos.title }}</a ></p> 
      <p>by {{ exhibitos.creator }}</p>
      <p><a href="{{ licence_url.url }}">{{ exhibitos.licence }}</a ></p >
      <p>Tags: {{ exhibitos.tags }}</p >
    </div>
  {% endfor %}
</div>