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
      <a href = " "><img src="{{ exhibitave.image-url }}" class="gallery_thumb" width="300" height="450"></a >
      <p class = "caption"><a href = "{{ exhibitave.url | relative_url }}">{{ exhibitave.title }}</a > by {{ exhibitave.creator }}</p >
      <p><a href="{{ licence_url.url }}">{{ exhibitave.licence }}</a ></p >
    </div>
  {% endfor %}
</div>
