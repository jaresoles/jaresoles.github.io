---
layout: page
title: Plant and Animal Life and Random Finds
permalink: /finds/
---

Photos, short descriptions, and whatever I was thinking at the time — from walks, fieldwork, or wherever something caught my eye.

<div class="finds-grid">
  {% assign finds = site.finds | sort: 'date' | reverse %}
  {% for entry in finds %}
    <article class="find-card">
      <a href="{{ site.baseurl }}{{ entry.url }}">
        {% if entry.image %}
          <img src="{{ site.baseurl }}{{ entry.image }}" alt="{{ entry.title }}" class="find-thumb">
        {% else %}
          <span class="find-thumb find-thumb--empty"></span>
        {% endif %}
      </a>
      <h3><a href="{{ site.baseurl }}{{ entry.url }}">{{ entry.title }}</a></h3>
      <div class="date">{{ entry.date | date: "%d %b %Y" }}</div>
      {% if entry.content %}
        <p>{{ entry.content | strip_html | truncatewords: 22 }}</p>
      {% endif %}
    </article>
  {% else %}
    <p>Nothing posted here yet &mdash; check back soon.</p>
  {% endfor %}
</div>
