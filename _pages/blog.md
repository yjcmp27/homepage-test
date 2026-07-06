---
layout: page
title: Notes
permalink: /notes/
description: Notes on geometry, geometric analysis, gauge theory, and spectral geometry.
nav: true
nav_order: 3
pagination:
  enabled: false
---

<style>
/* Notes page based on blog posts */

/* Whole list */
.notes-list {
  margin-top: 2rem;
}

/* Each item */
.notes-list .note-item {
  margin-bottom: 1.55rem !important;
}

/* Title: close to publication/talk item size */
.notes-list .note-title,
.notes-list .note-title a {
  font-size: 1.08rem !important;
  line-height: 1.4 !important;
  font-weight: 400 !important;
  color: var(--global-text-color) !important;
  text-decoration: none !important;
  margin: 0 0 0.35rem 0 !important;
}

/* Hover */
.notes-list .note-title a:hover {
  color: var(--global-theme-color) !important;
  text-decoration: none !important;
}

/* Description */
.notes-list .note-description {
  font-size: 1rem !important;
  line-height: 1.45 !important;
  font-weight: 400 !important;
  color: var(--global-text-color) !important;
  margin: 0 0 0.4rem 0 !important;
}

/* Date */
.notes-list .note-date {
  font-size: 0.95rem !important;
  line-height: 1.35 !important;
  font-weight: 400 !important;
  color: var(--global-text-color-light) !important;
  margin: 0 !important;
}
</style>

<div class="notes-list">

{% assign sorted_posts = site.posts | sort: "date" | reverse %}

{% for post in sorted_posts %}
  <article class="note-item">
    <div class="note-title">
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </div>

    {% if post.description %}
      <div class="note-description">
        {{ post.description }}
      </div>
    {% elsif post.excerpt %}
      <div class="note-description">
        {{ post.excerpt | strip_html | truncatewords: 40 }}
      </div>
    {% endif %}

    {% if post.date %}
      <div class="note-date">
        {{ post.date | date: "%B %-d, %Y" }}
      </div>
    {% endif %}
  </article>
{% endfor %}

</div>
