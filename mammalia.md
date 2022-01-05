---
title: Mammalia
layout: nav
permalink: /Mammalia/
---
<div id = "animal_mammalia">
  {% assign sorted_exhibitmammalia = site.exhibitmammalia | sort: "title" %}
  {% for exhibitmammal in sorted_exhibitmammalia %}
    {% assign licence_url = site.data.licences | find: "licence", exhibitmammal.licence %}
    <div class = "grid_cell">
      <a href = "{{ exhibitmammal.url | relative_url }}"><img src="{{ exhibitmammal.image-url }}" class="gallery_thumb" width="450" height="400"></a >
      <p class = "caption"><a href = "{{ exhibitmammal.url | relative_url }}">{{ exhibitmammal.title }}</a ></p> 
      <p>by {{ exhibitmammal.creator }}</p>
      <p><a href="{{ licence_url.url }}">{{ exhibitmammal.licence }}</a ></p >
      <p>Tags: {{ exhibitmammal.tags }}</p >
    </div>
  {% endfor %}
</div>

<br>
<div class="attention">
 <p>* indicates that due to copyright or lack of resources, the image is not of the specific animal but of the family or genus to which it belongs, as indicated in the description page.</p>
 </div>