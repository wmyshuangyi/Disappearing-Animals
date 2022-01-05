---
title: Reptilia
layout: nav
permalink: /Reptilia/
---
<div id = "animal_reptilia">
  {% assign sorted_exhibitreptilia = site.exhibitreptilia | sort: "title" %}
  {% for exhibitreptile in sorted_exhibitreptilia %}
    {% assign licence_url = site.data.licences | find: "licence", exhibitinsect.licence %}
    <div class = "grid_cell">
      <a href = "{{ exhibitreptile.url | relative_url }}"><img src="{{ exhibitreptile.image-url }}" class="gallery" width="450" height="400"></a >
      <p class = "caption"><a href = "{{ exhibitreptile.url | relative_url }}">{{ exhibitreptile.title }}</a ></p> 
      <p>by {{ exhibitreptile.creator }}</p>
      <p><a href="{{ licence_url.url }}">{{ exhibitreptile.licence }}</a ></p >
      <p>Tags: {{ exhibitreptile.tags }}</p >
    </div>
  {% endfor %}
</div>
<br>
<div class="attention">
 <p>* indicates that due to copyright or lack of resources, the image is not of the specific animal but of the family or genus to which it belongs, as indicated in the description page.</p>
 </div>