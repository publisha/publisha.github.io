---
layout: page
title: How to Build Your Web Site with GitHub Pages
published: true
images: full-width
tags: [Using GitHub]
screencast: [blogwithgithub]
categories: [Web, HTML]
date: 2019-11-29
blurb: GitHub provides a way to use a free web site. Here is a simple way to get started with a provided template that you can change later.
order: 4
---

<!-- TOC depthFrom:2 depthTo:2 withLinks:1 updateOnSave:1 orderedList:0 -->
<section class='toc'>
## On this Page

- [Getting the software required](#getting-the-software-required)
- [Setup Github](#setup-github1)
- [Getting a local copy](#getting-a-local-copy)
- [Adding and Editing Content](#adding-and-editing-content)
- [Adding images to a page](#adding-images-to-a-page)
- [Getting the new content up to the web](#getting-the-new-content-up-to-the-web)
- [Your first look at your new site](#your-first-look-at-your-new-site)
- [Adding to and Editing your site Online](#adding-to-and-editing-your-site-online)
- [How does all of this work?](#how-does-all-of-this-work)
- [Further reading](#further-reading)

</section><!-- /TOC -->

# How to Build Your Web Site with GitHub Pages

This document explains all of the steps to take when creating a static web site using the free hosting at Github.Pages. The site that we build can be a blog or just an information web site. We will use a template that styles the site making sure that it is responsive to different screen and device sizes.

You will learn how to set the site up and configure with your own branding. Further, more complex styling can be achieved, but for this we need to have some knowledge of HTML and CSS.

Writing to your blog involves using the `Markdown` language and this will then be automatically be converted to `HTML` for the web site. You can learn about `Markdown` by viewing the [Markdown Guide on the web][47a5cbc0]. There are many writing apps that use `Markdown` but we will use a free tool called _Atom_ that will give you the means to write and update your live web site.

  [47a5cbc0]: https://www.markdownguide.org "Take a look at this helpful site"

Note: [There is a PDF of this document available here][7f29443a].

  [7f29443a]: /resources/createyourownblog.pdf "Grab this PDF"

## Getting the software required

You will only need the application called _Atom_ and to help you get the correct settings I am [providing you with a distribution][61862e36] package as a `zip` file. This will create an `atom` folder which you need to place inside your `Home` folder.

[![To find your Home folder use the Go menu item.](/images/getintoyourhomefolder.png)](/images/getintoyourhomefolder.png)

From the Finder use `Go` to find your Home folder. Read the `readme.txt` file that comes inside this zip file.

[61862e36]: http://www.publisha.org/resources/atom.zip "Get this zip file and unpack"

[![It will help if you show the extensions for the files](/images/showfileextension.png)](/images/showfileextension.png)

> **Note:** If you use Safari as your browser then the zip file will unpack into your downloads folder.

### Installing Atom

1. In your Home folder (remember use `Go > Home`) create a new folder and name it `Applications` (note the capital **A**).
2. Drag the `Atom.app` into this Applications folder.
3. Drag the `for_home_folder.zip` file into the home folder
4. Double click this file to unpack - this creates a _hidden_ folder called `.atom` (**but you won't see it**).

> You can view hidden files by using `SHIFT-CMD full-stop` on the keyboard.

The `Atom` program comes ready built with the following packages that will help you write posts for your blog.

-   tool-bar
-   markdown-writer
-   toolbar-markdown-writer
-   zen (this will provide a distraction free interface)

Now that you have the software installed you can sign up for the free web site at github.

## Setup Github

### Create a free account on [Github.com][a260d92e][^1]

  [a260d92e]: https://github.com/ "Sign up for an account on GitHub"

Naming the account (**your username**) is important (although you can change later) because this will become part of your website URL.

> For example, if you name the account `MyLoveofBooks`then the web site will become `myloveofbooks.github.io`. Not all names will be available and yours may be rejected if it is already taken.

Please remember your username and password or keep somewhere safe.

Choose a **Free** account and go through the various steps although you can skip the questions about your interests. You will also need to verify your email address. Optionally you can edit your profile and add an avatar image.

### Signed in to GitHub

Once you are signed in to Github, go to the following URL:

[https://github.com/publisha/student_site/][fc1ed271]

  [fc1ed271]: https://github.com/publisha/student_site/ "Get this template"

[![Click the green button to grab the template](/images/templategrab.png)](/images/templategrab.png)

Use the template link to receive the repository in your own github account. Make sure that you choose the `Public` option. You will be asked to name the repository.

>**This is important**: You need to name the repository _username.github.io_ where _username_ is the name of your username _but in lowercase letters_.

[![Name the repository using lowercase letters but use the same as your GitHub owner name.](/images/nametherepo.png)](/images/nametherepo.png)

> You should now have a copy of the template web site in your github account.

This will be the URL of your site.

Although it is always possible to edit the files directly on the github site, there is a much better way!

## Getting a local copy

Select the repository just created and locate the button labelled `Clone or download`. Once you click this, you need to copy the URL (the button to the right of the URL field will copy this for you).

[![You need this link and so this will copy the link for you.](/images/copythelink.png)](/images/copythelink.png)

### Now open Atom

You should see a set of icons at the bottom of the window. The icon at the far right end looks like this:

<i class="fab fa-git-alt fa-2x"></i>

Click this and a window appears. Paste into the top box.

[![Here is the clone window. Paste into the top box. You can move the repository later.](/images/clonerepo.png)](/images/clonerepo.png)

**Note**: Before you finish setting up, you can move the complete web site folder out of the `github` folder to your `Creative Cloud` folder (do _not_ use Google Drive). That way, you can find it on any of the computers that you are signed into. If you are using your own computer then there is no need to move the site out of your own home>github folder.

Close the Atom window and locate the github folder inside your Home folder. Now drag the folder called yoursite.github.io to a location on your Creative Cloud folder.

### Configuring your site

Before you make your web site live and post new articles, you need to edit the configuration file with your own details. The file you must edit is:

`_config.yml`

[![Here is a view of the site open in Atom. Changes to be made to the config file first.](/images/configchanges.png)](/images/configchanges.png)

The file itself has comments so it should be self explanatory but here are the important changes that you must make:

### Site configuration

Please make these changes before using the student blog.

Configure as your own website in the file called `_config.yml`:

```yml
  baseurl: ''
  url: "https://username.github.io"
```

Change _username_ to the username you chose for GitHub. In other words, the url will be the repository name prefixed with `https://`

### Meta and Branding

Meta variables hold basic information about your site which will be used throughout the site and as meta properties for search engines, browsers, and the site's RSS feed.

Change these variables in `_config.yml`:

Variable             | Placeholder                         | Make Yours
---------------------|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------
url                  | https://yoursite.github.io          | Change this to your url
title                | My name or organisation             | Name of website will appear top left on your pages
description          | A website with blog posts and pages | Name of website will appear top left on your pages
avatar               | assets/img/face.jpg                 | This can be changed to your own picture optionally
favicon              | assets/favicon.ico                  | Change to reflect your brand
header_text          | Me and my blog                      | Yours to change
header_feature_image | /images/hhh.jpg                     | You should create a different image to replace the picture of Headington Hill Hall. This image needs to be no smaller than 1800 pixels wide.
footer_text          | Copyright 2019 My name              | Put your name or organisation in here  |   |

You can also add your social media links such as Instagram, Twitter, Facebook etc.

There are other settings in the `_config.yml` file such as the configuration of prose. This is used if you use prose.io to edit and post to your site (see the section ‘Step 7. Adding and Editing your site online).

You will need to edit the `siteurl` in the prose section of the `_config.yml` file.

You also need to edit the placeholder tags url in the file called `_mdwriter.cson`. This is at line 34 in that file. This will make it easier to select and re-use tags for your posts.
urlForTags: 'https://yoursite.github.io/tags.json


## Adding and Editing Content

Writing to your blog involves using the Markdown language and this will then be automatically be converted to HTML for the web site. You can learn about Markdown by viewing the Markdown Guide on the web. (see Further Reading).

There are many writing apps that use Markdown but we are using Atom with a user-friendly toolbar that makes structuring your content easy..

There are 2 types of pages in your site:

### Posts

You can post articles or blog posts and these will be dated so that they appear in date order, on the home page, the latest at the top.

Each post has it’s own page but the extract will appear on the home page.

The number of post extracts that appear on the home page can be configured in the `_config.yml` file (the default is 5 posts with a link to the previous 5 etc.)

The posts themselves are files that will automatically be generated inside the `_posts`folder.

### Pages

You can create other pages for special (non-dated) content and, as long as you save them inside the `pages` folder, they will automatically generate a menu item at the top right of your site.

Apart from the **About** page described below, you can also create any page that you like to add to your site and, thus, a menu item. Examples could be a CV, or a Project page, or even a gallery of your photos.

#### The About page

This is the one page ready for you to edit. This page needs to be edited to contain information about yourself or what you want this site to do!

Editing this page will be a good way for you to get used to the way to edit and create pages using `Markdown`.

If you want to create another page, you can duplicate the _About_ page so that you can see what the structure needs to be.

### Markdown

Markdown is a way to write for a web site that uses simple structure and markup that will then be converted to `HTML`. It is useful to understand how `Markdown` works, but actually, when we use **Atom** with the added package, the elements can be selected from a toolbar.

Here are some examples of what the Markdown syntax means.

```Markdown
  ## Heading level 2
  ### Heading level 3

  This is **bold** text.

  This is *italic* text
```

### `YAML` metadata

At the top of each page or post there will always need to be some metadata to control certain aspects of the page when it is converted to `HTML` and then included in your site. When you create a post with Atom, the metadata is added automatically, but you need to edit this/

This metadata is enclosed within the 2 groups of hyphens. Here is an example.

```YAML
    ---
    layout: post
 title: Here is a sample blog post 
    date: 2019-10-19
 published: true 
    header_feature_image: images/2019/07/tomatoes.jpg
 caption: "Juicy Tomatoes" 
    tags: 
      - Journalism 
      - Life 
      - Food
    ---
```
Notice that the `header_feature_image` does NOT have the leading slash.

>Some of this metadata is generated automatically when you create a new post (the date for example).

You will also need to edit this metadata to confirm that the post is ready to be published; change from `published:false` to `published:true`. When the page is set to `published:false` it won't appear on your live site.

#### Page image

We will describe how you can add images to your posts and pages later, but all content can also have a `header_feature_image` and this image will appear at the top of the page, with the post heading set against it. You will need to place this image into your `images` folder and then provide the link to it in your metadata.

> **Tip** you can drag images into the images folder (make sure that they do _not_ have spaces in the file name) and then `right-click` over the image and copy the path. Then paste and edit this path into the metadata for `header_feature_image: pathtoimage`.

## Adding images to a page

This is done through the image icon on the `markdown` toolbar at the bottom of the active Atom window. <i class="fas fa-image fa-2x"></i>

You will get a popup window and you need to select and image from somewhere on your system. Make sure to click the box `Copy to ...`

[![Pay careful attention to this box. You need to enter the title (ALT tag). This becomes the caption.](/images/addimage.png)](/images/addimage.png)

### Previewing your page

You can preview the appearance of your page by clicking the icon near to the bottom left. The icon appears like this: <i class="fab fa-markdown fa-2x"></i>

[![The preview opens in another tab](/images/preview.png)](/images/preview.png)

## Getting the new content up to the web

Atom interacts with your `github` site, so once you have made changes or added a post, you will need to open the `Git` pane (bottom right) and then notice the changed or added files up at the right. These are `Unstaged Changes`.

[![Here we see the changed files being pushed to the Github repository](/images/stagingandpushing.gif)](/images/stagingandpushing.gif)

>   Now click `Stage All` and these will move down to the `Staged Changes` pane. You need to write something in the commit box, so that the changes will have a meaning to you later. You can now `Push` these changes to Github but for the first time you will need to add your credentials (please tick the remember box so that you only do this for the first time).

[![We will need to use our GitHub credentials for the first time. Select remember so that you won't need to do this again on this computer.](/images/signingin.png)](/images/signingin.png)

## Your first look at your new site

Your site is available now at `username.github.io`. Change _username_ of course.

You should now be able to write blog posts and and add further pages. You can customise your site by changing the title, the main image and the avatar through the `_config` file.

[![Web site with changes](/images/postadded.png)](/images/postadded.png)

For further changes to the appearance you will need to make changes to the `CSS`. This is the subject of future advanced sessions.


## Adding to and Editing your site Online

Although we recommend using `Atom` as the way to write posts and edit your site (you certainly need to use it for editing the config file and changing the appearance of your site), you can optionally use an online tool from anywhere with an internet connection to post articles.

### Using Prose

Go to the web site [prose.io][fdc8fec9] and authorize with your GitHub credentials.

[fdc8fec9]: https://prose.io "Prose is an online editor"

You should now see your repository available.

[![Here you see your web site repository](/images/prosescreen1.png)](/images/prosescreen1.png)

Once you go into the repository, you can edit the posts or create new posts directly.

[![Here we see a post being entered into prose.](/images/prosescreen2.png)](/images/prosescreen2.png)

### Synchronising

Be aware that if you use `prose.io` to edit your site then your local copy (edited with Atom) will not be the same. If this is the case then you will need to find the `Fetch` link at the bottom right of the Atom window to **pull** the changes to your local space.

## How does all of this work?

### Github Pages

GitHub provides for free github pages. [You can read more about this here][d89d9da3]. Basically anyone can host web pages here but we are using a static site generation system called `Jekyll` which is also supported in GithUb pages.

  [d89d9da3]: https://pages.github.com "Go to the Github site for an explanation"

### Jekyll

This software operates your site, converting the `markdown` files into `HTML` when you _push_ your files up to the GitHub repository. The Jekyll site that you have created from the provided template includes all of the files necessary to build the live pages including the stylesheets (CSS) and some javascript. There is also a system of logic that builds the menus and pagination. This logic engine is called `Liquid` and [you can explore this further here][c324856c].

  [c324856c]: https://shopify.github.io/liquid/ "Go to the shopify site"

## Further reading

| Title                                                     	| Type of resource 	|                                 	|
|-----------------------------------------------------------	|------------------	|---------------------------------	|
| [Creating Blogs with Jekyll][68777208], Vikram Dhillon    	| Book             	| 2016, APRESS                    	|
| [Working with Static Sites][c0190ded], by Raymond Rinaldi 	| Book             	| 20 Mar 2017, O'Reilly Press     	|
| [The Atom Flight Manual][b2bb191a]                        	| web site         	| How to Use Atom in great detail 	|

  [68777208]: https://learning.oreilly.com/library/view/creating-blogs-with/9781484214640/ "see this book on O'Reilly Online"

  [c0190ded]: https://learning.oreilly.com/library/view/working-with-static/9781491960936/ "See this book on O'Reilly Online"

  [b2bb191a]: https://flight-manual.atom.io "Read this online"

[^1]: GitHub is a free code hosting platform for collaboration and version control. GitHub lets you (and others) work together on projects. We use GitHub pages to host our web site.
