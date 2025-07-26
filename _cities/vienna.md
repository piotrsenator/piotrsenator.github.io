---
layout: city
title: Vienna
---
<main class="page-wrapper city-page">
  <article>
    <h1 class="page-title">{{ page.title }}</h1>
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

    <div class="button-center" style="margin-top: 2rem;">
      <a class="button subtle" href="/my-cities/">← Back to cities</a>
    </div>
  </article>
</main>

