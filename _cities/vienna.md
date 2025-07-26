---
layout: city
title: Vienna
slug: vienna
permalink: /cities/vienna/
---

{% assign city = 'vienna' | downcase %}

<main class="page-wrapper city-page">
  <article>
    <h1 class="page-title">{{ page.title }}</h1>

    <section class="city-category">
      <h2>Food & Drink</h2>
      <ul>
      {% assign category = 'food' %}
      {% for note in site.city_notes %}
        {% assign note_city = note.city | downcase %}
        {% if note_city == city and note.category == category %}
          <li><a href="{{ note.url }}">{{ note.title }}</a></li>
        {% endif %}
      {% endfor %}
      </ul>
    </section>

    <section class="city-category">
      <h2>Walks & Views</h2>
      <ul>
      {% assign category = 'walks' %}
      {% for note in site.city_notes %}
        {% assign note_city = note.city | downcase %}
        {% if note_city == city and note.category == category %}
          <li><a href="{{ note.url }}">{{ note.title }}</a></li>
        {% endif %}
      {% endfor %}
      </ul>
    </section>

    <section class="city-category">
      <h2>Arts & Heritage</h2>
      <ul>
      {% assign category = 'culture' %}
      {% for note in site.city_notes %}
        {% assign note_city = note.city | downcase %}
        {% if note_city == city and note.category == category %}
          <li><a href="{{ note.url }}">{{ note.title }}</a></li>
        {% endif %}
      {% endfor %}
      </ul>
    </section>

    <section class="city-category">
      <h2>Outings & Excursions</h2>
      <ul>
      {% assign category = 'trips' %}
      {% for note in site.city_notes %}
        {% assign note_city = note.city | downcase %}
        {% if note_city == city and note.category == category %}
          <li><a href="{{ note.url }}">{{ note.title }}</a></li>
        {% endif %}
      {% endfor %}
      </ul>
    </section>

  </article>
</main>
