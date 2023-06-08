---
layout: personal
title: personal
order: 5
permalink: /personal/
description: I spend my free time travelling, clicking pictures, playing soccer or simply enjoying a book. Here are some of my clicks
nav: true
---

{% assign personal_pages = site.personal %}
{% for page in personal_pages %}

  <div>
  <hr>
  <!-- <h2>{{ page.title }}</h2> -->
  <!-- <hr> -->
  
  
  
  <ul class="image-gallery">
  {% for image in site.static_files %}
    {% if image.path contains "assets/img/personal" %}
      {% if image.path contains page.photos.set %}
      <li>
        <a href="{{site.baseurl}}{{image.path}}" title="{{ filename }}"><img src="{{site.baseurl}}{{image.path}}"/></a>
      </li>
      {% endif %}
    {% endif %}
  {% endfor %}
  </ul>
{% endfor %}


