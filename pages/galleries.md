---
layout: default
title: Galleries of Images
published: true
permalink: galleries/index.html
---

<h1>Image Galleries</h1>

<p>Image galleries from my Flickr stream.</p>

<div class="posts">

{% assign items = site.galleries | sort: 'date' %}
  {% for gallery in items limit:30 %}
  <div class="post">
  <h2><a href="{{ site.baseurl }}{{ gallery.url }}">{{ gallery.title }}</a></h2>
  
  <span class="post-date">{{ gallery.date | date_to_string }}</span>
  <p><a href="{{ site.baseurl }}{{ gallery.url }}">Permalink to this Gallery page</a></p>
  </div>
  {% endfor %}


</div>
