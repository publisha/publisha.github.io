---
layout: default
title: Articles and Conference papers
published: true
permalink: papers/index.html
---
<h1>Papers</h1>

<p>Articles and Conference papers</p>

<p><i>These articles (and more) are published on my <b>Medium</b> publication at:</i></p>

<p><a href="https://medium.com/publisha" title="go to the medium space to view">medium.com/publisha</a></p>

<div class="posts">

{%- assign items = site.papers | sort: 'date' -%}
  {%- for paper in items limit:30 -%}
  <div class="post">
  <h2><a href="{{ site.baseurl }}{{ paper.url }}">{{ paper.title }}</a></h2>
  <span class="post-date">{{ paper.date | date_to_string }}</span>
{{ paper.blurb }}
  </div>
  {%- endfor -%}
</div>
