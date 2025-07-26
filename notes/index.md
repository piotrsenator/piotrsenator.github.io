---
layout: default
title: Notes
permalink: /notes/
---

<main>
  <div class="page-wrapper">
    <h1 class="page-title">Notes</h1>

    <div class="note-previews-grid">
      {% for note in site.notes %}
        <article class="note-card">
          <h3><a href="{{ note.url }}">{{ note.title }}</a></h3>
          <p>{{ note.excerpt | strip_html | truncatewords: 30 }}</p>
          <p class="note-date">{{ note.date | date: "%d %B %Y" }}</p>
        </article>
      {% endfor %}
    </div>
  </div>
</main>
