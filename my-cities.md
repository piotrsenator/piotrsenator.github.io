---
layout: gallery_overview
title: Off the Trail
---

# Off the Trail

Walks, hikes and day trips that left an impression. Scroll through the gallery and click to explore.

<div class="trail-grid">
  {% for item in site.trail_items %}
    {% include gallery_item.html item=item %}
  {% endfor %}
</div>
