---
layout: personal
title: personal
permalink: /personal/
description: I spend my free time playing soccer, travelling, clicking photos or simply enjoying a book.
nav: true
---

{% assign personal_pages = site.personal %}
{% for page in personal_pages %}
  <h2>{{ page.title }}</h2>
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


