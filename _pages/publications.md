---
layout: page
permalink: /publications/
title: publications
description: 
nav: true
nav_order: 2
---
<!-- _pages/publications.md -->
<div class="publications">

{% assign pubs = site.scholar.bibliography | bibliography %}

{% for entry in pubs %}
  <div class="pub-entry" style="margin-bottom: 1.5em;">
    <p>
      {% if entry.url %}
        <strong><a href="{{ entry.url }}" target="_blank" rel="noopener">{{ entry.title }}</a></strong>
      {% else %}
        <strong>{{ entry.title }}</strong>
      {% endif %}
      <br>
      {{ entry.author }}. <em>{{ entry.year }}</em>.
      {% if entry.journal %} <em>{{ entry.journal }}</em>.{% endif %}
      {% if entry.booktitle %} <em>{{ entry.booktitle }}</em>.{% endif %}
    </p>
  </div>
{% endfor %}


</div>
