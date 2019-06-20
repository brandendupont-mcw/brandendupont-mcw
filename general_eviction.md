---
layout: archive
permalink: /general_eviction/
title: "Eviction Metrics"
---

Aggregate City of Milwaukee eviction data and case outcomes. View yearly and monthly trends. See top evictors by lead plantiff.

<div class="tiles">
{% for post in site.categories.general_eviction %}
  {% include post-grid.html %}
{% endfor %}
</div><!-- /.tiles -->