---
layout: default
title: Notes
permalink: /notes/
---
<section class="note-wrapper page-wrapper">
  <h1 class="page-title">Notes</h1>
  <div class="note-grid">
    {% for note in site.notes %}
      <a href="{{ note.url }}" class="note-tile">
        <h3>{{ note.title }}</h3>
        <p>{{ note.excerpt | strip_html | truncate: 160 }}</p>
        <span class="note-date">{{ note.date | date: "%d %B %Y" }}</span>
      </a>
    {% endfor %}
  </div>
</section>
