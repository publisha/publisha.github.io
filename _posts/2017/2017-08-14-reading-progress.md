---
layout: post
title: "Reading Progress Indicator"
date: "2017-08-14 17:07"
published: true
categories: [HTML, CSS, ePub]
comments: true
---
Some time ago I wrote a post over on [pagetoscreen.net][e7c525bd] about a progress bar in a fixed-layout eBook. In that article I also made a link to a web site that spoke about implementing the progress bar in HTML5.

  [e7c525bd]: http://www.pagetoscreen.net/journal/item/page_numbers "read this piece from a while ago"

More recently, I was grateful to have been shared a link to an article by the very same [Pankaj Parashar][28dc5a67].

  [28dc5a67]: https://css-tricks.com/reading-position-indicator/ "Reading Position Indicator"

The idea is that when scrolling through a long article in a web browser, the scroll bar on the right is not really a strong enough indicator to the user, as to the amount of text that has been read, and how much remains.

Some discussions do suggest that the usual scroll bar is enough, but, there again, the scrollbar disappears when the current window is not active. Of course, this varies over different browsers and platforms.

Pankaj Parashar's article demonstrates the indicator at the top of the current window, but I agreed with some comments that this might be mistaken for some _content still loading_, so I have implemented on this web site at the bottom of the window.

You will observe this **reading position indicator** on some pages of this web site, although, I suspect, not on the article that you are reading, because it is (after all), rather short. The indicator is made to be very slightly transparent, to show the content underneath. I have also made the colour suitably adjusted to blend nicely with the overall scheme of the site.
