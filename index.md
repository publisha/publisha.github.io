---
layout: default
title: Home
published: true
images: full-width
---
# What is this website about?

Chris Jennings teaches at Oxford Brookes University for Undergraduate and Postgraduate modules on Digital Publishing. He also is a consultant specialising in eBook Production.

Right now a lot of my documents are to found on my [PagetoScreen][b016960a] web site. I also have created lots of PDFs for my students and often printed these out (sometime 70 copies!).

Now it is time (surely) to make all of these helpful documents digital and online, so I can update very easily.

[b016960a]: http://www.pagetoscreen.net "Lots of useful information"

You will find here help documents and tutorials and a range of topics including using Adobe InDesign and Apple iBooks Author, as well as using GitHub to edit documents within a repository.

More documents are being added and you can find the list within the left hand menu. Just click on the icon top left.

Project maintained by @Pageboy

Here is a random photo taken by me.

[![My shadow bottom right. View from Wittenham Clumps by the Thames at Dorchester.](/images/2017/01/fromWittenhamClumps.jpg)](/images/2017/01/fromWittenhamClumps.jpg)

## How was this Web site built?

### Jekyll
The site is built with Jekyll which you can [find out about here][92c344c3]{:target="_blank"}.

It is delivered on a GitHub repository with GitHub pages. My preferred writing tool is Atom 'cos you can customise it!

[92c344c3]: https://jekyllrb.com "Visit the Jekyll web site"

### Atom
Atom is the free text editor that comes from GitHub. [You can get it here][f9a83765]{:target="_blank"}.

[f9a83765]: https://atom.io "Get Atom"

I based this look and feel on the [Lanyon theme from here][2b9a33ee]{:target="_blank"}.

[2b9a33ee]: http://lanyon.getpoole.com/ "Lanyon"

Images can be enlarged and use a variation of [Fancybox][f6b39499]{:target="_blank"} using jquery.

[f6b39499]: http://fancybox.net "Take a look at Fancybox"

<section class="categories">
<h2 class="header">Pages by Category</h2>
{% for category in site.categories-list %}
  <h2><a href="#">{{ category }} <i class="fa fa-caret-down" aria-hidden="true"></i></a></h2>
    {% for page in site.pages %}
     {% for cat in page.categories %}
          {% if cat == category %}
            <h3><a href="{{ page.url }}">{{ page.title }} <i class="fa fa-caret-right" aria-hidden="true"></i></a></h3>
          {% endif %}
        {% endfor %}
    {% endfor %}
      {% endfor %}
</section>
