---
layout: city
title: Vienna
slug: vienna
permalink: /cities/vienna/
---

## Food & Drink
{% assign city = 'vienna' %}
{% for note in site.city_notes %}
  {% if note.tags contains city and note.tags contains 'cafés' %}
    - [{{ note.title }}]({{ note.url }})
  {% endif %}
{% endfor %}

## Walks & Views
...

## Arts & Heritage
...

## Outings & Excursions
...
