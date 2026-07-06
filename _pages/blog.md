---
layout: page
title: Notes
permalink: /notes/
description: Here are some notes I took during my studies. Some of them are not yet finished and are still being updated.
nav_order: 3
pagination:
  enabled: false
---

<style>
.notes-list {
  margin-top: 2rem;
}

.notes-list .note-item {
  margin-bottom: 1.55rem !important;
}

/* Note title: black, normally bold, keep current size */
.notes-list .note-title,
.notes-list .note-title a {
  font-size: 1.08rem !important;
  line-height: 1.4 !important;
  font-weight: 600 !important;
  color: var(--global-text-color) !important;
  text-decoration: none !important;
  margin: 0 0 0.35rem 0 !important;
}

/* Keep title black also when hovering */
.notes-list .note-title a:hover {
  color: var(--global-text-color) !important;
  text-decoration: none !important;
}

/* Note description: black, normal weight, NOT bold */
.notes-list .note-description,
.notes-list .note-description p,
.notes-list .note-description strong,
.notes-list .note-description b {
  font-size: 1rem !important;
  line-height: 1.45 !important;
  font-weight: 400 !important;
  color: var(--global-text-color) !important;
  margin: 0 0 0.4rem 0 !important;
}

/* Note date */
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
