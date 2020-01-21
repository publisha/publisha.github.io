---
title: Scrolling Text Frame in Fixed-Layout ePub
date: 2017-03-31
YouTube: zFQJ8rLFnWo
layout: screencast
categories: [InDesign, ePub, "Multi-Platform Publishing"]
---
First things: I am not using the overlays feature of InDesign.

It is not possible to add scrolling text fields in a reflowable ePUB, but with the fixed layout format we can add a text box on a page and include (almost) as much scrolling text as you like.

Here are the instructions to create a vertical scrolling text for the ePUB(Fixed Layout).

Start a new document in InDesign with a very long vertical page size (maximum height is about 5000pixels). This really just depends on the length of your text!

Paste your long text into a text field on this page.

Make sure there is no overset text. Reduce the size of the text field so that the text just fits. Copy this this text field (not just the contents but the selected object).

In your target InDesign file create an empty text field wider that the one you created in the other temporary InDesign document.

Select the text field and ‘Paste Into’ this selected text box.You can select all of this text and style accordingly.

With the parent text box selected, create an Object Style and set the export tagging for HTML and ePUB to a <div> with a class of ‘scroller’.

Create a CSS file with the following:

```css
div.scroller {
position: relative;
border:1px solid silver;
}
div.scroller > div {
overflow: auto;
overflow-y:scroll;
overflow: scroll;
overflow-x:hidden;
-webkit-overflow-scrolling:touch;
}
```

Add this CSS file into the CSS panel when you export.

There may be other adjustments that you can make to the CSS, but essentially, this will created a scrolling text field.

You may notice that there is no scroll bar on the iPad until you actually touch the field. You may want to include an instruction above or below the text field to indicate that scroll is available.

As an alternative to using InDesign to create a nested text field, you could also consider leaving a blank page and then adding the text directly into the HTML after unpacking the ePUB package. Just create a web page and then copy the content from within the <body> tag and paste into the ePUB page. With additional styling you can then achieve the same as before.
