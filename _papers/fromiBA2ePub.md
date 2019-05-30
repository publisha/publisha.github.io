---
layout: paper
title: From iBooks Author to ePub - A Case Study
date: 2019-05-29
images: full-width
published: false
annotate: true
version: [0.65]
Author: Chris Jennings
status: [early release]
comments: true
blurb: The
---

## A kind of report on the work for APGRD on their eBook products
 and looking towards future

# What is here?

This article explains various aspects of the tools used to convert the iBooks Author version of the APGRD project: _Medea, A performance History_. This was finally published on the Apple book store in May 2016.

It was a requirement that a more easily accessible version was created using the ePub3 standard. This documents the process.

# Theoretical Considerations
iBooks Author (from Apple) is a wonderful piece of software for creating eBooks with lots of marvellous interactive features.

There are some very good reasons for using this software to add rich multimedia and interactivity to educational content.

 + It's free. Apple provide this software as a download from their web site and it runs perfectly well on most recent MACs under MacOS.
 + It is (fairly) easy to learn, and, there are several books and online resources (some free eBooks as well) available to help learn.
 + Proofing, transferring and distribution can all be done from within the software itself.
 + There are lots of templates for the beginner to use, to easily get started.
 + iBooks Author can be used by an author or editor to construct a prototype, that can then be further developed and enhanced.

## The disadvantages to using iBooks Author

 + The product that is exported from iBooks Author (.iBook) can only be viewed with an Apple device (MacOS or iOS)
 + By default, the eBooks produced can only be sold through Apple's own iBookstore although they can be **freely** distributed by other means.
 + The content cannot be exported in any form other than the raw text and PDF.
 + Although the content can also be exported as PDF, this is not at print resolution.
 + Although there is an ePub template available, this is only in the reflowable form.
 + You cannot open an existing ePub file for editing.
 + Using iBooks Author to create eBooks from existing print focussed digital assets is very difficult but, with some effort, possible (see the third section).

The main disadvantage is that there will be a large potential audience (particularly in the education sector) who will not be able to benefit from the iBook created with iBooks Author since they do not own MACs or iPads. This is a shame, because it is perfectly possible to create an eBook with very similar qualities that will perform well on 'non-Apple' devices, such as a PC under Microsoft Windows, some tablet devices _as well as_ the MAC and iPad. This is known as the ePub format.

### What is ePub?

The first version of the ePub standard was released by the International Digital Publishing Forum (IDPF) in 2007. The IDPF is a consortium of organisations and individuals. The standard is open and anyone can create software that will read and display the ePub.

The specification was originally in use as version 2 (ePub2) and in this release books could **only** be reflowable with text not formatted as is for print but more like a web page; flowing to fit the size of the device or window.

In 2014 the ePub3 version was released and now includes the ability for content to arranged as 'fixed' or precise layout. This new format also can include 'overlays' to deliver javascript, multimedia and animation.

In the ePub3 format, we have 2 available modes; the re-flowable and the fixed-layout forms. They are different in the amount of display control that they leave to the user/reader. Within a re-flowable eBook, the user may change the font size, the typeface and (on some devices), display features such as leading, alignment, justification and hyphenation. On the other hand, the fixed-layout form removes any such flexibility, and the page designer can arrange text and image on each page and be sure that this is how it will remain. The fixed-layout form is the _friend to the graphic designer_; the re-flowable form provides _more accessibility for the user_.

So, in summary, the ePub can either be used to deliver *re-flowable* or *fixed-layout* content.

For the fixed-format, the ePub that we create _must_ be created to the ePub3 standard. Let's look at what an ePub file actually is.

#### HTML, XML and CSS
The ePub file is actually a package of files. Although an eBook is one file (example.ePub) it can be 'unpacked' by renaming as a zip (example.zip).

Each page in the eBook is an HTML file (actually **XHTML**). This is where the fixed-layout and re-flowable eBook diverge; in a re-flowable eBook, each chapter (or section) is a single HTML file. There are a number of other files inside the ePub package, but essentially, the ePub package is like a _web site in a box_ with an interactive table of contents that provides navigation and a section of the content manifest that provides the reading order.

### How does this differ from the Apple iBooks format?
Apple's iBook (sometimes referred to as 'Multi-touch book') is similar to the ePub and is also a package of files wrapped-up in a ZIP file. The similarity ends there though, because there are many proprietary features that cannot be constructed in any way other than through Apple's iBooks Author.

### Can we make a more broadly available ePub version from the original Apple iBooks Author construct?
There is not a simple answer to this, but in the next section we will describe how we built the ePub version from the original iBook.

# Practical Considerations

For the APGRD project it was decided that using iBooks Author offered the easiest way to overcome the main objectives; building an interactive information resource from diverse types of assets in the archive.

The benefits and limitations of this software were soon understood by the project team, and it was perfectly possible to use the tool as a means to communicate the various options as the items in the archive were digitised.

