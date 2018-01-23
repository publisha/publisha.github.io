---
layout: "post"
title: "Using Flickr to Generate an Image Gallery"
date: "2018-01-23 18:57"
published: true
categories: [Flickr, jQuery]
---
We should all be very grateful that Flickr exists. This is one of the most popular (free if you want) hosting services that is also very sophisticated in the way that it delivers, and categorises images. But there is more; Flickr has an **API** that enables you yo pull your hosted pictures down to your own web site. I am doing this here (see the rolling banner on the home page and the galleries).

## What got me started

I have a book in my shelf. It is quite old now. It's called *Flickr Hacks* 2006, O'Reilly Publishers, New York.

[![Flickr Hacks - Bausch and Bumgardner](/images/Screenshot 2018-01-14 19.30.52.png)](/images/Screenshot 2018-01-14 19.30.52.png)

This book is an unusual O'Reilly book, in that it does not have an engraving of an animal but rather the slide projector. As you can see, it's an unbranded Kodak Carousel.

## Flickr

Flickr has been around for a long time and was launched in 2004[^1]. It was taken over by Yahoo and is now owned by them. There are millions of users and there are certainly more than 6 billion public photos.

Enough of the history. The important thing to note is that it is possible to *interogate* flickr's publically available photo streams and deliver to your own web site.

## Hacking the API

The _Flickr Hacks_ book is all about mashing-up the content from Flickr. We are very fortunate that the Flickr organisation have made available an API (Application Programming Interface), whereby the photos can be accessed and pushed onto a web page.

This API was available in 2006 and the book does explore various ways to use images directly from the site, and at the time, I didn't really exploit the potential; preferring to [host photos on my own web site][fe9df4dd].

  [fe9df4dd]: http://www.pagetoscreen.net/lens/category/76 "Take a look at some over on pagetoscreen.net"

## jQuery + FlexBox CSS

So, now with jQuery at our finger tips we can build a gallery of images using the Flickr API and styling with CSS flexBox.

I am now going to point you to the gallery I have built on this site, but before you invoke the link and move away from this page, please note the rolling slide show of images on this home page (I mean the opening page of this site), because those images come from my Flickr account.

I have 2 galleries in progress at the moment but [please have a look at this one][0fadd0bb].

  [0fadd0bb]: https://publisha.github.io/galleries/bookimages/ "Gallery built from Flickr"

[^1]: [Wikipedia][92be4fb2] will give you a brief history.

  [92be4fb2]: https://en.wikipedia.org/wiki/Flickr "Have a look at Wikipedia and make a donation while you're there."
