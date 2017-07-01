---
layout: page
title: O'Reilly Media Books
permalink: /oreilly/
---

{% include JB/setup %}
 

{% assign tags_list = site.tags | sort %}  
{% for tag in tags_list %} 
  {% if tag[0] == "O'Reilly" %}
  <h2 id="{{ tag[0] }}-ref">{{ tag[0] | replace: '-', ' '}}</h2>
  <ul>
    {% assign pages_list = tag[1] %}  
    {% include JB/pages_list %}
  </ul>
  {% endif %}
{% endfor %}