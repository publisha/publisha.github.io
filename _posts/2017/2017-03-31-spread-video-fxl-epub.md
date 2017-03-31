---
layout: "post"
title: "Video across a 2 page spread"
date: "2017-03-31 23:30"
published: true
---
There is an issue when video in a fixed layout ePub spans across 2 pages. This situation arises when you have 2 page spreads and you are converting to landscape. What happens is the video only really plays one half, even though, at first the video appears to be available full width.

## There are really 2 videos (one on each half)

[![In iBooks, the video is split](/images/2017/03/videoover2_broke.png)](/images/2017/03/videoover2_broke.png)

When you export to the fixed-layout ePub from InDesign – and you choose the `Convert Spread to Landscape` option. The process takes the pair of pages and creates one XHTML file (in the ePub package) with a viewport dimension based on the overall width of 2 pages. But, it also creates a 2 divisions with a width obtained from the width of the page. Inside these `<div>`s, it puts a copy of the video; there are 2 videos on the ePub page.

## Can we fix?

Yes, but only by editing the XHTML inside the ePub package!

Before we go ahead and show those changes you are advised to keep the spread where the video sits very simple; remove page numbers and headers and any empty text boxes that are sitting around on those pages.

> Note: When you edit the XHTML inside the ePub package you will lose the ability to _round-trip_ to InDesign, so leave these changes to the last in your workflow.

## Why do we need to edit the XHTML?

Blame Adobe! When the ePub is exported to fixed-layout specifying `Convert Spread to Landscape` a single XHTML document is created for the pair of pages, however, a `<div>` for each page is created with _inline styling_ but **no** id or class name. This means we cannot target this with our own CSS.

## Here are the steps then.

- The spread where you have the video needs to be simplified; that is, get rid of page numbers, headers and even empty text frames. The reason for this, is that you will be editing the XHTML, and you want to keep this simple!
- You will need to unpack the ePub after you have exported.
- You now need to find the XHTML file that contains the video.
- You now need to make 2 changes to this file.

Look at this line:

```html
<meta name="viewport" content="width=792,height=594" />
```

Take a note of the width (yours may be different to mine). Now **change** the width on the first `<div>`, because this will have a width that is half of the width above; You see that this is an inline CSS - this is why we cannot change in our own CSS.

[![This shows the HTML where the video is displayed across 2 pages](/images/2017/03/editHTML2videos.png)](/images/2017/03/editHTML2videos.png)

Here is mine:

```html
<div style="position:absolute;
overflow:hidden;
left:0px;
top:0px;
-webkit-transform:translate(0.00px,0.00px);
-ms-transform:translate(0.00px,0.00px);
transform:translate(0.00px,0.00px);
width:396.00px;
height:594.00px">
```
The width should be changed from `396.00px` to `792px`

The next change is to hide the second `<div>`. Find the second block that also has a width set to half the overall viewport width and add (within the inline style):

```html
;display:none;
```

> Note: These changes will be reversed if you re-export from InDesign, so you should only do this at the end of your workflow or copy this code somewhere and paste back in at the end.
