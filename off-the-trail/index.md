---
layout: default
title: Off the Trail
permalink: /off-the-trail/
---

<h2>Off the Trail</h2>

<div class="trip-gallery">
  {% for trip in site.trips %}
    <a href="{{ trip.url }}">
      <img src="/assets/images/trip__{{ trip.slug }}__1.jpg" alt="{{ trip.title }}">
    </a>
  {% endfor %}
</div>
