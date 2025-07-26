---
layout: city
title: Vienna
slug: vienna
permalink: /cities/vienna/
---

{% assign city = 'vienna' %}

## Food & Drink
{% assign category = 'food' %}
{% for note in site.notes %}
  {% if note.city == city and note.category == category %}
  - [{{ note.title }}]({{ note.url }})
  {% endif %}
{% endfor %}

## Walks & Views
{% assign category = 'walks' %}
{% for note in site.notes %}
  {% if note.city == city and note.category == category %}
  - [{{ note.title }}]({{ note.url }})
  {% endif %}
{% endfor %}

## Arts & Heritage
{% assign category = 'culture' %}
{% for note in site.notes %}
  {% if note.city == city and note.category == category %}
  - [{{ note.title }}]({{ note.url }})
  {% endif %}
{% endfor %}

## Outings & Excursions
{% assign category = 'trips' %}
{% for note in site.notes %}
  {% if note.city == city and note.category == category %}
  - [{{ note.title }}]({{ note.url }})
  {% endif %}
{% endfor %}
