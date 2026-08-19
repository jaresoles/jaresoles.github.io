---
layout: page
title: Plant and Animal Life and Random Finds
permalink: /finds/
---

Sometimes I daydream going briefly to places of the past and existing in times that has long passed and of course it remains as a conception that also passes because my brain rapidly rejects and jumps from one thing to the other, but how wonderful it would be if that were possible, and then I realize it is not so impossible through photos and paintings and vivid descriptions in writing - and I feel so completely distraught and heartbroken at the thought that animals and plants that I perceive at this moment are passing and slowly fading into the recesses of humanity's memory. So, I thought I'd do this to remedy what ails my soul. Make no mistake - I am an optimist and this is why I do this, but every once in a while, I cannot comprehend how diabolical we can be to creatures that have vocabularies unreachable to our comprehension. If I could make flowers and grass and weed sprout through concrete and everywhere, the Earth would be nothing more than a meadow to all things that fly, writhe, burrow, moo, meow, croak, bleat and sing (and speak?). Of course, the marine organisms will have their own rightful place. So, this is an attempt to time travel and a resistance to the act of not noticing.

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
  {% endfor %}
</div>
