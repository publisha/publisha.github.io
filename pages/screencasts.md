---
layout: page
title: Screencasts from the PagetoScreen YouTube Channel
published: true
---

# Screencasts

These screencasts are pulled in from my [YouTube channel][fc76014b].

  [fc76014b]: https://www.youtube.com/channel/UCk1bhTLPDzbqm-tEMBYId1w "Subscribe at YouTube"

<div class="posts">
  {% for screencast in site.screencasts %}
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

<!-- <a class="video fancybox.iframe" title="XML output from InDesign" href="https://www.youtube.com/embed/izYu_V-MKeI?autoplay=1;rel=0&amp;showinfo=0"><i class="fa fa-youtube-play fa-3x" aria-hidden="true"></i></a>
## Exporting from InDesign to XML

Including exporting to XML and viewing in TextWrangler.

In our InDesign document all content needs to be attached to an appropriate style element.

<a class="video fancybox.iframe" title="From InDesign to reflowable ePub" href="https://www.youtube.com/embed/-bXM3_viRoE?autoplay=1;rel=0&amp;showinfo=0"><i class="fa fa-youtube-play fa-3x" aria-hidden="true"></i></a>
## From InDesign to Reflowable ePub first steps

 This video shows you what happens when you first export to the reflowable ePub from a print ready InDesign book file. Then we see what we have to change to get better results.



<a class="video fancybox.iframe" title="Using the Articles Panel to determine content order in the eBook" href="https://www.youtube.com/embed/cBiOheSPECY?autoplay=1;rel=0&amp;showinfo=0"><i class="fa fa-youtube-play fa-3x" aria-hidden="true"></i></a>
## Using the Articles Panel to determine content order in the eBook

When we export our book to the reflowable ePub from InDesign, we have a choice about the content order. Usually we choose 'Based on Page Layout', but if you want to make sure that your front matter pages don't end up at the back of the book, then you need to use the Articles Panel to organise the content.

<a class="video fancybox.iframe" title="Getting better at exporting to the ePub reflowable" href="https://www.youtube.com/embed/5WXSmuyMRRg?autoplay=1;rel=0&amp;showinfo=0"><i class="fa fa-youtube-play fa-3x" aria-hidden="true"></i></a>
## Getting better at exporting to the ePub reflowable

We notice that there a few things that don't seem to match what we have in our print version. Can we make some changes to the InDesign document before we export again? -->
