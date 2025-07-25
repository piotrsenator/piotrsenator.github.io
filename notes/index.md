---
layout: default
title: Notes
permalink: /notes/
---

<h2>Notes</h2>

<ul class="note-list">
  {% for note in site.notes %}
    <li><a href="{{ note.url }}">{{ note.title }}</a> <span class="date">{{ note.date | date: "%Y-%m-%d" }}</span></li>
  {% endfor %}
</ul>