### The Multi-touch iBook for Apple
After various iterations this version was completed and delivered to the Apple book store and users were able to download for their Apple devices.

There was no intention to create an iBooks version with a 'scrolling' view to give users the ability to change font size.[^7c5496db]

[^7c5496db]: This would have meant keeping the text in a continuous stream (more on this in section 3).

Since it was always in the plan to build a more accessible version for use on non-Apple devices, a strategy was then developed to make this conversion from the final iBook built with iBooks Author.

### From iBooks to fixed-layout ePub

As explained above, there are **no** *export* options in iBooks Author that can provide easy conversion to the ePub format.

The iBooks Author application creates 2 file types:

 + the .iba or iBooks Author file; saved as the work is developed and can be loaded back to iBooks Author for further development.
 + the .ibook file is created when the eBook is exported from iBooks Author; this is the publishable file

This .ibooks file is considered to be the final (signed off) copy. The one that gets distributed. It is this file that needs to be used to extract the assets for the ePub version.

The .ibook file is a package (much like the ePub) and it is possible to extract the content from this package by unpacking the file.

### Technical and toolset Requirements
Before we go through the steps in the workflow, here is a description of the set up and software requirements:

#### Software
1. InDesign CC 2015 or beyond. This was the best version for creating a fixed-layout ePub3.
2. PhotoShop. For some image editing.
2. iBooks Author
3. ImageOptim. This can reduced the size of the graphic images files with control over the quality.
4. Sound Normaliser. This takes sound from all media and sets at the the same level.
5. Miro Video Converter. To convert various formats; audio and video.
6. BBedit. Preferred editor for changes to ePub components.

#### Hardware
2. A MAC with Two Monitors
We need to have iBooks open at the same time as InDesign so we need a lot of screen 'real estate' to be able to see the final version of the iBook as well as the InDesign pages and the assets folder.

#### Workflow
1. Unpack the .ibook file by renaming as .zip and using an archive extraction tool.
2. Drive through the files to locate the assets folder. This contains the images folder and the media folder amongst many other things:

![assets folder](images/2016/12/Screenshot 2016-12-13 09.24.46.png)

3. The images folder contains all images that are needed to build a new version but also the thumbnail images and various icons and interface graphics that the iBooks version uses. We can delete all thumbnails and icons. We can tidy this folder up by removing all unwanted images.
4. The media folder contains all audio and video files. We will need to convert the audio to .mp3 files and the video to .mp4 so that InDEsign can use these files.

**InDesign** now needs to be opened and a template created. The InDesign page size is based on the format for landscape iPad. For this project, 1024 x 768 pixels was chosen although future projects might now target the 'retina' version at 2048 x 1536 pixels. Styles to equate with those in the iBooks Author version were created, and fonts added to the author system as required.

**Body text changed for easier reading experience**. Feedback from the users of the published iBooks Author version suggested that a sans-serif font would be better so Avenir Next was chosen since this already exists on Apple iOS systems and can be embedded in the ePub version.

**Two Screens are better than one**. The best option for this kind of work is a 2 screen display, so that InDesign can be on the main display and the iBook version on the other. This helped in matching each page content.

**Text should flow**. One problem with the iBooks Author (from a conversion perspective) is that the text on each page was placed in separated boxes; the headings in one, then 2 or more for the body text and a further set for the captions. It was the intention in capturing this text that all text (apart from the captions) would be in one single flowing text. It was also determined for consistency to set a spacing styles for the headings so that the body text would always follow on at the same space. This spacing was a little bit random in the iBooks Author version.

**Master Pages and grid**. The master pages including page numbers and heading decoration (dagger!) was also set up for the template. There are several master page options:
![Master page options](images/2016/12/Screenshot 2016-12-13 10.04.03.png)
to be used throughout the chapter. Grid lines were used to set up the consistent positioning of elements on the page.

**An InDesign Book**. The chapters were kept as separate files and combined in the InDesign book panel.

## From iBooks Author to InDesign

### The text
The only way to get the text across was to copy and paste; with the two screen system described above the the text is copied within iBooks Author and then pasted into the text box on the equivalent page in InDesign.

### Text enlargement
Where there was the need for an enlarged block of text (translation or alternative version) then these were created as separate objects on a hidden layer and then revealed on click over a button.

### The glossary
It was not possible to get an equivalent feature to work in the ePUB version. I did experiment with various options, but popover text is not supported on most platforms so this was not pursued to a satisfactory conclusion.

### The images
The images that decorate the page (backgrounds, daggers, underlines) were collected in a devoted folder. For the single information images, they needed to be located in the assets folder and then placed in the InDesign page. The size of the images was always larger, since in iBooks Author images can be made to enlarge. Once the image was placed and reduced down, then a second copy was placed on another layer set up for the purpose. This second copy was enlarged to fit the complete page and attached to an object style that delivered a very large semi-transparent outline (to cover the whole page). The first (smaller) copy of the image was then made into an interactive button scripted to reveal the larger version. *Note*: This is a somewhat simplified description of the process.

