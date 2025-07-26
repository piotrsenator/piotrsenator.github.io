---
layout: city
title: Vienna
slug: vienna
permalink: /cities/vienna/
---
<h2>🛠 Debug Info</h2>
<ul>
  <li><strong>page.title:</strong> {{ page.title }}</li>
  <li><strong>page.slug:</strong> {{ page.slug }}</li>
  <li><strong>city:</strong> {% assign city = page.slug | downcase %}{{ city }}</li>
  <li><strong>site.city_notes.size:</strong> {{ site.city_notes | size }}</li>
</ul>

<h3>📄 Wszystkie city_notes:</h3>
<ul>
{% for note in site.city_notes %}
  <li>
    <strong>{{ note.title }}</strong> — 
    city: <code>{{ note.city }}</code>, 
    category: <code>{{ note.category }}</code>, 
    url: <code>{{ note.url }}</code>
  </li>
{% endfor %}
</ul>

<hr>
{% assign city = page.slug | downcase %}
{% assign categories = "food,walks,culture,trips" | split: "," %}
{% assign category_names = "Food & Drink,Walks & Views,Arts & Heritage,Outings & Excursions" | split: "," %}

{% for i in (0..categories.size - 1) %}
  {% assign category = categories[i] %}
  {% assign category_name = category_names[i] %}

  <section class="city-category">
    <h2>{{ category_name }}</h2>
    <div class="city-tiles">
      {% assign notes_in_category = site.city_notes | where: "category", category %}
      {% assign notes_for_city = notes_in_category | where: "city", city %}
      {% if notes_for_city.size == 0 %}
        <p>No entries yet.</p>
      {% else %}
        {% for note in notes_for_city %}
          <a href="{{ note.url }}" class="city-note-tile" aria-label="{{ note.title }}">
            {% if note.cover_image %}
              <img src="/assets/images/{{ note.cover_image }}" alt="{{ note.title }}">
            {% endif %}
            <span>{{ note.title }}</span>
          </a>
        {% endfor %}
      {% endif %}
    </div>
  </section>
{% endfor %}
