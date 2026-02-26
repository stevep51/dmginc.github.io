---
layout: default
title: Security Blog
nav_exclude: true
---

<section class="home-hero">
  <div class="hero-copy">
    <h1>{{ site.data.site_text.home.title }}</h1>
    <p>{{ site.data.site_text.home.intro }}</p>
    <div class="signal-row">
      {% for chip in site.data.site_text.home.chips %}
      <span class="signal-chip">{{ chip }}</span>
      {% endfor %}
    </div>
  </div>
</section>

<h2 class="section-title">{{ site.data.site_text.home.latest_posts_heading }}</h2>

<div class="post-grid">
{% if site.posts and site.posts.size > 0 %}
{% for post in site.posts limit: 6 %}
  <a class="post-card" href="{{ post.url | relative_url }}">
    <p class="meta">{{ post.date | date: "%b %-d, %Y" }}{% if post.categories and post.categories.size > 0 %} · {{ post.categories | first | replace: '-', ' ' | capitalize }}{% endif %}</p>
    <h3>{{ post.title }}</h3>
    <p class="excerpt">{{ post.excerpt | strip_html | truncate: 125 }}</p>
  </a>
{% endfor %}
{% else %}
  <div class="post-empty" aria-hidden="true">
    <div class="empty-line"></div>
    <div class="empty-line short"></div>
    <div class="empty-dots">
      <span></span><span></span><span></span>
    </div>
  </div>
{% endif %}
</div>
