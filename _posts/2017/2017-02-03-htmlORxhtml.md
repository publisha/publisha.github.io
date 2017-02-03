---
layout: "post"
title: "HTML, XHTML, HTML5 or XHTML5"
date: "2017-02-01 11:00"
published: true
categories: [HTML]
---
Goodness me there seem to be so many flavours of HTML. What does this all mean for eBook production and why should we care?

## So you thought it was just 'HTML'!

HTML5 is the newest version of HTML and is very 'loose' and forgiving. In fact when you create HTML5 markup you do not need to close the tags.

For example this is acceptable in HTML5:

 ```html
<h1>This is a heading
<p>This is a paragraph
```

eBooks made to ePub3 standard use HTML but the markup is very strict. In fact the markup should conform to `XML` standards and this means that the format is actually `XHTML5`.

For the above markup snippet to conform to `XHTML` (and thus ePub3) it would need to be:

```html
<h1>This is a heading</h1>
<p>This is a paragraph</p>
```

In order to validate XHTML you need to name the file with the XHTML extension; thus `recipe.xhtml`

There are also some very specific items that need to go at the head of an XHTML file. Here are the required items:

```
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<meta charset="UTF-8"/>
and so on
```

As you can see, although the doctype is `html`, the namespace (`xmlns`) is using the one from the World Wide Web consortium for `xhtml`.
