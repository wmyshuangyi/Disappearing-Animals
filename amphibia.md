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
      <a href = " "><img src="{{ exhibitamph.image-url }}" class="gallery_thumb" width="450" height="400"></a >
      <p class = "caption"><a href = "{{ exhibitamph.url | relative_url }}">{{ exhibitamph.title }}</a ></p>
      <p> by {{ exhibitamph.creator }}</p >
      <p><a href="{{ licence_url.url }}">{{ exhibitamph.licence }}</a ></p >
      <p>Tags: {{ exhibitamph.tags }}</p >
    </div>
  {% endfor %}
</div>
