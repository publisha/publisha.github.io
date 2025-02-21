---
layout: page
title: InDesign to iBooks Author (Recipes edition)
published: false
tags: InDesign, "iBooks Author"
categories: [InDesign, "iBooks Author"]
screencast: [id2iba_recipeBook]
date: 2018-04-18
order: 5
blurb: An Authoring tool for an *Apple-only* hybrid format eBook. iBooks Author is Apple software for creating _Multi-Touch_ eBooks. We can take the content previously created with InDesign and import into iBooks Author from the IDML files.
---
<!-- TOC depthFrom:2 depthTo:2 withLinks:1 updateOnSave:1 orderedList:0 -->
<section class='toc'>
## On this Page

- [InDesign to iBooks Author (Recipes edition)](#indesign-to-ibooks-author-recipes-edition)
  - [The iBooks Format](#the-ibooks-format)
  - [The Authoring Environment](#the-authoring-environment)
    - [The Template](#the-template)
    - [Orientation Options](#orientation-options)
    - [The Styling Options](#the-styling-options)
  - [The iBooks Author Structure](#the-ibooks-author-structure)
  - [The Layouts](#the-layouts)
    - [Full Page Chapter Headings?](#full-page-chapter-headings)
    - [Layouts = Master Pages](#layouts--master-pages)
    - [Adding Layouts](#adding-layouts)
    - [Saving the Template](#saving-the-template)
  - [Typographic Style](#typographic-style)
  - [From InDesign to iBooks Author](#from-indesign-to-ibooks-author)
  - [From ePUB to iBooks Author](#from-epub-to-ibooks-author)
    - [Typographic Styles](#typographic-styles)
  - [Insert Chapter from InDesign (IDML)](#insert-chapter-from-indesign-idml)
    - [What is in the IDML File?](#what-is-in-the-idml-file)
    - [Chapter by chapter](#chapter-by-chapter)
    - [Export as IDML](#export-as-idml)
  - [Insert Chapter from IDML file](#insert-chapter-from-idml-file)
  - [Some broken features](#some-broken-features)
  - [Scroll Mode](#scroll-mode)
    - [What Is Portrait Orientation / scrolling view?](#what-is-portrait-orientation--scrolling-view)
    - [The Layouts in Scrolling View](#the-layouts-in-scrolling-view)
    - [The Typographic Styles](#the-typographic-styles)
    - [Images in the scrolling view](#images-in-the-scrolling-view)
    - [Decorative Images](#decorative-images)
    - [Content Images](#content-images)
  - [Further Details](#further-details)
    - [The Cover](#the-cover)
    - [Metadata](#metadata)
  - [Summary](#summary)
    - [InDesign &gt; ePub(reflowable) &gt; iBooks Author](#indesign--epubreflowable--ibooks-author)
    - [InDesign &gt; IDML &gt; iBooks Author &gt; Chapter](#indesign--idml--ibooks-author--chapter)

</section><!-- /TOC -->
# InDesign to iBooks Author (Recipes edition)

iBooks Author was released by Apple in 2012 and is an authoring tool that runs on any Apple computer that operates under MAC OS x 10.9 or later. The software is freely available and has gone through several version changes since first released.

eBooks created with iBooks Author (described by Apple as ‘multi-touch’ books) can only be experienced on Apple iOS devices (iPad) or MAC with iBooks eReader software. Apple’s licensing restrictions mean that it is only possible distribute through the Apple iBookstore or (for free) through your own web site.

## The iBooks Format

The eBook created with iBooks Author is a proprietary format that does have some resemblance to the ePUB3 format, although it is (virtually) impossible to edit the internal components.

## The Authoring Environment

Since our work has involved using InDesign to create eBooks, we will focus on taking content from InDesign and pushing it into the iBooks Author environment. First we must consider the approach that iBooks Author (IBA) takes to developing a design layout, because it is really very different from page layout tools like InDesign. Whereas InDesign expects a page size and proportion to be defined, with content then added and arranged, IBA uses a template system to define the layouts for typical components of the structure; the cover, the start page, the chapter start page, the section pages and so on. The template system also expects the designer to take control of the alternative portrait view of the book, because, the eBook created with IBA is a hybrid format; fixed-layout for the landscape view and reflowable for the portrait view.

[![Choose from one of the templates](/images/id2ibarecipes/image1.png)](/images/id2ibarecipes/image1.png)

### The Template

iBooks Author comes with many templates and, for many teachers and self publishers the options available are enough, but for us – we have to take control of the design by creating our own template.

There is no way to start a template from scratch. You have to start with one of the provided templates. It really makes sense to spend some time exploring the templates so that you can get a feeling for the way the structure of the iBooks Author environment works. As you will see from the list of templates there is one blank template, that you can use to build from but have a look through the others to get a sense of what id possible.

### Orientation Options

Make a decision first about the orientation that you will give your eBook. You can choose ‘Landscape’ or ‘Portrait’. It is possible to select the ‘Landscape’ option and then later turn on the scrolling view; effectively creating a Landscape with a portrait view.

If you are confused by this, you should experiment with a few of the template options, to get a better feel for the choices.

[![The style panel](/images/id2ibarecipes/image2.png)](/images/id2ibarecipes/image2.png)

### The Styling Options

Just like in any other design for publication toolset, there are 2 variables that you need to control; the layout and the typography.

The typography is controlled with a style palette and in iBooks Author this is known as the ‘style drawer’. Paragraph styles, character styles and list styles can be modified through the Text panel and the Fonts Panel. You can also create new styles by building those on the page and then, on selection, add as a new style.

Some of your decisions at this stage also depend on how you planning to get content into IBA. We are using InDesign, so we have already made some typographic choices. We will be able to use the paragraph and character styles. More on this later, first we need to deal with structure.

## The iBooks Author Structure

IBA provides you with a basic structure using the terms ‘Chapters’ and the further ‘child’ elements as the ‘Sections’. You don’t actually need to use these terms nor do you need to use Sections within Chapters. Indeed your book can be one ‘Chapter’ with many sections! You can even rename the Chapters and Sections so that Sections become Chapters and Chapters become sections.

Some books may have sections as the top level with chapters inside those sections. Anything is possible, although in terms of IBA’s automatic construction of the table of contents, you can only have 2 levels, so by default you have Pages within Sections within Chapters although you can dispense with Sections altogether.

[![The structure of an iBooks Author Document ](/images/id2ibarecipes/image3.png)](/images/id2ibarecipes/image3.png)

In my example book that that I have created for print we can look at the table of contents to try to establish the structure. We do only have 2 levels to work with but this should not be a serious limitation.

The TOC shows that the Heading ‘Introduction’ is at the same level as the Each recipe.

[![A sample table of contents](/images/id2ibarecipes/image4.png)](/images/id2ibarecipes/image4.png)

We need to equate these headings with the structural items of iBooks Author.

‘Introduction’ becomes Chapter 1. ‘Ingredients’ becomes the first Section inside Chapter 2 (Potato balls). ‘Moussaka’ will be Chapter 3 with 2 sections within this; Ingredients, and Method.

With this idea in mind we can construct a template that serves this structure. I am going to start iBooks Author and use the ‘blank template’.

## The Layouts

On the left hand side of the display window you will see the sample blank pages - a Chapter Heading page and beneath this (set in), a Section heading page. To see the layouts we need to expand the the collapsed window by dragging down the menu indicator to the right of the word ‘Book’.

Alternatively you can select ‘Show Layouts’ from the View Menu.

Be aware that we are looking at the thumbnail pages for the landscape view. We will also be looking at the portrait view pages in a moment.

### Full Page Chapter Headings?

Before we go ahead and look in detail at the layouts, we will need to consider whether or not to have a full page that announces the top level (ie the Chapter). In my example, I intend to do this, so that (for example), the recipe will have a full page (with an image). This image could be the same for every Chapter start, or I can replace this with a different one for each Chapter.

[![The layouts panel](/images/id2ibarecipes/image5.png)](/images/id2ibarecipes/image5.png)

### Layouts = Master Pages

With reference to the work we have done with InDesign, the Layouts are a bit like the master pages (but not exactly!).

There are are some elements on the Layout pages, that we can leave in’ The word ‘Chapter’ will automatically become the name of the Chapter heading.

For the first Chapter Page I remove the text field and add an image.

My second page will have 2 text fields and then I could add a header.

The Section start page includes the ‘Section 1’ header which I don’t want to keep. I can delete this.

My pages ‘2 column’ and ‘blank’ are available for me to modify further.

### Adding Layouts

Within each of the layout areas (Chapter, Section and Pages) I can add further layouts. So, say I want a title page, then I add this as a chapter layout by basing it on the selected layout. This then creates a copy of the Chapter layout.

I am naming this layout ‘Title Page’.

### Saving the Template

It is important that you save this as a template. Not a book.

We are not finished yet, but should now consider the styles of the typography.

## Typographic Style

You will see from the Style Drawer, that we have some basic styles for paragraphs, headings and characters. This how we received the styles within the ‘blank’ template.

We can modify these styles or create new ones, however in our workflow from InDesign, we don’t actually need to do this, because we can bring these styles from InDesign. However, we need to explore this important part of the process first; how can we get content from InDesign to iBooks Author?

## From InDesign to iBooks Author

Only in the most recent versions of iBooks Author have the following features been added. These features give us the possibility to get our content (styled and structured) within InDesign into iBooks Author. We must thank Apple for these additions, because prior to version 2.1 we could only copy and paste our content from InDesign and paste into iBooks Author (still an option, of course).

Neither of the 2 options described below are without their difficulties, and your decision as to which is better for you, will depend on the amount of work you would rather do in iBooks Author or back in InDesign.

## From ePUB to iBooks Author

>**Note**: I don’t recommend this method if you are working  from InDesign

In our sample project we have already created an ePUB(reflowable), and Apple have kindly added the feature for us to ‘Create New from an ePUB file …’. If you have a correctly structured reflowable ePUB3 with a working logical table of contents, then this will produce the most instant moderately successful iBooks Author file.

You will find this option on the File menu.

But before going through this process, let me just point out some facts.

The Table of Contents is where IBA gets its information for the structure – you know – Chapters, Sections, Pages etc. So, you really must be sure that the logical TOC, is going to provide that information. Take a look at your beautifully formed reflowable ePUB3 and analyse the TOC, before building the IBA file from it. iBooks Author only transfers 2 levels of the TOC to build the structure.

[![A template view for the ePub file import](/images/id2ibarecipes/image7.png)](/images/id2ibarecipes/image7.png)

### Typographic Styles

Creating a new iBooks Author file from an ePUB (reflowable) will bring into the template the correct appearance of the paragraph and character styles, but they will not have the names you gave them in InDesign. They will only have generic names such as heading 1, heading 2, etc. Furthermore, the many other styles that you have in your InDesign file (in my example: preamble, body text,sectionHeading etc), will all become **Free Form styles**. Now, this may not be a problem, but it will be impossible to modify these styles for the whole book.

## Insert Chapter from InDesign (IDML)

> This is the best method, but does require some preparation in InDesign to get robust IDML files

IDML is the published interchange format from Adobe that represents InDesign markup language. It is essentially an XML package that contains all the information to rebuild the assets, structure and layout for the whole document.

Using this technique is far from straightforward but if we are careful we can get good results that will also transfer all of the paragraph and character styles with correct labels. This is significant, because it means we can still **modify the styles globally** throughout the IBA document.

### What is in the IDML File?

Apple IBA will take everything that is in the IDML file and put it on its own pages. We expect the IDML file to include everything, but there is one thing that we do not want in the IBA file; the master page items. This means the header and the footers (page number especially).

Since the book you are reading proposes a workflow that retains the print elements and yet successfully produce eBooks, we will simply hide the master page items by putting them on their own layer and hiding that layer.

[![Hide some elemnts in InDesign by hiding the layer](/images/id2ibarecipes/image8.png)](/images/id2ibarecipes/image8.png)

### Chapter by chapter

IDML files can only be created from the individual InDesign files, not from the book panel. From within each document you will need to use the File &gt; Export and choose IDML.

In order for this work successfully, you really need to break the InDesign documents into their individual chapters and then export one IDML for each of those. The reason for this is that when you move back to iBooks Author, you are only able to insert one chapter at a time to get the correct structure. If you export one IDML file for the whole book (or section within the book), then it will become one chapter in IBA. If your workflow habits involve using the book panel and keeping chapters in individual files, then you are one step ahead of all the other eBook producers!

### Export as IDML

Since you have used the Book Panel then you can easily create all of the IDML files by packaging the book for print. We will now be ready to insert into the iBooks Author Template.

## Insert Chapter from IDML file

With our template open we now need to choose the first of our IDML files and after opting to include text, media and graphics, paragraph and character styles, we select the chapter, because we are entering the chapter in selectively for each.

[![Choosing the content to import](/images/id2ibarecipes/image9.png)](/images/id2ibarecipes/image9.png)

## Some broken features

We are going to experience some very strange anomalies with this process, and I am afraid you just need to accept that getting the content into iBooks Author this way does throw up some artefacts such as repeated pages, ghost text frames, that were not in the InDesign file and images that seem smaller than they were in InDesign.

The good thing is that you should not be missing anything, you just need to delete some pages and move top level heading to the Chapter start page.

To add a chapter (in our example so far this is a recipe), we just need the ‘Insert pages’ menu.

## Scroll Mode

If you want to give your users an option to read the book in a portrait mode (vertical orientation on the iPad) then you will need to look at the scroll view and make adjustments to a variety of places and settings.

Scroll View is an opt-out setting. You will find that in the Document inspector panel, the ‘Disable scrolling view’ tick box is off by default. You must tick this box if you have done nothing to style for the portrait view as well as the landscape view. We can only view the book in a portrait orientation with an iPad; you cannot see the portrait view with iBooks on the MAC, although you can see the portrait view in iBooks Author.

### What Is Portrait Orientation / scrolling view?

When you see a book in the vertical format on the iPad, the content can be scrolled through. There are are clear divisions at the Chapter level, but the Section levels will simply scroll through. The table of contents is all on one page with links through to all Chapters and Sections of the whole book, not just the individual chapters (this is quite different from the landscape view).

In the portrait view the users can increase the font size and for this reason it is a worthwhile extra step, to get this looking good.

[![Layouts in the scrolling viewing](/images/id2ibarecipes/image10.png)](/images/id2ibarecipes/image10.png)

### The Layouts in Scrolling View

You can open and edit the portrait layouts and the content pages by clicking the vertical icon in the toolbar. The view of this left hand panels changes to Book Outline, and you can see the Chapters and Sections listed but no image thumbnail. Each Chapter is one long scrolling page.

You will see the same layout labels; the Chapter and Section, but you don’t have much control over the actual layout, because you only have one text field that should fill with the text that is flowing in the landscape pages.

### The Typographic Styles

All of the styling will be carried across to the scrolling view, and this may not be too much of an issue except where you are using page decoration (as in my example), where the text is white against a background image. This can be resolved by unchecking the ‘Share color between orientations in the text style settings.

### Images in the scrolling view

There are 2 kinds of images in our eBook; content (images that subject matter or information relevant to the text) and decoration (images that serve to make the book more attractive. The latter are often in the background, or help inform the arrival of a new chapter or section. We need to look at both types.

### Decorative Images

We can only decorate the headers for the Chapter and Section start; unlike the landscape layouts where we can use the whole backgrounds.

[![Images can enlarge](/images/id2ibarecipes/image11.png)](/images/id2ibarecipes/image11.png)

### Content Images

[![The scrolling view thumbnails](/images/id2ibarecipes/image12.png)](/images/id2ibarecipes/image12.png)

You could have a shock when you view the Scrolling Pages, because you may not see any images at all. This is because images placed on the pages in the landscape view need to be turned into Widgets. This isn’t really as complicated as it sounds. With an image selected (in the landscape view), find the small widget icon and check the ‘Goes full-screen’ tick box. This will mean that the image in the landscape view can be enlarged, and in the portrait view it will become a thumbnail image in the left margin (Apple calls this the thumbnail track), also available for enlargement.

You can optionally add a caption and/or a title for the image. This will also then appear in the enlarged view.

We can also add images as thumbnails into the content

## Further Details

### The Cover

For a multi-touch eBook created with iBooks Author, the cover needs to be a very specific size. This is not the same as in ePUB (reflowable or fixed), where the cover can be any proportion that you like.

To place a cover in iBooks Author, select the Book icon in the left pane. This will show a box that will have the title of the book. You can, optionally construct the cover from text and a background image. I usually, create the cover as a graphic and drag it into this cover space.

The image needs to be in portrait orientation and sized precisely as:

1004 x 768 pixels

If it it has a greater resolution than 72dpi, then you will need to enlarge to fit.

[![Adding the cover](/images/id2ibarecipes/image14.png)](/images/id2ibarecipes/image14.png)

### Metadata

You will need to enter information about the book in the document inspector panel.

## Summary

We have looked at 2 methods to get content from InDesign to iBooks Author.

### InDesign &gt; ePub(reflowable) &gt; iBooks Author

This seems to work well with a cleverly formed table of contents. As long as you only expect 2 levels – Chapter &gt; Section, then this could be for you.

**Here are the issues**

The most significant difficulty is that all styles below Heading 1 and Heading 2 (in other words paragraphs) are not available as a style that can be edited; they will simply be provided as ‘Free Form’ styles.

### InDesign &gt; IDML &gt; iBooks Author &gt; Chapter

The results are reasonably good and anomalies are easily edited, since all named styles will correctly translate from InDesign.

**Here are the issues**

You really can only use this technique if you have split a complete InDesign document into constituent parts (such as chapters and sections), because you are only able to add the IDML file into a chapter not a complete book.

Fortunately, we have used the book panel to create our earlier eBook versions and so we can get the IDML files by creating a package for print from the book. This will create an IDML file for each chapter or recipe.
