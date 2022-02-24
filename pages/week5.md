---
layout: page
title: Week 5 Issues
published: true
categories: ["HTML and CSS", "Multi-Platform Publishing", GitHub]
tags: [GitHub, HTML, CSS]
date:  2022-02-24
order: 2
images: full-width
blurb: We are using GitHub pages to host a web site for the Shakespeare play. This page explains everything to get working on this at home.
---

# Week 5
## To do for the play:

* Fixed navigation hides the destination when clicking an item in the navigation.  We can - sort out with  *scroll-padding-top* on the `html` element.

```css
html {
scroll-padding-top: 45px;
}
```

* You can increase the value for the mobile version but:

Not good that clicking the links does not hide the menu - can only be sorted with javascript

[[How to do Javascript]]

* sort this out with simple javascript in the **head** tag of the play HTML 


```javascript
    <script>
      function hidemenu() {
        document.getElementById("toggle").checked = false;
      }
    </script>
```

Give the ul an ID and then:

```html
<ul id="menu" onclick="hidemenu()">
```


## For the home page

* Collect together the files in the **docs** folder - this is from the downloaded repository from GitHub
* open the **docs** folder in vscode
* add a hyperlink to the play file

```html
<p class="readplay"><a href="play4web.html">Read the play</a></p>
```

* ditto on the cover image

- - - -
## More on the play

* add a **back to top** with position fixed and > id on body

```html
<div class="backtotop">
<a title="go back to the top of the page" href="#play4web">&#x25B2;</a>
</div>

see the id on the body for your ow link
```


* add a **home** link to go back to the home page of the site
Put this as a `li` at the top of the navigation `ul`. Give it a class name of ‘home’ and then style this with auto right margin.

Here is what this should look like:

```html
 <li class="home"><a href="index.html">Home</a></li>
```


### Optional

* Add an audio clip

```html
<audio controls src="/media/act1scene1_clip01.mp3"></audio>
```

- - - -
## Making the site live
It is very important that you build your site from the home page  `index.html`  and the play and put these _inside_ the `docs` folder. The live site comes just from the `docs` folder at your GitHub repository

### Method 1 with vscode push to GitHub repository

* You must be working with the cloned version of the **docs** folder
* You must be signed in to your Github account
* You will see a number against the source control icon
* Add a commit message and hit the tick
* This should send the files up  although you may need to accept a few messages and GitHub credentials

### Method 2 by uploading to GitHub directly

* Sign in to your GitHub account
* Navigate to the **docs* folder
* Use Add file in the root for the `index.html`



* Move into the css folder and Add file in there
* Alternatively you can replace the **docs** folder altogether as long as this is working locally


#multiplatform
