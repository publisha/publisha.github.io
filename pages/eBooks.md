---
layout: default
title: eBooks Published
published: true
permalink: eBooks/index.html
---

<h1>eBooks</h1>

<p>These are the eBooks I have made.</p>

<div class="posts">

{%- assign items = site.eBooks | sort: 'date' | reverse -%}
  {%- for ebook in items limit:30 -%}
  <div class="post">
  <h2><a href="{{ site.baseurl }}{{ ebook.url }}">{{ ebook.title }}</a></h2>
  <span class="post-date">{{ ebook.date | date_to_string }}</span>
  <a title="read about this" href="{{ site.baseurl }}{{ ebook.url }}">
  <img class="medium" src="{{ ebook.coverimage }}" alt="eBook Cover" />
  </a>
{{ ebook.excerpt }}
  <p><a href="{{ site.baseurl }}{{ ebook.url }}"><b>Further details here</b> <i class="fa fa-caret-right" aria-hidden="true"></i></a></p>
  </div>
  {%- endfor -%}
</div>
