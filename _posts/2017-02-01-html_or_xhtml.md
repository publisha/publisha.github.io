---
layout: blog
published: false
categories:
  - HTML
---
## HTML, HTML5, XHTML or XHTML5
Oh gosh, what on earth does all this mean? You thought it was just _HTML_.

HTML5 is the newest version of HTML and is very 'loose' and forgiving. In fact when you create HTML5 markup you do not need to close tags.

For example this is acceptable in HTML5:

```
<h1>This is a heading
<p>This is a paragraph
```

eBooks or the ePub flavour use HTML but the markup is very strict. In fact the markup should conform to XML standards and this means that the markup format is actually XHTML5.

For the above markup to be conformant to XHTML (and thus ePub3) it must be:

```
<h1>This is a heading</h1>
<p>This is a paragraph</p>
```

## Validation

In order to validate XHTML you need to name the file with the XHTML extension; thus `recipe.xhtml`

There are also some very specific items that need to go at the head of an XHTML file. Here are the required items:

```
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<meta charset="UTF-8"/>
```

As you can see, although the doctype is html, the namespace (xmlns) is using the one from the World Wide Web consortium for xhtml.
