---
layout: page
title: InDesign to the Fixed Layout ePub
published: true
tags: InDesign
categories: [InDesign, ePub]
# screencast: [anchoringimages]
---
<!-- TOC depthFrom:2 depthTo:2 withLinks:1 updateOnSave:1 orderedList:0 -->
<section class='toc'>
## On this Page

- [The Basics](#the-basics)
- [InDesign export to ePUB (fixed layout)](#indesign-export-to-epub-fixed-layout)
- [Export ePUB (Fixed Layout)](#export-epub-fixed-layout)
- [How Does our Fixed-Layout ePUB look?](#how-does-our-fixed-layout-epub-look)

</section><!-- /TOC -->
# InDesign to the Fixed Layout ePub

The fixed-layout format ePUB3 format provides a way to deliver every single page in your print book laid out just as it was in the print version.

This fixed-layout format can be considered almost the same as an interactive PDF, however, as you will see, the ePUB can have much more interactivity and, you, the designer can control the way the eBook is displayed. For those that ask ‘why can’t I deliver a PDF?’. The answer is that you cannot sell and distribute a PDF through the same channels as the ePUB (or Kindle) format eBooks.

## The Basics

InDesign Creative Cloud 2014 introduced the ability to export the ePUB3 as a fixed-format package, and we can use this method to create a perfect acceptable ePUB3. However, it should be pointed out that the controls for the way certain aspects work in the export process, are limited:

 - There is no way to include footnotes as popups (they will simply be at the bottom of the page - as in your print version)
 - You cannot use the Articles panel to order content, or even prevent some objects from exporting.
 - All items will be delivered as they appear, including the master page items.
 - Post editing the CSS is almost impossible, because every single word on the page is positioned with the CSS, so you dare not make any adjustments.

## InDesign export to ePUB (fixed layout)

The instructions for this are very limited, but we should first explain that the fixed-layout ePUB is formed from many XHTML files – one for every single page that you see in the InDesign view. Whichever method you use for this output, you need to become aware of the individual pages (how they begin and end, if there are orphans and widows, and what your master page items look like. Effectively, you are now designing as if for print.

### Duplicate and move on.

I suggest that you duplicate your InDesign documents and book, because you might (for this fixed-layout edition) be making some destructive changes. You need to *fork* this file as a new version.

### Page by Page

Go through all the pages, and satisfy yourself that each page is how you want it to be. You can make adjustments to fix widows and orphans. You should be certain that the master page items display correctly. Items can go to the edge of the page.

> **Note:** We have noticed that if images bleed off the page (as you might for print) then you might observe scroll bars in the exported ePub.

You will need an InDesign document set up as if for a re-flowable eBook.

Images are likely to be anchored in the text, although technically, for the fixed layout ePub you do not need images to be anchored. Since this is all about trying to use the same file for these different techniques, we should have anchored images!

Note: Images can now use the full size of the page, so you can move the images right to the edge of the page.

You will need to be using InDesign Creative Cloud. The screen images in this document are created from InDesign version 11.1.

Having had a good look at our InDesign book and files, we only have one matter to address – do we want the table of contents on the page or just as a logical TOC? If the TOC is on the page, then it will be on the page in the ePUB (fixed layout). If you don’t want this, you need to move it on to the paste board and delete those blank pages.

In the fixed-layout format for Apple devices there are 2 types of ‘tables of contents’; you will always have a thumbnail image version, but your table of contents in InDesign will also provide a logical menu item TOC, that will be available in a drop-down menu.

## Export ePUB (Fixed Layout)

I am presuming that you will export from the book panel, but if you are working with a single file, then the procedures are exactly the same. You will already be familiar with the panel that appears when you export the ePUB, only this time the features are limited.

### The General Section

[![In this panel you can decide how the spread will be handled](/images/2017/02/id2fxlePub/image1.jpeg)](/images/2017/02/id2fxlePub/image1.jpeg)

In the General panel you will need to select the cover image and the table of contents as a Multi Level Navigation from your saved TOC in InDesign.

There are Spread Layout options that will control the way the spread is formed. You can even join the pages as a landscape form. On the other hand, you may simply base the spreads on your layout (as if for print). You can also choose to Disable the Spreads so that only one page will show in a portrait format.

> **Note:** If you decide to convert Spread to Landscape, it will be worth re-organising the pages so that the first is a spread. This will mean adding a page at the beginning.

If you do want to convert the spread to a landscape view you may want to look at adding a thin line to divide the 2 pages and even consider using the full width of the 2 page spread to add an image.

### The Conversion Settings

[![Choose the best quality for images unless the file size will become too large.](/images/2017/02/id2fxlePub/image2.jpeg)](/images/2017/02/id2fxlePub/image2.jpeg)

In this panel we can decide how the export process will convert the graphics in your book.

The other panels that you can select include the following:

The CSS panel allows you to add your own CSS, however there are few adjustments that we are likely to need to make. Likewise the javascript panel provides a chance to add javascript, as we did for the reflowable ePUB in the earlier chapter.

We will need to add Metadata in the appropriate panel, before we proceed.

## How Does our Fixed-Layout ePUB look?

[![A sample spread in iBooks](/images/2017/02/id2fxlePub/image1.png)](/images/2017/02/id2fxlePub/image1.png)

You will see pages exactly as you had in the InDesign. Is this successful?

Certainly. If this is what you wanted, then we can surely say that we have a good fixed-layout eBook. But take a look at another image from a spread in the play.

[![A spread showing that footnotes remain just that. No popups are possible](/images/2017/02/id2fxlePub/image2.png)](/images/2017/02/id2fxlePub/image2.png)

Here we see the problem with our footnotes. They are appearing as they did in the print version and we have no possibility of interactive popup notes.

Now have a look at the XHTML of one page in the eBook.

[![The complexity of the markup is overwhelming](/images/2017/02/id2fxlePub/image3.png)](/images/2017/02/id2fxlePub/image3.png)

If you look carefully, you will see that every word on the page is wrapped in a span tag with a position set through an inline style rule. This is the way that InDesign has exported the content and it works to precisely position all content on the page. The problem comes when you want to make any edits after-export. We have little hope of making any changes to the CSS other than possibly adding a background colour to the pages.
