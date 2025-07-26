---
layout: default
title: Piotr Senator
---

<main class="home-wrapper">

  <section class="home-about-and-cities">
    <section class="home-about">
      <h2>About Me</h2>
      <p>Strategist, auditor and observer of systems. I draw on diverse disciplines and cities to better understand the world.</p>
      <p><a class="button subtle" href="/about/">Read more</a></p>
    </section>

    <section class="home-cities">
      <h2>My Cities</h2>
      <div class="city-tiles">
        <a href="/cities/vienna/" class="city-note-tile"><img src="/assets/images/city__vienna__1.jpg" alt="Vienna" /><span>Vienna</span></a>
        <a href="/cities/warsaw/" class="city-note-tile"><img src="/assets/images/city__warsaw__1.jpg" alt="Warsaw" /><span>Warsaw</span></a>
        <a href="/cities/luxembourg/" class="city-note-tile"><img src="/assets/images/city__luxembourg__1.jpg" alt="Luxembourg" /><span>Luxembourg</span></a>
      </div>
    </section>
  </section>

<section class="home-trail">
  <h2>Off the Trail</h2>
  <div class="trip-gallery">
    {% assign latest_trips = site.trips | sort: 'date' | reverse | slice: 0, 3 %}
    {% for trip in latest_trips %}
      {% assign image_path = trip.cover_image | default: 'trips__placeholder.jpg' %}
      <a class="trip-card" href="{{ trip.url }}">
        <img src="/assets/images/trips/{{ image_path }}" alt="{{ trip.title }}">
        <div class="trip-caption">{{ trip.title }}</div>
      </a>
    {% endfor %}
  </div>
  <div class="button-center">
    <a class="button subtle" href="/off-the-trail/">View all excursions</a>
  </div>
</section>

<section class="home-notes"> 
  <h2>Notes</h2>
  <div class="note-grid">
    {% assign latest_notes = site.notes | sort: 'date' | reverse | slice: 0, 2 %}
    {% for note in latest_notes %}
      <a href="{{ note.url }}" class="note-tile">
        <h3>{{ note.title }}</h3>
        <p>{{ note.excerpt | strip_html | truncate: 160 }}</p>
        <span class="note-date">{{ note.date | date: "%d %B %Y" }}</span>
      </a>
    {% endfor %}
  </div>
  <div class="button-center">
    <a class="button subtle" href="/notes/">View all notes</a>
  </div>
</section>



</main>
