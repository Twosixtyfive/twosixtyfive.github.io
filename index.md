---
layout: default
title: Home
---

<section class="hero">
  <h1>Welcome to twosixtyfive</h1>
  <p>Exploring the intersections of technology, privacy, and digital design.</p>
</section>

<section>
  <h2>Latest Updates</h2>
  <div class="card-grid">
    {% for post in site.posts limit:3 %}
      <div class="card">
        <h3>{{ post.title }}</h3>
        <p>{{ post.excerpt | strip_html | truncate: 100 }}</p>
        <a href="{{ post.url | relative_url }}" style="color: var(--accent); font-size: 0.8rem; text-decoration: none; font-weight: bold;">Read more &rarr;</a>
      </div>
    {% endfor %}
  </div>
</section>
