---
layout: default
title: Off the Trail
permalink: /off-the-trail/
---

<div class="page-wrapper">
  <h1 class="page-title">Off the Trail</h1>
  <p>I spend a lot of time at a desk but whenever I can, I put on my hiking boots or hop on my bike. I enjoy heading out with friends just as much as walking alone, whether it’s a quick escape nearby or a longer trip into the mountains. Here I have gathered a few outings that brought me real joy. Maybe they will inspire your next adventure.</p>
  <div class="trip-gallery">
    {% assign sorted_trips = site.trips | sort: 'date' | reverse %}
    {% for trip in sorted_trips %}
      <a class="trip-card" href="{{ trip.url }}">
        <img src="/assets/images/trips/{{ trip.cover_image | default: 'trips__placeholder.jpg' }}" alt="{{ trip.title }}">
        <div class="trip-caption">{{ trip.title }}</div>
      </a>
    {% endfor %}
  </div>
</div>
