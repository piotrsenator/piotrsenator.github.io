---
layout: city
title: Vienna
---
<main class="page-wrapper city-page">
  <article>
<section>
  {% assign notes_for_city = site.city_notes | where: "city", page.slug %}
  {% assign notes_sorted = notes_for_city | sort: "date" | reverse %}
  {% assign notes_grouped = notes_sorted | group_by: "category" %}

  {% for group in notes_grouped %}
    <h2>{{ group.name | capitalize }}</h2>

<div class="city-note-grid">
  {% for note in group.items %}
    <a href="{{ note.url }}" class="city-note-card {% unless note.cover_image %}no-image{% endunless %}">
      
      {% if note.cover_image %}
      <div class="image-wrapper">
        <img src="/assets/images/{{ note.cover_image }}" alt="{{ note.title }}">
      </div>
      {% endif %}

      <div class="text-wrapper">
        <h4>{{ note.title }}</h4>
        <p>{{ note.excerpt | strip_html | truncatewords: 30 }}</p>
      </div>
    </a>
  {% endfor %}
</div>

  {% endfor %}
</section>

  </article>
</main>
