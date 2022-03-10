---
layout: page
title: Editing inside the ePUB package
date: 2022-03-10
published: true
categories: ["ePub", "HTML and CSS", "Multi-Platform Publishing"]
tags: [ePub, InDesign, CSS, "Multi-Platform Publishing"]
blurb: When we have created a reflowable ePub by exporting from InDesign, we may find that there are some stylistic details that need tidying up, changing or even correcting. Not all aspects of our wonderfully crafted typographic design work will give perfect results in the ePub.
---
# Editing inside the ePUB package

When we have created a reflowable ePub by exporting from InDesign, we may find that there are some stylistic details that need tidying up, changing or even correcting. Not all aspects of our wonderfully crafted typographic design work will give perfect results in the ePub.

Some text editors have the functionality to edit the components of the ePUB package even without unpacking. BBedit is the one I have used, but Oxygen XML will also give you that ability. Oxygen is more sophisticated and expensive; it will allow you to remove and add files into the package, so if you wanted replace a picture, Oxygen will do it!

These days I use ~*Atom*~ *Vscode* as my text editor and so, although you can view the insides of the ePub package, you need to unpack before editing.

[![Here we see the files within the ePub package using Atom](/images/2017/02/editing_ePub/atomfilelist.png)](/images/2017/02/editing_ePub/atomfilelist.png)

Edit: *Atom* and *Vscode* are very similar

## Unpacking and repacking
For this I recommend downloading eCanCrusher available here: https://www.docdataflow.com/ecancrusher/


## Can we Edit?

It really depends on the software tools that you have.

I tend to use Atom as the text editor, and once you have unpacked the ePub (using the script just described), then you can drag the complete folder onto the Atom app, and this will then become a project that you can edit.

[![The ePub package open for editing with Atom](/images/2017/02/editing_ePub/epubinAtom.png)](/images/2017/02/editing_ePub/epubinAtom.png)

### What Can We edit?

This really depends on how the ePUB looks after export from InDesign and what changes you want to make, but crucially you need to keep your options open to go back to InDesign to make further changes. This means avoiding the editing of the XHTML documents and just focussing on the stylesheets.

In our workflow we plan to return to InDesign for further edits, so let us explore how to create our own copy of the stylesheet (CSS), that we can link back in the next time we export to the ePUB.

### How many CSS files do we have?

If you have used the InDesign book panel to organise your content, you are gong to find several CSS files; one main file with a filename- `idGeneratedStyles_0.css` and then further stylesheets one for each of the documents in your book panel.

The main CSS file is where the generic styles are located (those which are common throughout the eBook), and then each of the others will only include style information for elements present in those separate XHTML files.

All we want to do at this stage is to edit the stylesheet called `idGeneratedStyles_0.css`.

### Our First Correction

You will remember from our previous chapter that we found that an offer rule that provided a background grey block to the Act heading had disappeared when we views the ePUB. Here is a reminder:

[![An indicator showing the missing Act heading](/images/2017/02/editing_ePub/image3.png)](/images/2017/02/editing_ePub/image3.png)

The reason for this error is that InDesign does not export the rules (lines) above or below the paragraphs from the paragraph style settings, and our tex is white so it disappears.

> **Version alert:** Since InDesign 2015 edition it is possible to use `Background Shading` in a paragraph style, so we might us this instead of offsetting a paragraph rule.

The correction we need to make is in

`idGeneratedStyles_0.css`

In our Export Tagging setting we configured the paragraph style called act to use the tag - h1 with a class name of ‘act’. We then look for and find this block in the CSS.

[![The setting for the paragraph rule that gives a background to the text.](/images/2017/02/editing_ePub/image4.png)](/images/2017/02/editing_ePub/image4.png)

We need to add the following line:

`background-color:#a196a0;`

I grabbed the hexadecimal value of the colour from the swatch in InDesign.

We can make adjustments to the height of this block of colour by adjusting the leading – in CSS this is the line-height:

`line-height:1.5;`

