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
      <a href = "{{ exhibitinsect.url | relative_url }}"><img src="{{ exhibitinsect.image-url }}" class="gallery" width="400" height="450"></a >
      <p class = "caption"><a href = "{{ exhibitinsect.url | relative_url }}">{{ exhibitinsect.title }}</a ></p> 
      <p>by {{ exhibitinsect.creator }}</p>
      <p><a href="{{ licence_url.url }}">{{ exhibitinsect.licence }}</a ></p >
      <p>Tags: {{ exhibitinsect.tags }}</p >
    </div>
  {% endfor %}
</div>
<br>
<div class="attention">
 <p>* indicates that due to copyright or lack of resources, the image is not of the specific animal but of the family or genus to which it belongs, as indicated in the description page.</p>
 </div>