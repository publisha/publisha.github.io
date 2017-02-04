---
layout: "post"
title: "Vertical Spacing for text; pBook and eBook"
date: "2017-02-04 22:50"
---
When we choose a value for _leading_ in InDesign, we are actually defining the distance between the baselines. The more traditional definition of leading is the space between the baseline and top of character container; the term coming from the little slabs of lead put between the type.

## Baseline Grid or Doing the maths?
InDesign has a super useful feature in paragraph styles; *Align to Grid*.
If you set this up correctly for your body text, then you will be guaranteed to get the lines of text to align across the spine and to 'back up' through the paper. Where the paper has any transparency at all, the lines of the body text should coincide back to back.

Text should always align across the spine of a double page spread, whether for print or eBook. In print, text should also align where columns are used. To be be more specific, the main text or body text must align to an imaginary baseline across the spread. In print the lines of text should coincide through the page when held up to the light.

InDesign can help control this through the 'align to grid' in the paragraph style settings, however care must be taken with this method since it may not achieve the desired result for a double page view for a **reflowable** eBook.

## So how can we get the correct alignment for both pBook and eBook?

If a text consisted entirely of body text with no headings or sub headings then no problem exists in making both sides of the spine align, as long as the space between the paragraphs is either nothing or a multiple of the body text leading. All you will need is the text to start from the same position both verso and recto and alignment is achieved. The problem arises when the text is punctuated with other blocks of text for the headings, sub-headings or block quotes, or you separate the paragraphs with a dimension that is not a multiple of the body text leading. If we are only dealing with print, then you can forget about aligning the headings to this grid, because the body text paragraphs will get back into alignment after the heading.

InDesign can help us by providing this 'align to grid' feature, but eBooks (being HTML and CSS) do not understand 'align to grid'. eBooks need to use 'line-height' (leading) and margins to achieve this vertical alignment. In transferring vertical spacing from InDesign to the eBook export, leading becomes line-height and space-before and space-after becomes margin-bottom and margin-top in the CSS.

Getting the alignment correct for the body text will involve some maths and a consideration of vertical units.

The first problem that we encounter with *InDesign* is the units in use. Type is measured in points, whereas other dimensions (vertical and horizontal) are measured in more worldly units such as millimetres or inches. Since 1 point measures 0.352777778 millimetres, we don’t want to have to keep making this conversion!

The vertical position of the lines of text are dependant on the type size, the leading and the space allocated before and after the full paragraph.

Since your type sizes and leading will use point units then you can set the vertical units in InDesign’s preferences to points also. This will then give you the benefit of being able to ensure that all vertical dimensions follow a multiple of the body text leading. But beware. You don’t want to set your preferences generally to use points for vertical units because you cannot (easily) set the page dimensions with points; for this you really need millimetres. So the trick is to set the vertical units to points after you have started the document and set the paper size and the margins.

You will see from the first images here that we can interrupt the flow of the body text with sub headings that are spaced with a multiple of the body text leading:

> Our body text uses 13pts leading so the space taken up by the subhead is 26pts, thus keeping the text aligned.

## What about images in the text?

If we introduce an illustration that has text **before** and **after**, then this will upset the vertical alignment of the body text, unless we can size the vertical dimension of the image with a multiple of the leading.
