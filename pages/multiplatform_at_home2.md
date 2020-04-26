---
layout: page
title: Final Assignment at Home - add Multimedia
published: false
categories: ["HTML and CSS", "Multi-Platform Publishing", GitHub]
tags: [GitHub, HTML, CSS]
date:  2019-10-08
order: 2
images: full-width
blurb: We are using GitHub pages to host a web site for the Shakespeare play. This page explains how to add vide and audio to the web page.
---

# Adding Multimedia to your Shakespeare play web site.

In this second document we explore the ways to add multimedia content to the Shakespeare play web page.

## Video

There are 2 ways to add video to the HTML and whichever of these 2 ways, you will also need to add some CSS to styles the way it is presented.

We will start with the easiest way even though this will have certain disadvantages.

### Embedding from Youtube

First of all you need to find an appropriate YouTube video that will make sense somewhere in your play. Go ahead and search YouTube for your play and see if you can locate an extract of a performance or even an explanation of the plot.

Once you have found something suitable, look for the `Share` link.

[![Find the Share link](/images/sharefromyoutube1.png)](/images/sharefromyoutube1.png)

Now what you need is the `Embed` option like this:

[![Share the embed](/images/shareyoutube2.png)](/images/shareyoutube2.png)

You will notice that you can, optionally start the video some way in thus removing any introductions or advertisements.

The copy button will take the code and put into your computer memory so that you can place into the HTML. Here is the example of the embed code:

```html
<iframe width="560" height="315" src="https://www.youtube.com/embed/XL2-MbVniR4?start=6" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
```

You can place this code into somewhere in your play `HTML`.

As you can see the `iframe` has a width and height set and this will cause some problems if you want to make sure that your site is responsive, because the size of the video will always be fixed. To get round this, we need to wrap the `iframe` code inside a `div` and then some CSS to control the size of the video.

The screencast at the end of this section will provide a detailed explanation of how to add the markup but here is the code that you need using the youtube example above.

#### The HTML markup

```html
<div class="video-box">
<iframe width="560" height="315" src="https://www.youtube.com/embed/XL2-MbVniR4?start=6" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>
```

#### The CSS

```css
.video-box {
	position: relative;
	padding-bottom: 56.25%;
	padding-top: 30px;
	height: 0;
	overflow: hidden;
	margin-bottom: 12px;
}

.video-box iframe {
	position: absolute;
	top: 0;
	left: 0;
	width: 100%;
	height: 100%;
}
```

So if you add this `CSS` to your own CSS file for the play, then the video will resize automatically for different window sizes.

### Adding Video by file

Another way to add video to your page is to link to an actual file (probably an `MP4`), but then you need to have access to the file.

#### How to get video to use on your web site.

It is possible to actually download some videos from YouTube, but to do this you will need to install software.

**If you have a MAC** you can download VIDL from here: [https://omz-software.com/vidl/][9ed64ce1]

  [9ed64ce1]: https://omz-software.com/vidl/ "Grab vidl"

It is straightforward and all you need is to grab the share link from YouTube.

For the Windows/PC you can try 4kdownload from here:  [https://www.4kdownload.com][64074bd1]

  [64074bd1]: https://www.4kdownload.com "Grab 4kdownload"

You may not be able to download any video, since it may be protected.

You may be able to find other videos for your play not on YouTube, however even the Folger Shakespeare library hosts their videos on YouTube, so the `embed` method may be preferable in any case.

#### Adding video code to HTML

So, how do we attach a video file to the HTML?

The `video` tag in HTML is similar to the `img` tag, so first of all you will need to add the video file itself to your project space. I suggest that you create a folder named _assets_ and put the mp4 file inside that folder. Read about the video tag on [w3 schools][932911ab].

  [932911ab]: https://www.w3schools.com/tags/tag_video.asp "w3Schools"

So here is a sample:

```html
<video width="320" height="240" controls>
	<source src="assets/msnd01.mp4" type="video/mp4">
	Your browser does not support the video tag.
</video>
```

If you compare to the information you may find elsewhere you will notice 2 things:
