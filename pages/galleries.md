---
layout: flickrlist
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

<div class="gallerylist">
  <div id="{{gallery.flickr_album}}"></div>
  <script type="text/javascript" charset="utf-8">

  $(function() {
    // create a gallery with custom options
    var options = {
      apiKey: '{{site.flickr_key}}',
      flickrId: '{{site.flickr_id}}',
      photosetId: '{{gallery.flickr_album}}',
      captions: false,
      small: 'medium',
      large: 'original',
      firstOnly: true
    };

    $('#{{gallery.flickr_album}}').fancyPhotoset(options);

  });
  </script>
</div>
  <span class="post-date">{{ gallery.date | date_to_string }}</span>
  <p><a href="{{ site.baseurl }}{{ gallery.url }}">Permalink to this Gallery page</a></p>
  </div>
  {% endfor %}
</div>
