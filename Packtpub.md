---
layout: page
title: Packt Publishing Books
permalink: /packtpub/
---

{% include JB/setup %}
 

{% assign tags_list = site.tags | sort %}  
{% for tag in tags_list %} 
  {% if tag[0] == "Packtpub" %}
  <h2 id="{{ tag[0] }}-ref">{{ tag[0] | replace: '-', ' '}}</h2>
  <ul>
    {% assign pages_list = tag[1] %}  
    {% include JB/pages_list %}
  </ul>
  {% endif %}
{% endfor %}