---
title: Amphibia
layout: nav
permalink: /amphibia/
---
<div id = "animal_amphibia">
  {% assign sorted_exhibitamphibia = site.exhibitamphibia | sort: "title" %}
  {% for exhibitamph in sorted_exhibitamphibia %}
    {% assign licence_url = site.data.licences | find: "licence", exhibitamph.licence %}
    <div class = "grid_cell">
      <a href = "{{ exhibitamph.url | relative_url }}"><img src="{{ exhibitamph.image-url }}" class="gallery" width="450" height="400"></a >
      <p class = "caption"><a href = "{{ exhibitamph.url | relative_url }}">{{ exhibitamph.title }}</a ></p>
      <p> by {{ exhibitamph.creator }}</p >
      <p><a href="{{ licence_url.url }}">{{ exhibitamph.licence }}</a ></p >
      <p>Tags: {{ exhibitamph.tags }}</p >
    </div>
  {% endfor %}
</div>

<br>
<div class="attention">
 <p>* indicates that due to copyright or lack of resources, the image is not of the specific animal but of the family or genus to which it belongs, as indicated in the description page.</p>
 </div>
