---
layout: city
title: Vienna
slug: vienna
---

<main class="page-wrapper city-page">
  <article>
    <section>
      <h2>Notes about {{ page.title }}</h2>

      {% assign notes_for_city = site.city_notes | where: "city", page.slug %}
      {% assign notes_sorted = notes_for_city | sort: "date" | reverse %}
      {% assign notes_grouped = notes_sorted | group_by: "category" %}

      {% for group in notes_grouped %}
        <h3>{{ group.name | capitalize }}</h3>
        <ul>
          {% for note in group.items %}
            <li>
              <a href="{{ note.url }}">{{ note.title }}</a>
              <span class="note-date">({{ note.date | date: "%Y-%m-%d" }})</span>
            </li>
          {% endfor %}
        </ul>
      {% endfor %}
    </section>

    <div class="button-center" style="margin-top: 2rem;">
      <a class="button subtle" href="/my-cities/">← Back to cities</a>
    </div>
  </article>
</main>
