---
title: Aves
layout: nav
permalink: /aves/
---
<div id = "animal_aves">
  {% assign sorted_exhibitaves = site.exhibitaves | sort: "title" %}
  {% for exhibitave in sorted_exhibitaves %}
    {% assign licence_url = site.data.licences | find: "licence", exhibitave.licence %}
    <div class = "grid_cell">
      <a href = "{{ exhibitave.url | relative_url }}"><img src="{{ exhibitave.image-url }}" class="gallery" width="400" height="400"></a>
      <p class = "caption"><a href = "{{ exhibitave.url | relative_url }}">{{ exhibitave.title }}</a ></p>
      <p> by {{ exhibitave.creator }}</p >
      <p><a href="{{ licence_url.url }}">{{ exhibitave.licence }}</a ></p >
      <p>Tags: {{ exhibitave.tags }}</p >
    </div>
  {% endfor %}
</div>
<br>
<div class="attention">
 <p>* indicates that due to copyright or lack of resources, the image is not of the specific animal but of the family or genus to which it belongs, as indicated in the description page.</p>
 </div>
