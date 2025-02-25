---
layout: paper
title: eEditing for multi-channel publishing
date: 2018-10-16
images: full-width
published: true
annotate: true
version: [0.8]
Author: Chris Jennings
status: [edited - 18.01.22]
comments: true
blurb: When content is edited in a browser and shared on a web server, there is a potential to convert this text and image in combination to a variety of formats. These formats can then be used in both print and digital product outputs.
---
<!-- TOC depthFrom:2 depthTo:2 withLinks:1 updateOnSave:1 orderedList:0 -->
<section class='toc'>
## On this Page

- [Introduction](#introduction)
- [Structure rather than Style](#structure-rather-than-style)
- [Markdown writing tools](#markdown-writing-tools)
- [Tools that make this easy](#tools-that-make-this-easy)
- [Working Files in the Cloud](#working-files-in-the-cloud)

</section><!-- /TOC -->

# eEditing for multi-channel publishing
**Browser based systems for editing books and output to multiple formats**

**Author:** Chris Jennings

## Introduction

The are are now several systems available that make use of web browsers (Google Chrome, Safari etc) to provide editing capability.  Maybe we have become used to  tools that provide wysiwyg text inputting for blogging platforms such as blogger.com or wordpress.  I will explore in this article editing systems where the content is actually stored (much like blogging content) on a remote server.

### Authors use word processors to write text

Although there are many word processing programs on the market, Microsoft Word is the most common and although the format is propriety, files can be converted and edited with other tools.  LibreOffice Office is a good alternative to Word and for Apple users there is Pages that can open Word files and export back to the Word format.

Entering and editing text in a web browser will rely on a friendly interface that provides a limited set of options for structure and style and these may be based on a browser plugin or use a `Markdown` toolset.

## Structure rather than Style

Since our objective is to provide documents that will eventually, serve multiple formats we want our text to be logically structured.

The problem of word processing software, is that it is too easy to select styling that only visually enhances the text but does not adhere to any structural conformance. A word processed document that looks good, may not lend itself to being the basis for formats such as HTML and ePub (also formed form HTML).

### What do we mean by Multi-channels?

This is best illustrated by this diagram of the different types of file that can be output from the same content.

[![ from editing in the cloud to multiple outputs](/images/eEdit forMulti-platform.png)](/images/eEdit forMulti-platform.png)

### What do we mean by structuring the text?

First of all we have the `blocks` of text; these can be paragraphs, headings, lists or blockquotes. Headings can have different levels that head up divisions and help guide the reader through the sections. The headings need to be nested properly; so a sub heading will follow a top level heading, not the other way around. Paragraphs  are the basic blocks of text and are usually all of the same, although we might define a different type of paragraph that follows a heading. Blockquotes are paragraphs that may be set differently; drawing attention to themselves.

Within the blocks of text we will sometimes need to draw a different emphasise with words in bold or italic. These inline elements will be `children` of their paragraphs. Although I refer here to **bold** and *italic* we should not concern ourselves with appearance or style, because this can be anything we like and applied later in the workflow to publish.

The important thing is the structure and because of this, we can utilise an editing system that is very simple; `Markdown` .

## Markdown writing tools

Some authors are using such tools as *Ulysses* or *Scrivener* to write their texts. At the heart of these tools is a standard way to structure (we come to styling later) the text.

I am using Markdown to write this text. Markdown simply uses hash codes  to indicate levels of heading. One hash is the top level # with ## and ### and so on being the following levels 2 and 3. A basic paragraph needs no markup particularly but does need to be separated with a break (2 returns will ensure this is separated).

Lists (bulleted or numbered) have special methods. A bulleted list is created by adding a `+` sign and space before the first item; thereafter a single break will continue the list. Numbered lists are similar but a number 1. a period and space will start the list.

Blockquotes  need a `>` at the start of the first line.

Inline elements can use either an asterix `*` or an underscore `_`.

If you need to display a block of code in a technical document, then a set of 3 backticks will start the and finish the block.

Here is an example of how this appears:

```markdown
# This is a heading
## This is a sub heading

A paragraph of text looks like this and simply continues **although** can have **bold** and *italic* text.

+ One
+ Two
+ Buckle my shoe

1. Item 1
2. Item 2
3. Item 3

> Mary had a little lamb
> Its fleece was white as snow

```

There are other codes that will be needed for embedding images or for making hyperlinks. Footnotes are also possible, but as you will see, there are apps and tools that make this much easier.

## Tools that make this easy

I am writing this on my **iPad** with an app called **Editorial**. I am expected to type the markdown codes but the app makes this easy by providing a set of buttons along the bottom of the screen. The text will also be displayed appropriately giving feedback and confirmation that the elements are correctly formed.

I show here an example of _Editorial_ in use.

[![Editorial, an app on the iPad](/images/IMG_0069.png)](/images/IMG_0069.png)

There are other apps,  that use markdown for both iOS and desktop computers.

[![Ulysses, a writing app](/images/IMG_0067.png)](/images/IMG_0067.png)

I should also give a big mention to `Atom` a free editor for desktop computers. Below you see a screenshot with the `markdown` on the left and a preview on the right.

[![Atom  a feee text and code editor](/images/Screenshot 2018-09-07 16.19.03.png)](/images/Screenshot 2018-09-07 16.19.03.png)

Atom is available from [atom.io][332bd3a3]

  [332bd3a3]: https://atom.io "you can download the software from here"

### Conversion to other formats

To publish our documents or to deliver to those that need proprietary formats (such as Microsoft Word), we will need to convert or export the texts.

Some apps will already include the ability to directly export to a variety of formats; Ulysses, for example, will export to `docx`, `PDF` and `ePub` as well as `HTML`.

**Markdown** is raw text and has no styling applied. It can be read by any human or interpreted by a computer program that will then tag the markup and make appropriate formatting conversions depending on the requirement of the target file type.

### Pandoc

Thanks to John Macfarlane, a Professor of Philosophy at the University of California, we can convert just about any document format to any other with this universal document converter.

Pandoc can be used in a `command line` mode. Here is an example that will convert a Word file to a Markdown document:

$ pandoc --wrap=none --extract-media=images somefile.docx
 -o mynewfile.md

 Since **Pandoc** can be utilised on a web server, it can also be used by online tools to form publishing options.

 [More about Pandoc here][852da9ef].

  [852da9ef]: http://pandoc.org "Go to the Pandoc web site"

 Let us now explore some online systems that can provide multi-format export after editing in the browser.  Many of these systems also provide collaborative editing.

## Working Files in the Cloud

In an article I wrote recently about version control, (link here)  I mentioned a few systems for collaborative editing and a significant development elaborated there was the use of `Git` as a repository for files. Here is not the place to go into details about Git, but the system offers great potential for editing and exporting documents in a variety of formats.

### GitBook

GitBook uses a repository held in GitHub as the source files. It is possible to use this collaboratively, but export can only be done from GitHub or some other method such Atom to convert the markdown into Word or ICML via Pandoc.

**GitBook**, as the name suggests is built to edit (also with *markdown*) a book under revision control within a Git repository. This goes beyond the prose.io instance described above, because the content can be exported as PDF or eBook. The management of the edits by multiple authors can be hard to resolve.

[![GitBook with an alert to the chief editor](/images/iterativePublishing.045.jpeg)](/images/iterativePublishing.045.jpeg)

> **Note:** GitBook has a new interface and looks different from this image.

### Prose

**Prose.io** is a server based *markdown* tool that can be used to edit text held in a GitHub repository. While this system is effective and very easy to uses, the prime focus is editing for a web site, rather than for other platforms. [^13]

[![Prose.io](/images/iterativePublishing.044.jpeg)](/images/iterativePublishing.044.jpeg)

You will notice from this screen image that `Prose` also includes a row of icons that make the process of entering *markdown* a lot easier for the user if they have little knowledge of the required markup. This set of icons leads us on to look at other input systems providing a more user friendly approach to browser based editing.

## Other text input systems

Not all systems use `Markdown` as the basis for text input and there are many plugins that web developers can use to build user text input systems. Popular products such as _TinyMCE_ and _CKEditor_ can be seen in use on many blogging systems. These systems can be customised to control a limited set of options for the authors and editors.

[![Here showing the CKEditor in use for a text entry field.](/images/ckeditor.png)](/images/ckeditor.png)

[Read more about the CKEditor here][227e8bf1].

  [227e8bf1]: https://ckeditor.com "The CKEdotor web site"

### Booktype

**Note: Booktype is no longer supported.**

BookType is OpenSource software that can be installed on your own web server or as a paid for service.

I have now built an editing system based on this software here: [booktype.publisha.org][e5abacf4]

  [e5abacf4]: booktype.publisha.org "You would need an invite to see this working"

Here it is in action.

[![Animated screen view of BookType.Publisha](/images/usingbooktype.gif)](/images/usingbooktype.gif)

You can see from the image below that there are a variety of formats available for export.

[![Booktype can export a number of formats](/images/Screenshot 2018-09-07 16.00.59.png)](/images/Screenshot 2018-09-07 16.00.59.png)

### Collaborative Editing

I have written [elsewhere][c42c03c9] about editing collaboratively in the article on Iterative Publishing, but it is important to point out the difference between the systems mentioned above.

  [c42c03c9]: https://publisha.github.io/papers/iterativepublishing/ "check this article"

In systems that use Git as the basic versioning engine (Prose, GitBook), each author/editor has ownership of **their own** version and when a commit is made the changes are then merged into the original or master copy. This means that editors can be working on the same document simultaneously.

With Booktype however, the document is effectively checked-out for the editor and cannot be edited by anyone else until those edits are saved. Changes are not part of the final document until the changes are accepted by the admin or chief editor.
