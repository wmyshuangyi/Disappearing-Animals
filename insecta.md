---
title: Insecta
layout: nav
permalink: /Insecta/
---
<div id = "animal_insecta">
  {% assign sorted_exhibitinsecta = site.exhibitinsecta | sort: "title" %}
  {% for exhibitinsect in sorted_exhibitinsecta %}
    {% assign licence_url = site.data.licences | find: "licence", exhibitinsect.licence %}
    <div class = "grid_cell">
      <a href = " "><img src="{{ exhibitinsect.image-url }}" class="gallery_insecta" width="400" height="450"></a >
      <p class = "caption"><a href = "{{ exhibitinsect.url | relative_url }}">{{ exhibitinsect.title }}</a ></p> 
      <p>by {{ exhibitinsect.creator }}</p>
      <p><a href="{{ licence_url.url }}">{{ exhibitinsect.licence }}</a ></p >
      <p>Tags: {{ exhibitinsect.tags }}</p >
    </div>
  {% endfor %}
</div>