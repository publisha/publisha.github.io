---
layout: paper
title: How Shakespeare Helps me Teach Multi-Platform Publishing
date: 2018-06-26
images: full-width
published: false
annotate: true
version: [0.2]
Author: Chris Jennings
status: [just started]
comments: true
blurb: Using Shakespeare’s plays (content in the public domain) helps me, as the tutor for these students,  provide all the experience necessary to build wonderful publishable artefacts.
---

# How Shakespeare Helps me Teach Digital Publishing
**Using public domain texts and other resources**

**Author:** Chris Jennings

## Abstract
Masters students in the Oxford International Centre for Publishing  (OICP) at Oxford Brookes University get a chance to design and produce a book of one of Shakespeare’s plays and then further develop this as a web site and various eBook  formats.

Using Shakespeare’s plays (content in the public domain) helps me, as the tutor for these students,  provide all the experience necessary to build wonderful publishable artefacts. They can choose from any of Shakespeare’s plays apart from *A Midsummer Night’s Dream*; this is the play that I use to demonstrate the various assignments.

## Introduction
I have been teaching digital publishing at Oxford Brookes University since 1995, and, un-surprisingly, I have needed to change focus and digital tools many times. From CD-ROM to web, from Macromedia Director to InDesign— you know what I mean. We talked of SGML and Aldus Pagemaker, now we talk of POD (Print On Demand), ePub and XML.

Anyway, we are always re-inventing what we believe the students need to know.  My students are studying on an  MA Publishing programme and expect to move into the publishing industry. We listen to our `Industry Advisory Board` when they say that their new recruits need more knowledge of  digital technologies.

**Content is King (Lear)**

We have to work with something. We can’t expect our students to actually create the content (this is not what publishers do). And, in any case, we can’t wait for that to happen; we need something to work with that is available but is also challenging. We need content that can be enhanced with images and even multi-media.

**The Play’s the thing** [^1]

The typographic choices when setting a play are really quite interesting, and although there are conventions[^2] we still have a lot of flexibility.  A play includes many different elements which  all need to be styled appropriately. Moreover, there is a need to provide a structure to the form that helps the reader work through the flow of the text.

**Public Domain**

The text for all of Shakespeare’s plays are in the public domain. The texts have been converted to a digital form and can be found in various locations such as the Gutenberg project. Not only is the text available to us, there are many images that we can use to illustrate the plays.

## The structure of a play

Let’s go through the details of a Shakespeare play and consider the structure.

There will be some prelims such as the title page but thereafter we will need:

### Dramatis Personae

This is where the characters are listed. This is often presented as a list with the character name followed by their role. We are likely to consider the whole line as one entity and then the `role` inside this. It could be presented as a table. The facsimile (from where the public domain text has come from) may use `ditto` where the role is repeated. [we can look at examples]

The last line of the Dramatis Personae will announce the general location of the play.

### The Play

The structure may be simply several scenes inside an Act. Possibly 5 Acts with 3 or 4 scenes in each. Some plays have a prologue and even an epilogue. [check the range of structures]

The **Act** is the top level in the play structure. The title of this may be simply at the top of the first page or may even have a page (recto in print) dedicate to it. The number could be uppercase roman, Arabic or even a word. So we might depict as:

> Act IV, Act 4 or Act Four

The latter being most unusual.

The **Scenes**, likewise may be as:

> Scene III, Scene 3 or Scene Three

The conventions dictate the first of these in each case, but we are looking at the possible options and encourage new choices.

Each scene label is normally followed by a **location** for that scene.

#### Location

This is where the scene takes place and is an element in its own line. 

Now follows the first **stage direction**.

add the MindNode diagram here.

**To be or not to Be**

#### The character name

The words spoken in the play will be preceded by the name of the character and the method of displaying this is our first  structure and presentation conundrum.

To explain the issue we should look at how the character name is presented in print versions of the play, and we might look first at a page from the `first folio` of Shakespeare’s works. The image below shows the opening page of a _Midsummer Night’s Dream_

image here

You will notice that the character name is abbreviated. We don’t want our modern version to emulate this. Some public domain texts (from which we work) also abbreviate the character name. We will need to use `search/replace` to
change these. While we are here, we should observe also that the abbreviated character name is *on the same line* as the first line of the speech. More on this in a moment. We will want to have as much stylistic control of this character name as possible, so we should avoid capitalised letters; use title case. We can style as uppercase if we need, but, remember, if the digital text is using capital letters, then we cannot reverse this with a style setting.