[![The styles that InDesign has given us.](/images/2017/02/editing_ePub/image5.png)](/images/2017/02/editing_ePub/image5.png)

## Test and View Our Changes

If you want to view one of your XHTML files when open in Atom, you should obtain an extension called HTML-Preview. With this you can view the page simply. On the other hand, just opening the XHTML file in a web browser will also give a good idea of the result.

[![With the extension to Atom - HTML-Preview we can see the results of our changes right away.](/images/2017/02/editing_ePub/epubinAtomwithpreview.png)](/images/2017/02/editing_ePub/epubinAtomwithpreview.png)

### Roundtrip to InDesign

If we need to return to InDesign then we will lose these corrections that we make to the CSS, because InDesign will generate the same ones again.

Once you have made the corrections that solve the style and display issues, then you can take a copy of the CSS file and save this somewhere in your working files with a logical name (mine is dream.css). The next time that you export the ePUB, we can then select this external CSS file (see the CSS panel when exporting), and this will be added in the head of each XHTML file.

Here we see the listed CSS files - 2 generated by InDesign and one of our own making. This custom one should come after the other 2 so that your rules will override the ones that InDesign has put in.

[![here we see how the mystyles.css has been added](/images/2017/02/editing_ePub/mystyles.png)](/images/2017/02/editing_ePub/mystyles.png)

## Changes to the CSS.

### The page breaks

Each of the XHTML pages represents a new chapter or section (or Act / Scene of the play), and will therefore begin a new page. This has happened because you opted to have the style for the Act or Scene to ‘Split the ePUB’ on export. The paragraph style in the play is ‘act’ and the resulting HTML is:

`<h1 class="act">`

Because for print we also set this up to Start on a New Page (in fact - On Next Odd Page under the Keep Options), InDesign has been less than helpful by applying a rule to the CSS as follows:

`page-break-before:always;`

Guess what! This means that you may get a blank page, because the ePUB gives the eReader software 2 reasons to start a new page

1. It starts a new page because we split the ePub into separate HTML files at the Act start
2. And then because we use 'Keep Option' we get the CSS above.

The line in the CSS will need to be changed to:

`page-break-before:auto;`

## Footnote References

