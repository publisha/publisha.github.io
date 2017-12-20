---
  title: InDesign to HTML and CSS
  published: false
  categories: [InDesign, HTML, “Multi-Platform Publishing”]
  screencast:
  date: 2017-11-22
  blurb: HTML is the language for the web; delivering content for our various types of screens. InDesign is a *page layout* tool; presuming for the printed page, but we can still generate HTML from our content and with some attention to detail, we can can get good HTML markup ready for further styling and attention to a responsive design.
  order: 2
---
When we export InDesign to ePub, content is marked-up as HTML and styles are converted to CSS. We can also export to HTML and same thing happens, but what should we do to make sure our HTML and CSS are perfectly formed and can also (if needed) be edited.

## Introduction
In this detailed description, we are going to use our Shakespeare play to create a single web page but with an interactive navigation block that will help is locate the Acts and Scenes.

## From Styles to Markup

Of course we have developed good habits and have made sure that all content has styles attached. we avoid overrides and adjusting appearance with bespoke settings. We also avoid adding empty paragraphs to achieve space. Once we have our styles applied (paragraph, character and objects) we then need to instruct InDesign what HTML tags to apply to those elements on export.

## Two Features we need first

- If you have already mapped your styles to tags by name and have an XML structure then this will be a marvellous benefit.
- If you have a table of contents then we can use this to generate a friendly menu for navigation.

### Check your XML structure

We will generate the HTML *based on the XML Structure* so only those elements will appear in the HTML. You *can* base the export on the layout but this may give some unwanted elements.

### Build the Table of contents

If you don't have a TOC then get InDesign to build one. You don't need to worry about how this looks but use an unordered list to style. You'll need the nesting sorted (Scenes inside Acts).

see the page for the toc
do i need to explain the lists (or another page?)

## HTML tags

You should know what HTML tags can be used. Please do read up on the basic introduction to HTML and CSS, because you will need to configure each style to use a particular tag; inline tags such as `<em>` and `<strong>` or block level tags like `<h1>` and `<div>`.

In the style settings for each element (paragraph or character), there is a section **Export Tagging**.

We can makes this setting for each style in turn or we can use the InDesign panel for `Edit All Export Tags` that helps us makes these settings in one place.

### Class names

HTML tags can also have class names that will give us even more control over the styling in the web page that we are going to construct.

## HTML and CSS

Styles are applied to HTML Elements
with CSS rules

## InDesign Styles

- Paragraph styles
- Character Styles
- Object Styles
- Table styles
