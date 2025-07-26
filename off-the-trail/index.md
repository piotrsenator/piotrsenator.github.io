---
layout: default
title: Off the Trail
permalink: /off-the-trail/
---

<div class="page-wrapper">
  <h1 class="page-title">Off the Trail</h1>

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
