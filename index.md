---
layout: default
title: Home
published: true
---
# Publisha Helper

Right now a lot of my documents are to found on my [PagetoScreen][b016960a] web site. I also have created lots of PDFs for my students and often printed these out (sometime 70 copies!).

Now it is time (surely) to make all of these helpful documents digital and online, so I can update very easily.

  [b016960a]: http://www.pagetoscreen.net "Lots of useful information"

<section class='categories'>
## Contents by Category
{% for category in site.categories-list %}
### {{ category }}
  <ul>
    {% for page in site.pages %}
        {% for cat in page.categories %}
          {% if cat == category %}
            <li><a href="{{ page.url }}">{{ page.title }}</a></li>
          {% endif %}
        {% endfor %}
    {% endfor %}
  </ul>
  {% endfor %}
</section>