In the image below is a modern version of *A Midsummer Nights’s Dream*.

image here of the Alexander edition

In this example, we see that the character name is generally above the first line of the speech, however the typesetter in this case has put the character name on same line _when the line is short_.

I suspect that this must be a legacy detail when the text was set with lead type.  We would find this detail difficult to style with a style rule. The reason for this relates to how we decide to structure the verse lines; are they to be separate paragraphs or will they be separated as lines within a paragraph? The speech block can be a paragraph with individual verse lines separated by a forced line break. If this is the case then the speech block can be styled as a block with space above and below.

We may prefer to keep each line in the speech block as a paragraph with a paragraph break at the end of each line.

Going back then to the structure and presentation of the character name, it will help us if this is a separate paragraph too,  and not attached to the first line of the speech.

> How would we achieve this?

#### Prose or Verse

Some of Shakespeare plays use mostly verse spoken by the characters, whereas others use mostly prose. What is the difference from a presentation perspective?

**Prose** flows across the page and breaks when it runs out of space. It should only break to the next line if the speech ends.
**Verse** is deliberately broken at the end of the line and the next line will start with an uppercase letter. Verse may break before the end of the verse line if there is no more space; this usually only happens when the line is long or the font size is large.

**Our text source**

We are most likely to be working from a public domain text that has been scanned from print and there will be some changes to be made if this is the way we receive our public domain text. Here follows some issues that we will need to resolve.

Scanned texts that are converted to digital text will have the presentation on paper reproduced in a digital form with lines breaking where the line breaks occur in the printed version. This means that we will need to remove these breaks otherwise we cannot guarantee that the text will flow properly and be responsive to different screen sizes. 

#### Line numbers

Some printed versions of the plays will include line numbers, usually ranged to the right of the line. There are some advantages to display the page number in an educational environment, because they can be a way to navigate to particular locations within the text as in `Act 2, Scene 3. line 45`. Not every line number is labelled, only every 10 lines typically.

> The public domain sources that we use for our projects do not include the line numbers and so we don’t incorporate them in our work. However, this may be considered in the future.

#### Stage directions

Usually the main stage directions will take a complete paragraph. These might indicate the entry on the the stage of one or more characters. When characters leave the stage then, again we might have a stage directions that will use the word `Exit` for a single and `Exeunt`as the plural form.

There are also directions within the text. An inline indicator such as `[Whispers]` or `[sings]` does not always appear on it’s own line, but rather within the line or immediately after the character  name.

## Analysis of the raw text source

One of the first tasks for the students is to look closely at the public domain text that has been provided. As mentioned above, this will have been converted (by scanning) from a printed text.

> We can use a text editor to make global changes to the text.  We can use `search and replace` or even pattern matching with `GREP` however, there is a good reason to leave this process until we have the text in **InDesign**.

Our objective is to markup the text and we can achieve this by using InDesign to attach styles and then match these styles to the equivalent tags. We can use the search and replace with `GREP` function in InDesign to achieve this but first we need to create the styles that will ‘wrap’ the elements in the play. Make the style names as if they are valid XML tag names and our work is easier because we can match by name.

## Marking up the structure

Before we consider how the text will be styled we use the understanding of the elements just described to add markup to the text.

### The DTD (Document Type Definition)

We can create a DTD that represents the rule set of the Shakespeare play. Let’s describe the rules for the play in English first:

* A number of Acts
* A number of scenes in each act
* One location in each scene
* a number of stage directions in each scene
* a number character names in each scene that can be repeated
* a number of verse lines that follow a character name
* or - a number of prose paragraphs that follow a character name
* or - a number of song likes that’s follow a character name
* an inline stage direction within a verse line or within a prose paragraph

> Add the dtd in here as code

## What use the DTD?

The reason we use a DTD is that we can import this into InDesign and it will automatically create all of the elements as `tags`.

> can we make those into style names auto? I can’t remember...



[^1]: **Hamlet**:
I'll have grounds
More relative than this—the play's the thing
Wherein I'll catch the conscience of the King

[^2]: See Book Typography: a designer’s manual, Mitchell and Wightman, 2005
The Chicago Manual of Style
