---
layout: post
title: Validation
date: '2017-02-03 15:39'
categories:
  - HTML
---
Everything needs to be perfect for it to work in the digital domain. Or does it? Can our screens forgive our little markup errors?

## Checking for Errors. We have to do it so often!

If you create web sites, apps or eBooks then you are sure to have a few mark-up errors. So how can we check for errors?

### HTML

In the world _wild_ web there are several flavours of HTML markup in use, and in a previous post we talked of HTML5 and XHTML. At one time it was possible to be able to choose your favourite from HTML3, HTM4 and even transitional versions.

But what does it mean to have different versions? To a certain extent this is really a chronological thing. As you would expect, as time goes by, things improve and new versions make the experience of rendering HTML into a web page gets better. But it wasn't always so straightforward because web browsers have often interpreted the HTML tags and stylesheets (CSS) in different ways. Oftentimes a web developer would start off by making the markup valid (according to the rules) but then the web browser would deliver the unexpected and hacks would need to be applied.[^1]

## Forgiveness is a dangerous thing

The latest iteration of HTML is known as `HTML5` although, in fact some have suggested that we don't need versions anymore. We're beyond that now. It's just HTML. Anyway, HTML5 doesn't really replace earlier versions, it just builds on them. With HTML5 you get the ability to use some special tags that had previously been needed and were made to work in a 'roundabout' way:

Previously:

```html
<div class="navigation">
... some menu items
</div>
```

Now we can just use:

```html
<nav>
... some menu items
</nav>
```

But also, HTML5 is very forgiving, because you can leave tags unclosed and the browser is supposed to take a jolly good guess at what is supposed to be.

## Doctypes

In a pre-HTML5 world, web pages needed a _doctype_ at the head of the markup, so that if you really wanted to deliver to a particular HTML version, the browser _was supposed to_ read that first to interpret correctly. Maybe it did, maybe it didn't (I won't go into **quirks** mode).

Still, doctypes are significant if you need to validate the markup (stay with me here, because we **do** need to validate for the ePub).

Let's have a look at some doctype declarations:

Here is a transitional one:

```html
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
```
Here is a strict one:

```html
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
```

And here is HTML5, pure and simple, no references to data held on the web:

```html
<!doctype html>
```

## How can we validate?

### HTML
You can validate your web page by [going to this web site][d2ef4529]{target=_new} and putting in the a link to the file.

  [d2ef4529]: https://validator.w3.org/nu/ "The online validator"

There are several options, but be aware that the validation process needs to know what HTML version you are using, and it gets this from the DOCTYPE.

All being well you should see something like this:

[![We succesfully validated this XHTML file](../../images/2017/02/validation1.png)](../../images/2017/02/validation1.png)

## ePub

The ePub standard for delivering eBooks is a wrapped-up package of files, consisting (mostly) of HTML and CSS, although, actually the HTML is a particular flavour; `XHTML5`. This means that it must conform to a very strict set of rules.


We need to validate our web page for both the HTML markup and the CSS. To do this we can use online validation services.

The sample page that I have produced has validated but we need to aware of a few things:

First the web page must be named with .xhtml. This will inform the validator that we are using XHTML rather than just plain HTML.

Why is this? Well it turns out that ePUB3 (the eBook format that we are targeting) uses this markup standard, so we want to do the same from the beginning of our learning about these things.

One thing I noticed today was that the validator uses a new system and page layout.

So, to validate the HTML go here: https://validator.w3.org/

To validate the CSS go here: https://jigsaw.w3.org/css-validator/



[^1]: Chris Colyer's Website is the [goto place][7faa4e4f] for browser hacks:

  [7faa4e4f]: https://css-tricks.com/snippets/css/browser-specific-hacks/ "Off to the web"
