---
layout: default
title: Security Blog
nav_exclude: true
---

<section class="home-hero">
  <h1>Security Engineering, Cloud Security and Detection Engineering</h1>
  <p>Writeups, lessons learned, and practical guidance focused on building reliable defenses and improving detection coverage.</p>
  <div class="signal-row">
    <span class="signal-chip">Cloud Security</span>
    <span class="signal-chip">Detection Engineering</span>
  </div>
</section>

<h2 class="section-title">Latest Posts</h2>

<div class="post-grid">
{% for post in site.posts limit: 6 %}
  <a class="post-card" href="{{ post.url | relative_url }}">
    <p class="meta">{{ post.date | date: "%b %-d, %Y" }}{% if post.categories and post.categories.size > 0 %} · {{ post.categories | first | replace: '-', ' ' | capitalize }}{% endif %}</p>
    <h3>{{ post.title }}</h3>
    <p class="excerpt">{{ post.excerpt | strip_html | truncate: 125 }}</p>
  </a>
{% endfor %}
</div>
