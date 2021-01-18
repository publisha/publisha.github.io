---
layout: page
title: Using a Git Repository to host your Shakespeare Play Web Site
published: false
categories: ["HTML and CSS", "Multi-Platform Publishing", GitHub]
tags: [GitHub, HTML, CSS]
date:  2019-10-08
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

# Using a Git Repository to host your Shakespeare Play Web Site

We are using GitHub pages to host a web site for the Shakespeare play. This page explains what we are going to do to get started.

## You will need Atom software

> **Note: **Even if you have already grabbed a copy of Atom previously I still recommend that you get a fresh updated copy as in these instructions.

You will only need the application called _Atom_ and to help you get the correct settings I am [providing you with a distribution][61862e36] package as a `zip` file. This will create an `atom` folder which you need to place inside your `Home` folder.

[![To find your Home folder use the Go menu item.](/images/getintoyourhomefolder.png)](/images/getintoyourhomefolder.png)

From the Finder use `Go` to find your Home folder. Read the `readme.md` file that comes inside this zip file.

[61862e36]: http://www.publisha.org/resources/atom.zip "Get this zip file and unpack"

[![It will help if you show the extensions for the files](/images/showfileextension.png)](/images/showfileextension.png)

> **Note:** If you use Safari as your browser then the zip file will unpack into your downloads folder. **Now take the following steps**:

1. In your Home folder (remember use `Go > Home`) create a new folder and name it `Applications` (note the capital **A**).
2. Drag the `Atom.app` into this Applications folder.
3. Drag the `for_home_folder.zip` file into the home folder
4. Double click this file to unpack - this creates a _hidden_ folder called `.atom` (**but you won't see it**).

> You can view hidden files by using `SHIFT-CMD full-stop` on the keyboard.

## Now we need to create the Github repository

Here are the steps:

[Create a Github Account][8c08ca4b] (if you do not already have one) and login to the account.

If you already have an account then login at [github.com](https://github.com)

  [8c08ca4b]: https://github.com "Go to GitHub and create and account or login if you already have one"

Now go to this page (put this into the URL box): https://github.com/publisha/shakespeareplay

You will see the green button _Use this Template_

[![Click the green button to grab the template](/images/templategrab.png)](/images/templategrab.png)

Use the template link to receive the repository in your own github account. Make sure that you choose the `Public` option. You will be asked to name the repository.

- Go to **settings and change the name** of your repo (you should use the name of your play.

[![Change the name of your repo](/images/2017/01/changethenameofRepo.png)](/images/2017/01/changethenameofRepo.png)

## What's inside the repository?

When you download this repository, you will find a variety of files, but the 3 important ones are inside the **docs** folder:

- index.html - this will become the home page for your play. This page will have the cover image.
- play.html - this is where the text of the play will be. Linked from the home page above.
- styles.css -  this is where you define the styles for the elements in the play

You can also have a look at the sample scene inside the **sampleScene** folder.

## Ok, so what do I do now?
[You should now read the help document here][9bf3210c], that explains how to generate the HTML files from InDesign.

  [9bf3210c]: https://publisha.github.io/pages/InDesign_to_HTML/ "This gives you comprehensive information needed to build the HTML from InDesign."

### Here are the basic steps

- Open InDesign and find your final version of the play (**only the play - not the Introduction**)
- Make any corrections that you like (consider the comments from the previous assignment)
- If you created any new styles you will need to go to the style panel and configure the _Export Tags_ feature, making sure that each style will export with an HTML tag.
- As stated above - read the help document that I have provided - [InDesign to HTML][2aa24c4b].
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
- Click the Up Arrow
- Click Push

You should now be able to _push_ your updates direct to GitHub and see the results on your web site.

[![Push your changes to Github](/images/Screen Shot 2018-01-16 at 14.32.21.png)](/images/Screen Shot 2018-01-16 at 14.32.21.png)


## Back to GitHub

Now we need make the web site live at [github.com][448988fc]

  [448988fc]: https://www.github.com "Login at Github"

Go there in your browser and login with the credentials that you put in before and find the repository that you have previously renamed.

- Under GitHub Pages choose the **docs folder** for the source

[![You are telling GitHub to run the web site from the docs folder](/images/2017/01/choose_docsfolder.png)](/images/2017/01/choose_docsfolder.png)

- Your web page for the play will be live!
- When you have finished and are ready then post the URL of your site to the Moodle assignment location.

## Summary

Ok, so I know this seems complicated. Let me write out a simple list with the steps. Make this into a check list and tick them off as you go!

- [Download Atom][aea13298] and install in **your** Applications folder
- Create an account on [Github.com][fc57320f]
- Grab link on Moodle (week 1) for the GitHub template
- Copy the link next to the Clone button
- In Atom, use the icon bottom right to clone and use the window to paste in the link
- [Read the helper document about getting HTML from InDesign][f0f67b5c]
- Add the files into the local version of the repository and edit the HTML and CSS etc
- Check that the site works (home page is the cover image with link to the play)
- `push` the files to your GitHub repository
- Configure your GitHub repository to use the `docs` folder to deliver the web site
- Note the web address and finish

[fc57320f]: https://www.github.com "Create the account"
  [aea13298]: https://atom.io "Grab Atom"
  [f0f67b5c]: https://publisha.github.io/pages/InDesign_to_HTML/ "Read this"
