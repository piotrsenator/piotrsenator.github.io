---
layout: city
title: Luxembourg
---
<header class="city-page__header">
  <p>
Luxembourg is the place I now call home. Small in size but rich in contrasts, it’s a cultural crossroads where people from all over the world seem to arrive by chance—and often end up staying. Maybe it’s the sparkling wine, the endless greenery, or simply the quiet harmony of so many nationalities living side by side. There’s more to Luxembourg than finance: it’s a charming corner of Europe, full of hidden places and quiet surprises.
  </p>
</header>

<section>
  {% assign notes_for_city = site.city_notes | where: "city", page.slug %}
  {% assign notes_sorted = notes_for_city | sort: "date" | reverse %}
  {% assign notes_grouped = notes_sorted | group_by: "category" %}

  {% if notes_grouped.size > 0 %}
    {% for group in notes_grouped %}
      <div class="category-section">
        <h2 class="category-section__title">{{ group.name | capitalize }}</h2>
        <div class="city-note-grid">
          {% for note in group.items %}
            <a href="{{ note.url | relative_url }}" class="city-note-card {% unless note.cover_image %}no-image{% endunless %}">

              {% if note.cover_image %}
              <div class="city-note-card__image-wrapper">
                <img src="/assets/images/cities/{{ note.city }}/{{ note.cover_image }}" alt="{{ note.title }}" class="city-note-card__image">
              </div>
              {% else %}
                <div class="city-note-card__image-wrapper city-note-card__image-wrapper--placeholder"></div>
              {% endif %}
              <div class="city-note-card__content">
                <h3 class="city-note-card__title">{{ note.title }}</h3>
                      <p class="city-note-card__excerpt">{{ note.content | markdownify | strip_html | truncatewords: 15, "..." }}</p>
              </div>
            </a>
          {% endfor %}
        </div>
      </div>
    {% endfor %}
  {% else %}
    <p>Brak notatek do wyświetlenia dla tego miasta.</p>
  {% endif %}
</section>
