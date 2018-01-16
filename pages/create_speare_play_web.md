---
layout: page
title: Repository for Shakespeare Play Web page
published: true
categories: ["HTML and CSS", "Multi-Platform Publishing"]
tags: [Using GitHub]
date:  2018-01-16
order: 2
blurb: We are using GitHub pages to host a web site for the Shakespeare play. This page explains what we are going to do to get started.
---
<!-- TOC depthFrom:2 depthTo:2 withLinks:1 updateOnSave:1 orderedList:0 -->
<section class='toc'>
## On this Page
- [What to do?](#what-to-do)
- [Your digital tools](#your-digital-tools)
- [What's inside the repository?](#whats-inside-the-repository)
- [Ok, so what do I do now?](#ok-so-what-do-i-do-now)
- [The Play](#the-play)
- [The home page cover](#the-home-page-cover)
- [Making the web site work](#making-the-web-site-work)

</section><!-- /TOC -->

# The Repository for your Shakespeare Play Web page

We are using GitHub pages to host a web site for the Shakespeare play. This page explains what we are going to do to get started.

## What to do?
If you are reading this within your very own copy of this GitHub repository (because you followed the link from the **github classroom**), then read on. If you are reading this offline, then [please set up the Github account][8c08ca4b] before you do anything else.

  [8c08ca4b]: https://github.com "Go to GitHub and create and account or login if you already have one"

Before you do anything with your new GitHub account do this:

- Go to your account settings and put in your full name
- Add a picture or avatar of yourself

You will now need to click on the link in Moodle and accept the repository.

[![Accept the assignement from classroom](/images/Screen Shot 2018-01-16 at 14.15.41.png)](/images/Screen Shot 2018-01-16 at 14.15.41.png)

- Go to **settings and change the name** of your repo (you can use the name of your play, but this may conflict with others, so include your publisher or surname as well example: _blades-macbeth_)

[![Change the name of your repo](/images/2017/01/changethenameofRepo.png)](/images/2017/01/changethenameofRepo.png)

You don't need GitHub.com for the moment but you will need to recall your username and password during the next steps.

## Your digital tools
There are 2 free apps that you need to download and install.

### Atom
You will need a text editor that can show and preview HTML. We now want you to download and install _Atom_. You can find this [free open source editor here][9ef5b049]

  [9ef5b049]: https://atom.io "grab Atom"

[![Download Atom](/images/2017/01/downloadAtom.png)](/images/2017/01/downloadAtom.png)

This application will be placed inside your downloads folder, so you need to copy to your _Applications_ folder inside your user account on the MAC.

You can also install _Atom_ on your own computer at home.

[![Finding your Applications folder](/images/2017/01/yourHomefolder.png)](/images/2017/01/yourHomefolder.png)

Your Applications folder is inside your Home folder; find this by selecting _Go_ from the finder menu. You can copy or move the Atom app from the downloads folder.

If there is no Applications folder inside your home folder then create one. Do try to use the same MAC in the IT suite whenever possible, so that you do not need to install this software again.

Atom will now be available but we now need to move to the next stage.

> ### Configuring Atom
Atom is open source, so this means there are lots of packages that can be added to provide extra functionality.

> Here are a few packages that will prove useful but one that is highly recommended is:

> - Open in Browser

[![Add this package to Atom](/images/Screen Shot 2018-01-16 at 14.18.42.png)](/images/Screen Shot 2018-01-16 at 14.18.42.png)

> You can also use Atom to update your GitHub repository that is online, but to prevent having to login each time add the following command.

> In the terminal window copy and paste this:

> `git config --global credential.helper osxkeychain`

> You should now be able to _push_ your updates direct to GitHub and see the results on your web site.


[![Push your changes to Github](/images/Screen Shot 2018-01-16 at 14.32.21.png)](/images/Screen Shot 2018-01-16 at 14.32.21.png)

## Github Desktop_

You will need this app to make it easy to _clone_ the repository to your computer (use Google drive) so that you can edit offline/

_GitHub Desktop_ is free and [comes from here][c6de3c27]

  [c6de3c27]: https://desktop.github.com "grab GithUb Desktop"
One you download this app, put inside the Applications folder where you have placed _Atom_

- Open the GitHub Desktop APP
- Sign into your GitHub account that you have previously setup

Once you have done this you can now _clone_ the repository that is in your GitHub account online by selecting the **+** sign. All being well you should see something similar to this here:

[![You should see your repository once signed in](/images/Screen Shot 2018-01-16 at 14.25.58.png)](/images/Screen Shot 2018-01-16 at 14.25.58.png)

- You will be asked where to put it…. your Google drive is best! Stay in the GitHub desktop app:
- In the GitHub desktop right-click over the repo name in the left sidebar and select **Open in Atom**

[![Open in the repo in Atom for editing](/images/2017/01/openyourrepoinAtom.png)](/images/2017/01/openyourrepoinAtom.png)

- You should see something like this:

[![Atom editor](/images/2017/01/atom.png)](/images/2017/01/atom.png)

## What's inside the repository?
When you download this repository, you will find a variety of files, but the 2 important ones are inside the **docs** folder:

- index.html - this will become the home page for your play. This page will have the cover image.
- play.html - this is where the text of the play will be. Linked from the home page above.
- styles.css -  this is where you define the styles for the elements in the play

You can also have a look at the sample scene inside the **sampleScene** folder

- Also inside the resources folder you will find various InDesign scripts. These scripts needs to go into your copy of InDesign. The instructions are found in the readme for that folder.

## Ok, so what do I do now?
Here are the steps to take:

- Open InDesign and find your final version of the play (**only the play - not the Introduction**)
- Make any corrections that you like (consider the comments from the previous assignment)
- If you created any new styles you will need to go to the style panel and configure the _Export Tags_ feature, making sure that each style will export with an HTML tag.

[![The Export tagging panel in the paragraph styles](/images/2017/01/export_tagging.png)](/images/2017/01/export_tagging.png)

- You can read the help document that I have provided - [InDesign to HTML][2aa24c4b].
- Follow those instructions to create the interactive table of contents.
- Export your play InDesign document with settings in the instructions.
- You will find that you have now got a new file saved wherever your InDesign file was saved. You can drag this file into the `docs` folder of your working copy of the repo that you have open in Atom. This file should be renamed `play.html` and will replace the existing placeholder file.

  [2aa24c4b]: /pages/InDesign_to_HTML/ "read this for a thorough explanation"

> **Note:** if you included images in your play, you will need more work to get those into the appropriate location.

## The Play

In Atom it will look similar to this:

[![HTML version of the play](/images/2017/01/yourexportedplay.png)](/images/2017/01/yourexportedplay.png)

- Open the _play.html_ file that is inside the docs folder (that you have from your repository) with **Atom**
- Now edit the _style.css_ file (again inside the docs folder) to style each of the elements in the play
- Review in a web browser
- Validate the HTML file here: https://html5.validator.nu
- Validate the CSS file here: https://jigsaw.w3.org/css-validator/

## The home page cover
- You now need the cover image from the book.
- You can open the PDF of the cover in Photoshop and crop down to the front of the cover. In other words, remove the back and spine.
- The cover image needs to be 1400 pixels wide, because we need this later for the eBook.
- save this image as a JPEG in the **images** folder within the **docs** folder in your repository that you downloaded from GitHub.
- Now edit the index.html file and put the file name of the image where instructed in the markup. Also edit the ALT tag text.
- When you view this `index.html` file the image will be very large, so you must edit the styles.css file to change the width of the image.
- when viewed in a browser, this image will be a link to the play.
- check that the link functions correctly.

## Making the web site work
You can look at the web pages in the web browser by right clicking over the file and selecting _Open in Browser_. This will only work if you installed the Atom package (see above).

**When you are happy** with the look of these web pages then you can:
- Upload these new versions of these files to your GitHub repository
- You do this by using the Atom Git Tab (Packages > GitHub Toggle Git Tab).
- click Stage All (top right)
- write a message in the commit box (what did you change)
- Click commit
- Click to Up Arrow
- Click Push


- Under GitHub Pages choose the **docs folder** for the source

[![You are telling GitHub to run the web site from the docs folder](/images/2017/01/choose_docsfolder.png)](/images/2017/01/choose_docsfolder.png)

- Your web page for the play will be live!
- When you have finished and are ready then post the URL of your site to the moodle assignment location.