### Image sequences.
iBooks Author has a 'Gallery' widget feature that allows a sequence of images to be constructed. These images are represented by thumbnails and can be enlarged individually and the sequence navigated full screen. There is no exact equivalent in InDesign, so the solution was the display the images larger on the page and construct a 'multi-state' object, with interaction on each image to move to the next in the sequence. Captions were added to the state for each image and displayed nearby.

### Audio
The MP3 files were placed on the page and then hidden behind images or text blocks. Graphic buttons were created for play and pause and these were then linked to the MP3 on that page.

### Video
The MP4 video was placed on the page and the poster image selected from one frame. Video can be played full screen as well as within the page. Many videos are delivered on a devoted page in the eBook, but there are some where 2 videos are on the same page; in this situation javascript had to be added to prevent the 2 videos being played at the same time.

### Special Features
There are some special features in the iBooks Author version that were built with Apple Keynote (this a great way to add animated sequences into iBooks Author); there is no direct equivalent for this in the ePub version but sequences were constructed as multi-state objects and then navigation was provides by adding buttons to the page.

### Table of Contents
The iBooks Author version uses a different structure for the table of contents with page thumbnails displayed at the bottom of the page as well as the drop down menu on the MAC version. The ePub uses a simpler approach with a single drop-down menu or a display of thumbnails for each page along the bottom on the MAC or over the whole screen on the iPad.

### The final file Size
The final edited version with embedded media and fonts was 439MB. By further compressing the images the file was reduced to 377MB. The iBooks Author version is 469MB.

## The ePub on different platforms
The finished ePub validates to the ePub3 standard and is tested to work well with Adobe Digital Editions version 4.5 and above. It also works well with the Readium plugin for the Google Chrome browser. Theoretically, the ePub3 should work with Google Playbooks, but the finished file is too large (377MB) for Playbooks which restricts the file size to 50MB.

Some experiments were conducted to build a version without video, this still did not get the file size down enough.

A version for the Kindle Fire was also attempted, but all of the javascript would have meant a complete rebuild.

# Limitations and the future
Building an ePub version from the iBooks Author version was always going to be a struggle, since Apple do not provide easy access to the file format, and there are only limited export features. The description provided in the previous section shows that 'copy-paste' was the only way the work towards a near equivalent version. The ePub version does behave differently when it comes to the interactivity, but otherwise all of the content is the same, with some limitations.

## The Limitations of the ePub3 version
The authors and editors (as predominantly academic writers) using iBooks Author found the Glossary feature very valuable as a way to explain certain words that may be unknown to the young reader. Getting the glossary to work in the ePub version was attempted, but eventually this option was removed from the ePub since the popups could not be made to go full screen. It is always possible to use the in-built feature of some eReader software, to give a popup on right-click over a word:


![ the in built dictionary](images/2016/12/Screenshot 2016-12-13 12.01.10.png)


## The future
### From InDesign to iBooks Author
I do believe that there is a better way to achieve both the iBooks Author version and the –more standards compliant– ePub3 version and that is to work in the opposite workflow direction and here are the steps:

1. Write the text using any preferred text system. It may be better, with multiple authors, to use an online versioning system like GitHub or BitBucket as a means to develop a system where texts can be 'signed-off' as approved for incorporation into the whole.
2. Simultaneous to this would be the digitising of images with metadata added to include the caption and copyright information.
3. Videos and audios will be sourced according to the notes made in the text above. These assets can be edited and held ready for delivery within the repository.
4. Once the text is approved it can then be placed into the template created in InDesign. Images can be placed, text-flowed and media components added and embedded.

This then forms the basis of the ePub3 version, although there will be more work needed to finalise this version. What we need now is to get this text (and images) into iBooks Author.

### XML / IDML
InDesign has an underlying data format called IDML (InDesign Markup Language). This is effectively XML by another name.

iBooks Author can import IDML files into a chapter. This then forms the basis of the iBooks Author version. The important point here is that although there is still more work to do in both versions (adding gallery widgets, multi-state objects etc), the main text is available in both.

## Accessibility could be better
The re-flowable ePub is a type that would be very difficult to use for this type of product, since images and text need to be kept in close proximity. This is a shame, because the re-flowable format does offer the user the ability to increase the size of the font for easier reading. This is not offered in the fixed-layout ePub. However, the iBooks Author toolset does offer a 'scrolling' view option that can be enabled _as long as the text is provided in a threaded stream_.

If the workflow method suggested above is used then the text will be threaded and the iBook can also have the scrollable view, selectable by the user and affording them the possibility to enlarge the text.

Chris Jennings @pageboy May 2019
