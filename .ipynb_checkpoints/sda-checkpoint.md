---
layout: archive
permalink: /sda/
title: "Maps"
---

Explore eviction trends and outcomes at the address or parcel level. Assess how often certain owners file evictions. View eviction filing and judgement rates from 2016-2018.

<div class="tiles">
{% for post in site.categories.sda %}
  {% include post-grid.html %}
{% endfor %}
</div><!-- /.tiles -->