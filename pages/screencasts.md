---
layout: default
title: Screencasts from the PagetoScreen YouTube Channel
published: true
---

<h1>Screencasts</h1>

<p>These screencasts are pulled in from my <a href="https://www.youtube.com/channel/UCk1bhTLPDzbqm-tEMBYId1w">YouTube channel</a></p>

<div class="posts">

{% assign items = site.screencasts | sort: 'date' %}
  {% for screencast in items reversed limit:30 %}
  <div class="post">
  <a class="video fancybox.iframe" title="{{ screencast.title }}" href="https://www.youtube.com/embed/{{ screencast.YouTube }}?autoplay=1;rel=0&amp;showinfo=0"><i title="Show this screencast" class="fa fa-youtube-play fa-3x" aria-hidden="true"></i></a>
  <h2>{{ screencast.title }}</h2>
  <span class="post-date">{{ screencast.date | date_to_string }}</span>
  {{ screencast.content }}
  {% if screencast.categories != null %}
  <p><b>Filed under:</b> {{ screencast.categories | join: ', ' }} | <a href="{{ site.baseurl }}{{ screencast.url }}">Permalink to this Screencast</a></p>
  {% endif %}
  </div>
  {% endfor %}
</div>
