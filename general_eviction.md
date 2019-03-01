---
layout: archive
permalink: /general_eviction/
title: "General Eviction Data"
---

City of Milwaukee eviction data and  case outcomes.

<div class="tiles">
{% for post in site.categories.general_eviction %}
  {% include post-grid.html %}
{% endfor %}
</div><!-- /.tiles -->