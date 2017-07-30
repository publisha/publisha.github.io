---
layout: page
title: Master Pages in InDesign
published: true
tags: InDesign
categories: [InDesign, "Design and Production"]
date: 2017-07-30
blurb: The Pages panel will show you the pages in your document as thumbnails. You can configure the way this displays through the Panel Options from the context menu in the Pages panel.
---
<!-- TOC depthFrom:2 depthTo:2 withLinks:1 updateOnSave:1 orderedList:0 -->
<section class='toc'>
## On this Page

- [The Pages Panel](#the-pages-panel)
- [Page Numbers](#page-numbers)
- [Different Page Number Styles](#different-page-number-styles)
- [Headers](#headers)
- [Running Header](#running-header)
- [Overriding Master Page Items](#overriding-master-page-items)
- [Using the Book Panel](#using-the-book-panel)

</section><!-- /TOC -->
# Master Pages in InDesign
**Or How to Repeat Content**

## The Pages Panel

The Pages panel will show you the pages in your document as thumbnails. You can configure the way this displays through the Panel Options from the context menu in the Pages panel.


[![Configure the pages panel to suit your needs](/images/2017/04/masterpages/image2.png)](/images/2017/04/masterpages/image2.png)


[![The pages panl shows the page numbers](/images/2017/04/masterpages/image3.png)](/images/2017/04/masterpages/image3.png)

In the image here, the pages panel shows the current pages in a scrolling pane, with the master pages on the top. In our document we only have the `A-Master` and this is applied to all pages in the file. We can add Master Pages and base one on another, so we effectively create a hierarchy of page attributes.

## Page Numbers

One common use for the Master Pages is to add a header and footer across a range of pages.

To add page numbers go to the master pages (in this case A-Master) and create a text box at the bottom left of the left hand page. With the text cursor in that box, go to the menu: `Type>Insert Special Character>Markers>Current Page Number`


[![Page numbers are found under the 'Insert Special Character' menu.](/images/2017/04/masterpages/image4.png)](/images/2017/04/masterpages/image4.png)


[![The letter 'A' here represents the name of the master page](/images/2017/04/masterpages/image5.png)](/images/2017/04/masterpages/image5.png)

You can add text before the letter A (this represents the page number itself), such as ‘Page:’ You should style this text block as you prefer.

Copy this and paste to the right hand page of ‘A-Master’. You will now see the page numbers displayed at the bottom of each of the pages in the document.

## Different Page Number Styles


[![Page numbers can take different forms - roman or arabic](/images/2017/04/masterpages/image6.png)](/images/2017/04/masterpages/image6.png)

In a printed book, you will often see different page numbers for the front matter. You may often see page numbers using small Roman Numerals. The text of the book proper may start after this ‘front-matter’. To achieve this we need to use the Numbering and section Options. We may need to start a new section at a particular page, and then use the alternative page numbering styles.

## Headers

It is traditional to add headers to the pages in a book. In the headers we can include the title of the book and possibly the section or chapter name.


[![Headers can be repeated by using the master pages](/images/2017/04/masterpages/image7.png)](/images/2017/04/masterpages/image7.png)

Once again, in the master pages (A-Master) we can add text blocks to the top of the page. In the example here, I have also added a coloured bar; this will also repeat on all pages that use the ‘A-Master’.

## Running Header

In order to achieve the display of the current chapter, we need to use ‘Text Variables’. We need to tell InDesign which style we are using for the chapter name, and then this text can be displayed in place of the variable that we select.

In the ‘A-Master’, we should first add a text box as before, but this time we need to insert the Text Variable>Running Header.


[![Insering or editing the Text Variables'](/images/2017/04/masterpages/image8.png)](/images/2017/04/masterpages/image8.png)

Now we need to define where this variable gets its value, by going to:

Type>Text Variables>Define. Select the Running Header and then in the dialogue box here, we need to select the paragraph style that the chapter heading is using.


[!['Running Header' is default named Text Variable ](/images/2017/04/masterpages/image9.png)](/images/2017/04/masterpages/image9.png)

As you can see there are other changes we can make to the text, if we need.


[![You will see the name of the Text variable displayed on the master page](/images/2017/04/masterpages/image10.png)](/images/2017/04/masterpages/image10.png)

## Overriding Master Page Items

There are some situations where you want to remove the master page items on a particular page. One example might be where a page has a fully bled image and there is no space for the page numbers or headers; or maybe you just want a different style of page numbers for these types of pages.

There are 2 approaches to this problem. You could create a new master page—based on the ‘A-Master’ but with a different style for the headers and footers. This is the sensible choice where you know that this type of page is required more than once.

Alternatively, on one particular page, you can use the menu (from the pages panel context selector) ‘Override All Master Page Items’. This will bring all of the items on the master page on to the page where you can delete them. If you just want one item removed then hover over the item and use the keys: `shift-cmd` while you click the mouse. This will bring this one item onto the page, for you to delete or modify.

## Using the Book Panel

When combining chapters in a book we need to pay special attention to the way the master pages are synchronised across the different chapters.

You may want the master page items (such as book title in the header), to be the same across the whole book. However, if you are looking to use a different header in each chapter (maybe different colour banner), then do NOT synchronise the master pages.

These details are covered in another helper document - ‘Using the Book Panel in InDesign’.
