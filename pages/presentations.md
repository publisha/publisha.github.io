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
  <h2>{{ presentation.title }}</h2>
  <span class="post-date">{{ presentation.date | date_to_string }}</span>
  <div style="position:relative;">
  <iframe src="/keynotes/{{ presentation.folder }}/assets/player/KeynoteDHTMLPlayer.html" width="280" height="156" style="padding:1px;margin:0;" frameborder="0"></iframe>
  <a title="see the complete presentation" href="{{ site.baseurl }}{{ presentation.url }}" style="position:absolute; top:0px; left:0px; width:280px; height:156px; z-index:5;"></a>
  <p class="caption" style="font-size:70%;">The presentation page is available on clicking this first slide</p>
  </div>
  {% comment %}{{ presentation.content }}{% endcomment %}
  {% if presentation.categories != null %}
  <p><b>Filed under:</b> {{ presentation.categories | join: ', ' }} | <a href="{{ site.baseurl }}{{ presentation.url }}">Permalink to this Presentation page</a></p>
  {% endif %}
  </div>
  {% endfor %}
</div>
