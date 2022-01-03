---
title: Aves
layout: nav
permalink: /aves/
---
 {% assign class_aves = site.data.class2 %}

  {% for image_aves = site.exhibits | find: "class", class_aves.class %}
  
 <li> <img src = "{{ image_aves.image-url }}"></li>

{% endfor %}
