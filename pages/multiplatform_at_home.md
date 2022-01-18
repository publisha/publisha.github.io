---
layout: page
title: Final Assignment at Home
published: false
categories: ["HTML and CSS", "Multi-Platform Publishing", GitHub]
tags: [GitHub, HTML, CSS]
date:  2020-04-20 14:44
order: 2
images: full-width
blurb: We are using GitHub pages to host a web site for the Shakespeare play. This page explains everything to get working on this at home.
---

<!-- TOC depthFrom:2 depthTo:2 withLinks:1 updateOnSave:1 orderedList:0 -->
<section class='toc'>
## On this Page

- [How to work on your Shakespeare play web site at home.](#how-to-work-on-your-shakespeare-play-web-site-at-home)
- [You will need Atom software](#you-will-need-atom-software)
  - [For MAC users](#for-mac-users)
  - [For PC users](#for-pc-users)
  - [Getting your play repository on to your computer](#getting-your-play-repository-on-to-your-computer)
    - [Run Atom again.](#run-atom-again)
  - [Editing your play and adding images](#editing-your-play-and-adding-images)
    - [Getting the Images](#getting-the-images)
      - [How to unpack the ePUB](#how-to-unpack-the-epub)
    - [Putting the images into the project folder](#putting-the-images-into-the-project-folder)
    - [Adding Images to the play HTML5](#adding-images-to-the-play-html5)
  - [Styling the Images](#styling-the-images)
    - [The IMG tag](#the-img-tag)
  - [Pushing your changes up to your GitHub repository](#pushing-your-changes-up-to-your-github-repository)

</section><!-- /TOC -->

# How to work on your Shakespeare play web site at home.

These instructions help you work on your play web site at home. The idea is that you will add some content (images and video or audio) to the play web site to enhance it and make it more compelling.

# You will need Atom software

## For MAC users

If you have a MAC at home then you should be able to install as per the following instructions.

> **Note:** Even if you have already grabbed a copy of Atom previously I still recommend that you get a fresh updated copy as in these instructions.

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

**Note:** I have created a screencast on YouTube that goes through the process described above.

<iframe width="560" height="315" src="https://www.youtube.com/embed/Mb1DRhBOMWI?rel=0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## For PC users

If you have a PC at home running Microsoft Windows, you can install Atom from the Atom web site for free.

Here are the instructions for you.

To make this easier for you I have a settings file available here:
[www.publisha.org/resources/forwindows/atom.zip][7ccf54fe]

  [7ccf54fe]: http://www.publisha.org/resources/forwindows/atom.zip "Grab this zip file"

Once you have downloaded the configuration file from the link above you can then go to the Atom web site and download the application.

**How to install Atom on a PC and use for your GitHub site**

Go to [https://atom.io](https://atom.io) and install atom for your PC

If you have successfully dowloaded the configuration file above, you should see the toolbar along the bottom of the Atom window. If not, you _may_* install the packages yourself. Here are the instructions for doing that:

Locate the `Packages` menu and scroll down to `Settings View > Install packages/themes`

In the Install box for Packages you need to find the following and install them one at a time:

- tool-bar
- markdown-writer
- toolbar-markdown-writer

> **Please note:** The packages added above are only to help write markdown. If you are not using Atom to write blog posts then this will not be needed.

**Close Atom**

Leave Atom for the moment, now you need to install git from here:

[https://git-scm.com/download/win](https://git-scm.com/download/win)

You can choose the 64bit version if you have a recent PC otherwise choose the 32bit version but NOT the portable version.

Just go through the setup and choose the default settings as it goes through.

Then it will automatically run something called **git-bash**

You then need to type this first with your own email:
`git config --global user.email “9999999@brookes.ac.uk”`

_With the email you used on GitHub_

`git config --global user.name “Your Name”`

_This would be the username on GitHub_

**Now you should have Atom installed on your PC and we can now follow the instructions for both MAC and PC users.**

<hr />

## Getting your play repository on to your computer

Go to Github.com and sign in with your credentials.

Select the **play** repository and locate the button labelled `Clone or download`. Once you click this, you need to copy the URL (the button to the right of the URL field will copy this for you).


[![Use the icon to the right to copy this.](/images/clonewithhttps.png)](/images/clonewithhttps.png)


### Run Atom again.

**If you have a MAC** you will probably need to install the shell commands.

[![Install shell commands](/images/Screenshot 2020-04-22 16.01.15.png)](/images/Screenshot 2020-04-22 16.01.15.png)

If you have installed as per instructions you should see a set of icons at the bottom of the window. The icon at the far right end looks like this:

<i class="fab fa-git-alt fa-2x"></i>

Click this and a window appears. Paste into the top box.

[![Here is the clone window. Paste into the top box. You can move the repository later.](/images/clonerepo.png)](/images/clonerepo.png)

**If you have a PC** you may not have this icon so you will need to:

Locate Packages > Command palette > Toggle

You now can type into the box `GitHub:Clone`

Paste into here the link above and Clone onto your PC.

**Note:** I have created a screencast on YouTube that goes through the process described above.

<div class="video-box">
<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/GSlEFCqLYmA?rel=0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>


<hr />

## Editing your play and adding images

Once you have everything running on your computer at home, you should be able to take the next steps to fulfil the assignment brief which is to:

- Please edit the HTML and CSS to include the following:
  - Add the images that you have used in the re-flowable eBook (note you are welcome to use different images if you like or even add more)
  - You need to add a minimum of 12 images to the HTML
  - Add at least one video to the HTML (this may be a direct addition of an mp4 file or an embed from YouTube)

### Getting the Images

You can use the same images that you previously added to your re-flowable eBook (or you can source new or different ones). To get the images used before you can grab them from your assets in the InDesign project that should have been kept on Google drive. If you cannot get access to those files, then you can unpack the ePub file that you submitted and extract the images from there.

#### How to unpack the ePUB

An ePub is actually a compressed ZIP file by another name, so there are various ways to unpack:

Get this application (eCanCrusher) from here:

[eCanCrusher for MAC](https://www.rorohiko.com/downloads/eCanCrusherMac.1.2.1.zip)

[eCanCrusher for PC](https://www.rorohiko.com/downloads/eCanCrusherWin.1.2.0.zip)

Or just rename the ePub file by editing `.epub` to `.zip` then use an extractor program. This will already be available on the MAC and on the PC you can download from here: https://www.winzip.com/

### Putting the images into the project folder

Within your Atom project panel you should see the `images`folder. You need to transfer the images that you intend to use into this folder.
‎
### Adding Images to the play HTML5

Once you have located a position within the long HTML of the play, you then need to add the following markup (changing the **filename** and **alt** tag accordingly):



```html
<img src="images/forestscene.jpg" alt="Picture of a forest with tall trees" />
```


You will need this at least 12 times choosing appropriate locations.

> Please Note: The images will need to be `JPG` or `PNG` - not Photoshop files.

**Note:** I have created a screencast on YouTube that goes through the process described above.

<div class="video-box">
<iframe width="560" height="315" src="https://www.youtube.com/embed/ARayXHh2oSQ?rel=0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

<hr />

## Styling the Images

Once you have added the HTML markup to the page for the play, you can now focus on modifying the CSS to take control of the way the images are displayed. Locate the local copy of the HTML file for the play and open this in your browser.

To be certain that you are editing the correct CSS file look in the head section of your play HTML to see where this file is located. Here is mine:

```html
<head>
<meta charset="utf-8" />
<title>A Midsummer Night's Dream</title>
<link href="css/play.css" rel="stylesheet" type="text/css" />
</head>
  ```
### The IMG tag

You should find a reference to the `IMG` tag within you existing CSS file. It may look like this:

```css
img {
  width:100%;
}
```

When you see these newly added images in the browser for your play, you may be happy as they are, but there are some things you may wish to consider in the way the images combine with the text. Here are some examples:

> The images are too tall.

If you have some images that are in portrait mode (taller than wide) then, have a width of 100% may make the images too tall. You can resolve this by changing the width to less than 100%, however you may want to differentiate between wide and tall images by adding a class name to the tall images like this:

```html
<img class="portrait" src="images/athens.jpg" alt="Map of Athens" />
```

Then in the CSS you can have:

```css
img.portrait {
width:60%;
display:block;
margin:12px auto;
}
```

This will make _those_ images only 60% wide and centred.

Look at the following YouTube video for other examples.

<div class="video-box">
<iframe width="560" height="315" src="https://www.youtube.com/embed/CNIuvybUnqY?rel=0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

<hr />


## Pushing your changes up to your GitHub repository

Although you may not have finished your work on this, it may be wise to push your changes up to GitHub.

In Atom, you need to invoke the GIT pane on the right by clicking Git. This will probably have a number in a bracket `Git(2)`

Here is an annotated image of the Atom screen:

[![The Atom Workspace](/images/atomworkspace.png)](/images/atomworkspace.png)

Remember to select `Stage All` and then put a message in the `Commit message` box. Then you can `Push` the changes.

Here is a YouTube screencast that demonstrate this.

<div class="video-box">
<iframe width="560" height="315" src="https://www.youtube.com/embed/ZPv5FOdFr0A?rel=0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

<hr />

In the next document we look at adding multimedia and some other ways to enhance the viewing of images.

[Read the next document][a3d8140e].

  [a3d8140e]: https://publisha.github.io/pages/multiplatform_at_home2/ "Adding Video and Audio"
