---
layout: default
title: Inicio
---

<section class="featured-posts">
  <h2>Últimos Artículos</h2>
  <div class="posts-grid">
    {% for post in site.posts limit:3 %}
      <article class="post-card">
        <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
        <p class="post-date">{{ post.date | date: "%d/%m/%Y" }}</p>
        <p class="excerpt">{{ post.excerpt | strip_html | truncate: 100 }}</p>
        <a href="{{ post.url | relative_url }}" class="read-more">Leer más →</a>
      </article>
    {% endfor %}
  </div>
</section>