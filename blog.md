---
layout: default
title: Blog
---

<section>
  <h2>Blog & Guides</h2>
  <div class="card-grid">
    {% for post in site.posts %}
      <div class="card">
        <h3>{{ post.title }}</h3>
        <p>{{ post.excerpt | strip_html | truncate: 100 }}</p>
        <a href="{{ post.url | relative_url }}" style="color: var(--accent); font-size: 0.8rem; text-decoration: none; font-weight: bold;">Read more &rarr;</a>
      </div>
    {% endfor %}
  </div>
</section>
