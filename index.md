---
layout: default
title: Home
---

<section class="motto" style="background-color: #DCE8ED; padding: 2rem; font-style: italic;">
  <p>I question, I challenge, I choose my own trail – in work and in life.</p>
</section>

<section class="about-preview" style="margin-top: 2rem;">
  <h2>About Me</h2>
  <p>Hello, I’m Piotr Senator. I build, I observe, and I reflect — across borders, disciplines, and ideas.</p>
  <p><a href="/about" class="btn" style="background-color:#1F3D2D; color: white; padding: 0.5rem 1rem; border-radius: 0.3rem;">More about me</a></p>
</section>

<section class="cities-preview" style="margin-top: 2rem;">
  <h2>My Cities</h2>
  <div class="city-grid">
    {% for city in site.data.cities %}
      {% include city_card.html city=city %}
    {% endfor %}
  </div>
</section>

<section class="trail-preview" style="margin-top: 2rem;">
  <h2>Off the Trail</h2>
  <div class="trail-grid">
    {% assign previews = site.trail_items | slice: 0, 6 %}
    {% for item in previews %}
      {% include gallery_item.html item=item %}
    {% endfor %}
  </div>
  <p><a href="/off-the-trail">See all trips</a></p>
</section>

<section class="notes-preview" style="margin-top: 2rem;">
  <h2>Notes</h2>
  <ul class="post-list">
    {% assign latest_notes = site.posts | sort: 'date' | reverse | slice: 0, 3 %}
    {% for post in latest_notes %}
      {% include post_preview.html post=post %}
    {% endfor %}
  </ul>
  <p><a href="/notes">Read all notes</a></p>
</section>

