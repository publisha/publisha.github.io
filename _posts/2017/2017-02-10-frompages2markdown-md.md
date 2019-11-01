---
layout: post
title: "From Apple's Pages to Markdown"
date: "2017-02-10 11:40"
published: true
categories: [Conversion, Markdown]
---
I have a lot of documents authored with Apple's Pages. I wanted to convert these to markdown texts with the images (mostly screen grabs). The Pages file format is a proprietary format, and so we are dependent on the limited export features that the program itself provides. So how can we do this?

## Apple pages

I think _pages_ is a very nice word processor and I have been using for some time to build documents for my students, to either print out or convert to PDF for delivery on our Moodle pages.

[![Here is a sample from a Pages document.](/images/2017/02/pagessample.png)](/images/2017/02/pagessample.png)

But I don't want to print this type of material anymore. Beside, I need to update every year. Making version changes needs to happen more frequently, these documents really need to be delivered as web pages. Editing (and creating new pages) is better done with a markdown text editor.

## The workflow

_Pages_ is good at giving you options for export. You can export to PDF, Word, Plain text and ePub. But, you can't export to HTML or markdown.

The challenge then was to take the Pages document and recreate as markdown for use here on this site, so the pages can be easily maintained.

## Pandoc to the rescue

I just love this Pandoc. Thanks to [John Macfarlane][d0fed9b6], a Professor of Philosophy at the University of California, we can convert just about any document format to any other with this universal document converter.

  [d0fed9b6]: http://johnmacfarlane.net/ "Read about John MacFarlane"

You can read the [details here][a4c2389d].

  [a4c2389d]: http://pandoc.org "Take a look at the details"

Pandoc is great but it does **not** offer Apple's Pages as a source file format, so we need to use the Microsoft Word format as an interim. Here is what we do once we have Pandoc installed.

Export from pages to Word (make sure to use docx - the default)
Locate the file just exported in the finder and change directory to there.

```terminal
$ cd documents/myfles
$ pandoc --wrap=none --extract-media=images somefile.docx
 -o mynewfile.md
```
Here is an explanation of this terminal command:

 - first we change into the folder where our Word document has been saved
 - we now use pandoc with these parameters:
   - `wrap=none` tells pandoc to not wrap the text that it finds. In other words, allow the text to flow except where there are specific paragraph breaks
   - `extract-media=images` will pull the images out of the Word document and put them into a folder called images. This will be _inside_ a media folder that pandoc creates automatically.
   - then we have the input file followed by the output needed. The `.md` extension tells pandoc to create a markdown file.


Then we have a markdown file and then all of the images from the Word document, will be put into the images folder (inside a media folder). The images will be renamed _image1.png_, _image2.png_ etc (if they were originally png files) or _image1.jpg_ if they were originally JPEG files.

## The Markdown file
The markdown file will now need some editing. Here is what a portion looks like:

```markdown
Extracting XML from InDesign depends on a number of factors, but if we
successfully achieve our goal then we can be pleased that we have styled
all of our content and mapped these styles to our document structure.
<span id="_Toc1" class="anchor"></span>What is XML and why do we want
it?
```
The reason that we are not seeing markdown headings with `##` is because our pages document did not have named styles that could be converted. Not perfect, but we know that any span tag like this one is a heading, so we simply use a GREP search and replace like this:

```grep
<span id=".+?" class="anchor"></span>
```
Replaced with `## `

We can remove the table of contents.

More GREP search and replace, will then help to build the image links with the correct structure and image location.

The image links have a width and height set, so we can easily replace this too.

Finally, we need to add our ALT tag text for each image.
