---
layout: page
title: Contents
permalink: /contents/
---

Every entry on the site, newest first. This page updates itself as new posts and finds are added — nothing to maintain by hand.

### Posts

<ul class="toc-list">
  {% for post in site.posts %}
    <li>
      <span class="date">{{ post.date | date: "%d %b %Y" }}</span>
      <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
    </li>
  {% else %}
    <li class="toc-empty">No posts yet.</li>
  {% endfor %}
</ul>

### Plant and Animal Life and Random Finds

<ul class="toc-list">
  {% assign finds = site.finds | sort: 'date' | reverse %}
  {% for entry in finds %}
    <li>
      <span class="date">{{ entry.date | date: "%d %b %Y" }}</span>
      <a href="{{ site.baseurl }}{{ entry.url }}">{{ entry.title }}</a>
    </li>
  {% else %}
    <li class="toc-empty">Nothing here yet.</li>
  {% endfor %}
</ul>