In a printed book the footnotes are at the bottom of the page and the references in the text are usually a superscript number (slightly smaller in size and elevated next to the appropriate context.

[![Footnote references are superscript numbers](/images/2017/02/editing_ePub/image8.png)](/images/2017/02/editing_ePub/image8.png)

In our eBook version we can opt for the footnotes to become popup notes (supported in ePUB3 in Apple’s iBooks software and the recent Kindles. However, the little superscript number are very difficult to spot and even more difficult for the finger to touch, so I suggest making then stand out a bit more by adjusting the CSS to give a background colour and slight increase in size.

[![Here is the popup text showing a re-styled reference number](/images/2017/02/editing_ePub/image9.png)](/images/2017/02/editing_ePub/image9.png)

In the CSS we need to edit these lines to the rule for the reference element:

```css
span.reference {
 color:#cc071e;
 font-variant:normal;
 text-transform:none;
 vertical-align:super;
 font-size:1.6em;
 color:white;
 background:#cc071e;
 padding:3px;
 font-weight:bold;
}
```

## Typography

In our print book we have 2 columns in the introduction text and we have set this to be justified.

[![print version shows 2 coloumns](/images/2017/02/editing_ePub/image10.png)](/images/2017/02/editing_ePub/image10.png)

When this arrives in the ePUB (reflowable), we find only one column but the text is justified. Maybe we are happy with this, but if not we need to change the CSS in the body text rule from:

`text-align:justify;`

to

`text-align:left;`

If you delete the line altogether, the user will control the text alignment, in their eReader software settings.

If the intention is to go back to InDesign in this workflow / editorial cycle, then you should avoid editing anything other than the CSS. Your objective (wherever possible) is to avoid editing the XHTML pages. Once you edit any other files inside the ePUB package, then roundtrip to InDesign will be very difficult.

If your workflow requires that you edit the ePUB in order to consult the other members of your creative team or even a client, then you should copy and record the changes that you make so you can wind these changes back int a new version.[^2]

The other modifications that you may need to make are as follows.

## The OPF Package Document

If you exported from InDesign this file will be named `content.opf`

There are a number of adjustments that can be made to the OPF file that will affect the way that the ePUB is displayed. Some of these settings are particular for iBooks on iPad, but there are some settings that are generic and are needed for other devices and platforms.

## The Cover

You will find references to the cover in 3 places in the content.opf file.

```html
<meta name="cover" content="msnd_cover15.jpg" />
```

This is a line required only for backwards compatibility for ePUB2 and is not really need but leave this alone!

```html
<item id="cover" href="cover.xhtml" media-type="application/xhtml+xml">
```

In my case this is a separate page that can optionally display the cover. In other words, this refers to an XHTML page that includes a link to the image source. However, the item in the spine section that refers to this looks like this:

```html
<itemref idref="cover" linear="no">
```

and the `linear="no"` attribute means that this page will never show unless it is linked from elsewhere - for example - the table of contents.

So, if you would like your users to be able to navigate back to the cover, then you can remove `linear="no"`, so that the cover itself is part of the book flow, and can be seen as the first page in the book. Note: Do not do this if you intend to convert to the Kindle version, because you will then have the cover showing twice!

We are not done with the cover yet! There is another line required for the ePUB3 format and you will find this in the `<metadata>` section:

```html
<item id="msnd_cover15.jpg" href="image/msnd_cover15.jpg" media-type="image/jpeg" properties="cover-image" />
```

This we should leave alone!

## The Spine

The spine section of the `content.opf` file gives the reading order. This will have come from the order of the pages in InDesign or even the the Articles panels. Also, if (like me) you are using the book panel, the order of the InDesign files will affect this spine list.

You can modify this order; let’s say you have a colophon and you would rather have this in the back matter, then you can move the appropriate line to your choice in the sequence.

Here is my spine section:

```html
<spine toc='ncx'>
<itemref idref="cover" linear="no" />
<itemref idref="frontmatter" />
<itemref idref="dream_preface" />
<itemref idref="dream" />
<itemref idref="dream-1" />
<itemref idref="dream-2" />
<itemref idref="dream-3" />
<itemref idref="dream-4" />
<itemref idref="dream-5" />
<itemref idref="dream-6" />
</spine>
```

## The Guide Section

You will notice that under the spine items you will find the Guide section and this is only here for backwards compatibility.[^3]

The Guide Section of the package OPF file provides a similar function to the Landmarks section of the ePUB3 navigation document (see later), but harks back to the ePUB2 format.

There is some advantage to adding some items here if you plan to export to the Kindle/MOBI format for Amazon devices; especially if you wish to support earlier versions of these devices. Kindle software does have a drop down menu that can be populated with some items. Here is my Guide section built by InDesign on export:

```html
<guide>
 <reference type="cover" href="cover.xhtml" title="Cover" />
 <reference type="text" href="dream_preface.xhtml#_idContainer005" title="Beginning" />
</guide>
```

I want to add the Table of Contents in here because Amazon recommend that the TOC should display on the page; this is at odds with the ePUB3 format, where we would rather use the logical version in the eReader interface. So, how can we add an XHTML version of the TOC?

We have one already, because the ePUB3 export has given us - `toc.xhtml` - the Table of Contents that is perfectly formed to be displayable. So we use this. Add this line to the `<guide>` section to become:

```html
<guide>
 <reference type="TOC" href="toc.xhtml" title="Table of Contents" />
 <reference type="cover" href="cover.xhtml" title="Cover" />
 <reference type="text" href="dream_preface.xhtml#_idContainer005"   title="Beginning" />
</guide>
```
 This change will not effect the ePUB3, but is useful for the Kindle version.

## The Metadata Block

We can make some additions to the `<metadata>` section of the `content.opf` file. You should notice the following line if you opted to embed fonts when you exported to the ePUB:

```html
<meta property="ibooks:specified-fonts">true</meta>
```

InDesign has put this line into the `content.opf` file at the same time as encrypting the fonts that you chose in your paragraph styles. There could be a situation where you want to add this line in to the `<metadata>` block. This would be a situation where you are only targeting the Apple devices and you want to use some fonts that are present on the iPad/iOS devices[^1]. You don’t need to embed those fonts but you do need to switch on the ‘specified fonts’. So, if you plan to use the fonts that are available on the iOS systems, then do NOT tell InDesign to embed the fonts (when you export, but rather, add this line into the opf file.

### Let me offer an example.

So, let’s say that you decide to use avenir-next.

Build your ePUB with InDesign, with that font used in the paragraph styles.

When you export the ePUB, you can opt to NOT embed the fonts. Then, you will need to add the above line into the content.opf file.

But this line will only make a difference if the package item is included with all of the following:

```html
<package version="3.0" xmlns="http://www.idpf.org/2007/opf" unique-identifier="bookid" prefix="ibooks: http://vocabulary.itunes.apple.com/rdf/ibooks/vocabulary-extensions-1.0/" >
```

## Orientation and Spreads

If you expand the package section even more as follows:

```html
<package xmlns="http://www.idpf.org/2007/opf" unique-identifier="bookid" version="3.0" prefix="rendition: http://www.idpf.org/vocab/rendition/\# ibooks: http://vocabulary.itunes.apple.com/rdf/ibooks/vocabulary-extensions-1.0/">
```

We have added the extra prefix for rendition and this will also give you the potential to lock the orientation to landscape or portrait.

To lock the orientation on all iOS platforms we can use:

`<meta property="rendition:orientation">portrait</meta>`

To lock the orientation on a specific Apple device we can use

`<meta property="ibooks:iphone-orientation-lock">portrait-only</meta>`

## The Navigation Document (toc.xhtml)

InDesign CC will create the essential navigation document - toc.xhtml file ePUB3 as well as the ePUB2 equivalent - the toc.ncx file. This latter is provided for backwards compatibility.

All being well, your intelligent construction of the table of contents in InDesign, there should be no good reason to edit the TOC section of these files. Have a look at a sample section of the navigation section of the toc.xhtml file:

```xml
<nav id="toc" epub:type="toc">
<h2>Contents</h2>
<ol>
<li><a href="dream_preface.xhtml#_idParaDest-1">Shakespeare’s Life</a>
<ol>
<li><a href="dream_preface.xhtml#_idParaDest-2">Our Knowledge of Shakespeare</a></li>
<li><a href="dream_preface.xhtml#_idParaDest-3">Stratford</a></li>
<li><a href="dream_preface.xhtml#_idParaDest-4">Birth and Parentage</a></li>
<li><a href="dream_preface.xhtml#_idParaDest-5">Education</a></li>
<li><a href="dream_preface.xhtml#_idParaDest-6">Marriage</a></li>
<li><a href="dream_preface.xhtml#_idParaDest-7">Early Life in London</a></li>
</ol>
</li>
<li><a href="dream.xhtml#_idParaDest-8">Dramatis Personae</a></li>
<li><a href="dream-1.xhtml#_idParaDest-9">Act I</a>
<ol>
<li><a href="dream-1.xhtml#_idParaDest-10">Scene I</a>
<ol>
<li><a href="dream-1.xhtml#_idParaDest-11">Athens. The palace of Theseus</a></li>
……………… and so on ………
</nav>
```

This is a perfectly formed set of nested list items that can be viewed as a web page.

[![Here is what the `toc.xhtml` page looks like if I open in a web browser](/images/2017/02/editing_ePub/image11.png)](/images/2017/02/editing_ePub/image11.png)

In the image here you will notice another section called the Landmarks.

## Landmarks

Landmarks are a feature introduced with the ePUB3 format, and are provided so that eReader software can give the user a means to navigate to particular sections of the eBook. The ePUB format is ready to accept a number of `epub:type` values that can be addressed by the eReader software and will enable further navigation aids for the reader.

In later versions of InDesign you are likely to find this section on Landmarks is provided within your `toc.xhtml` file when you have selected the ePUB3 format on export.

In my first export to the ePUB, InDesign has given me 2 landmarks entries. Here is why:

The ‘Cover’ entry is there because InDesign has constructed a cover.xhtml file and this is normally not in the reading order of the spine (see the paragraph on The Spine in the section on The OPF Package Document). In eReader software that supports this feature, users can locate the cover from a menu.

The second item (Title-Page) is slightly more complex, and you will need to refer to the work we did in InDesign on our title page. Here is what this looks like in InDesign with the Object Export Options panel open:

As you see here the epub:type is set to title page and this is what provides the item in Landmarks section.

> **Note:** This may look different if you have an earlier version of InDesign.

The Landmarks section may include ‘cover’, ‘titlepage’, ‘bibliography’ etc. Here is an example:

[![This is where we select the epub:type](/images/2017/02/editing_ePub/image12.png)](/images/2017/02/editing_ePub/image12.png)

```xml
<nav epub:type="landmarks">
 <ol>
  <li><a href="cover.xhtml" epub:type="cover">Cover</a></li>
  <li><a href="titlepage.xhtml" epub:type="titlepage">Title Page</a></li>
  <li><a href="introduction.xhtml" epub:type="bodymatter">Introduction</a></li>
 </ol>
</nav>
```

This mark-up can be be added to the toc.xhtml file or you might prefer to set this up in InDesign by setting the Object Export Options for particular text frames.

## How can the Landmarks help in the way the eBook is read?

The way that the eReader software uses the Landmarks does vary. Some software does not make use of these items at all. For iBooks on Apple devices we can be very specific:

When you distribute the eBook through the Apple iBookstore, Apple will generate a preview of your book. This preview will be constructed from information in the landmarks section.

If you add the following to one of the items in the Landmarks section, the eBook will open on that page:

`epub:type="ibooks:reader-start-page"`

This is from the specific iBooks vocabulary and will only make a difference on Apple devices if you add the following attribute to the HTML tag at the top of the toc.xhtml page:

```html
<html xmlns="http://www.w3.org/1999/xhtml" xmlns:epub="http://www.idpf.org/2007/ops" epub:prefix="ibooks: http://vocabulary.itunes.apple.com/rdf/ibooks/vocabulary-extensions-1.0/">
```

Getting the page to start at a particular location is very difficult to test for because the eReader software (in this case iBooks on Apple devices), will remember your last location in the eBook, so you can only be certain by putting a fresh copy of the ePUB on to your device.

Generally though, one specific item needs to be positioned correctly, with the correct `epub:type` so that it becomes the first page that the user sees on opening their eBook.

Probably the most contentious issue here is the cover. The ePUB3 standard seems to presume that you don’t want your readers to see the cover as the first page. I can see the logic here, but if you do want the book to open initially at the cover, then you will need to follow the next paragraph on including the cover page in the flow within the spine section.

## Pages Outside the Flow

A more significant controller of your page ordering is the Spine section, where you are likely to find the following:

```xml
<itemref idref="cover" linear="no" />
```

This means that your cover is not available to your readers other than as a view in the Table of Contents (when in landscape mode on the iPad), or if you have linked in your logical table of contents.

You can rectify this by using:

`<itemref idref="cover" linear="yes" />`

Users can then navigate to the cover by turning back from your title page.

## Non-Linear Content

The concept of non-linear content is really important, because it means that you can have pages that will not be found by turning the page, but only through a hyperlink. For example, if you want a References page in your eBook, but you don’t want this page located at the end of the book (viewed by swiping through to that page), then you could edit your toc.xhtml file to include:

```html
<li><a href="references.xhtml">References</a></li>
```

But then in the spine use:

```xml
<itemref idref="references" linear="no" />
```

To prevent the page from being in the flow of pages.

## Displaying the Table of Contents as a Page

InDesign has been great at building the table of contents for us on export. We opted to keep this TOC off the pages, because we unchecked this page in the Articles panel.

Indesign created an HTML page for the ePUB3 version and this is used as the logical TOC.

But suppose you want to display this in your eBook with some further enhancements?

As you have seen earlier in this chapter, the `toc.xhtml` page is a page built with ordered lists, so we should be able to make it look better with some CSS.

We can add some CSS into the head tag of this page.

So I will just go ahead and add that to the `toc.xhtml` file.

Now I need to add this to the Spine section of the content.opf file:

```xml
<itemref idref="toc" />
```

You can see the image of the new page here on the left.

[![Here is the new page for the toc](/images/2017/02/editing_ePub/image13.png)](/images/2017/02/editing_ePub/image13.png)

I have also hidden the Landmarks section of this navigation document by using this CSS:

```css
nav#landmarks {display:none;}
```

## Adding Javascript

It is possible to use javascript to your ePUB3 package, for special purposes although this has limited support on devices and eReader software.

The example I am using here will solve a common problem when going from InDesign to ePUB - Balancing Ragged Lines.

In your paragraph styles, under Indents and Spacing, you may have switched on ‘Balance Ragged Lines’. This will be ignored on export to ePUB3 (reflowable), but we can use jquery and some code from Adobe (*blogs.adobe.com/webplatform/2013/01/30/balancing-text-for-better-readability/*).

We will need to add a class name to the item that we wish to apply this to, so in InDesign for the heading style - be sure to add this to the Export Tagging panel:

[![Adding a second class name ](/images/2017/02/editing_ePub/image14.png)](/images/2017/02/editing_ePub/image14.png)

You will notice that we have 2 class names. This is perfectly correct.

Now we need to add to our own CSS file the following:

```css
h2.balance-text {
text-wrap: balanced;
}
```

Then we add the following javascript files at the time we export the ePUB3:

`jquery-1.6.2.min.js`

`jquery.balancetext.min.js`

## Adding Content with Javascript

jQuery also gives us an easy way to add content to pages.[^4]

For example, suppose we want to take a heading and the first paragraph that follows it, and wrap this in a <div> so that we can apply a style to the whole block. We can create a javascript file that includes the following:

```javascript
$(document).ready(function(){
 $(".subhead").each(function() {
 $(this).next('p').andSelf().wrapAll('<div class="staytogether" />');
 });
});
```

We then add some style to the CSS like this:

```css
div.staytogether {
page-break-inside:avoid;
}
```

## Adding Content with CSS

CSS also has the potential for us to add some content at run-time.

In this example we are going to add a flourish before and after the scene name in the play.

The CSS we need is:

```css
.scene::before, .scene::after {
 font-family:ZapfDingbatsITC;
 content:'✣';
 font-weight:normal;
 font-size:1em;
 vertical-align:middle;
 color:#6bc77e;
 margin:0 10px;
}
```

[![Content added with CSS](/images/2017/02/editing_ePub/image15.png)](/images/2017/02/editing_ePub/image15.png)

## Summary

This chapter has shown you some of the edits you can make to the inner workings of the ePUB package.

Remember, if you want to ‘roundtrip’ back to InDesign then you will need to keep a record of these changes so that you can re-instate them, when InDesign overwrites your ePUB file. It is possible to add your own CSS at export time, but all other changes (to the package documents, toc.xhtml, landmarks etc.)- these will be lost at export time.

As time goes on, the export to ePUB3 feature of InDesign will no doubt improve, and so it may be that we will have more control over the output without having to make any edits inside the ePUB package.

Until that time — have fun!


[^1]: The fonts that are available on the iOS devices are listed here: *[iosfonts.com](http://iosfonts.com)*

[^2]: You might consider using a Git repository for this process so that you edits can be shared

[^3]: The guide section may be required when you convert this ePub to the MOBI format for the Kindle

[^4]: Some features of InDesign (such as animation) will automatically generate JavaScript inside the exported ePub. More on this topic when we explore the fixed-layout eBook.
