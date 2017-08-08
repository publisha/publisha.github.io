---
layout: default
title: Presentations generated from Keynote
published: true
permalink: presentations/index.html
---

<h1>Presentations</h1>

<p>These presentations have been created with Apple's Keynote and then exported to HTML.</p>

<div class="posts">

{% assign items = site.presentations | sort: 'date' %}
  {% for presentation in items reversed limit:30 %}
  <div class="post">
  <h2><a href="{{ site.baseurl }}{{ presentation.url }}">{{ presentation.title }}</a></h2>
  <span class="post-date">{{ presentation.date | date_to_string }}</span>
{{ presentation.excerpt }} 
  {% if presentation.categories != null %}
  <p><b>Filed under:</b> {{ presentation.categories | join: ', ' }} | <a href="{{ site.baseurl }}{{ presentation.url }}">Permalink to this Presentation page</a></p>
  {% endif %}
  </div>
  {% endfor %}
</div>
