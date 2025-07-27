---
layout: city
title: Vienna
---
<main class="page-wrapper city-page">
  <article>
    <section>
      <h2>Notes about {{ page.title }}</h2>
      <ul>
        {% assign notes_for_city = site.city_notes | where: "city", page.slug %}
        {% for note in notes_for_city %}
          <li>
            <a href="{{ note.url }}">{{ note.title }}</a> — {{ note.date | date: "%Y-%m-%d" }}
          </li>
        {% endfor %}
      </ul>
    </section>
  </article>
</main>

