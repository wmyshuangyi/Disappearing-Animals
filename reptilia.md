---
title: Reptilia
layout: nav
permalink: /Reptilia/
---
<div id = "animal_collection">
  {% assign sorted_exhibitreptilia = site.exhibitreptilia | sort: "title" %}
  {% for exhibitreptile in sorted_exhibitreptilia %}
    {% assign licence_url = site.data.licences | find: "licence", exhibitinsect.licence %}
    <div class = "grid_cell">
      <a href = " "><img src="{{ exhibitreptile.image-url }}" class="gallery_thumb" width="300" height="450"></a >
      <p class = "caption"><a href = "{{ exhibitreptile.url | relative_url }}">{{ exhibitreptile.title }}</a ></p> 
      <p>by {{ exhibitreptile.creator }}</p>
      <p><a href="{{ licence_url.url }}">{{ exhibitreptile.licence }}</a ></p >
      <p>Tags: {{ exhibitreptile.tags }}</p >
    </div>
  {% endfor %}
</div>