---
layout: default
title: Notes
permalink: /notes/
---

<main>
  <div class="page-wrapper">
    <h1 class="page-title">Notes</h1>

    <ul class="note-list">
      {% for note in site.notes %}
        <li>
          <a href="{{ note.url }}">{{ note.title }}</a>
          <span class="date">{{ note.date | date: "%Y-%m-%d" }}</span>
        </li>
      {% endfor %}
    </ul>
  </div>
</main>
