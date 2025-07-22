---
layout: default
title: Notes
---

# Notes

These are fragments of thought, travel reflections, book annotations, or strategy sketches. I write them as I go.

{% for post in site.posts %}
  {% include post_preview.html post=post %}
{% endfor %}

<div class="pagination">
  {% if paginator.previous_page %}
    <a href="{{ paginator.previous_page_path }}">← Previous</a>
  {% endif %}
  {% if paginator.next_page %}
    <a href="{{ paginator.next_page_path }}">Next →</a>
  {% endif %}
</div>
