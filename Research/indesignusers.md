## Important Tips for InDesign Users when Making eBooks

### Turn on hidden characters
Keep this on to show you where you might have empty paragraphs, double spaces, space at the end of a paragraph/heading, tabs, and soft-breaks.
Some of these things you might want to be rid of, but some, just may not convert to the ePub.{check on where to find hidden characters}

### Create a root paragraph style for the major part of the content
This makes sense if you have a lot of text that needs a style applying. Use select-all and then style with that body text style. The headings can then be styled afterwards.

### Use a  'Next-Style' as a rule for the headings
Headings will be  followed by a special first paragraph in the chapter or sub-section.

### Make a style for every category of content that you will have in your publication
These styles get converted to HTML mark-up in the ePub.
Make sure everything is styled with a style definition. If you use bespoke styles (by selecting attributes directly), your ePub may contain hard-to-edit, complex markup.

### Give names to your styles that make sense for the kind of content that belongs there
For paragraphs and headings use names that can easily be identified. An example might be 'first paragraph after the title', or 'author name'.
Character styles need names like 'citation' or 'name of country', or 'latin name'. Not 'italic' nor 'red underlined'!

### When using colour in text, define it with RGB values not CMYK. 
Colour defined in CMYK usually end up as the nearest 'web safe' colour. Our devices can do better than that!

### Provide every style with a tagging rule for HTML and ePub
If you leave the setting on 'Automatic' you are allowing InDesign to come up with it's own HTML tags when exporting to the ePub.
Use an HTML tag (h1 to h6) for a heading (not 'p'). InDesign may tag the HTML in the ePub with such things as `<p class="heading">`. It will work, but it should be <h1>. The reason that we don't want headings marked-in as `<p>` is that, when  you embed fonts in the eBook, and users change the font, then the headings will change as well as the body text. In other words, all text marked-up as `<p>` can be changed, headings tags cannot. Using proper HTML heading tags (h1-h6) will 'lock-down' your choice of font.

### Tag names and classes cannot have spaces in the names
Use 'camel-case' - like this: 'ChapterTopic'

### Keep text threaded
You may have got used-to the idea of putting a text box here and there for headings. Unless these loose text boxes are linked or anchored, they may all end up at the back of the book!

### Put caption information in the metadata of the images
Maybe your photo library/ asset managers and editors to do this.
You can then automatically populate the caption text box with this data.

### Anchor images and objects that need to flow within the main text
Objects need to be anchored so that they will flow with the text. They may need to move on to the following page, if the user of your eBook, increases the font size.
Images that are not anchored will probably appear at the end of your eBook
You should anchor at a paragraph break, even if, your print version has the image right after a particular line of text.

### Group the images with their captions and anchor those grouped objects
In your print version, you may have captions appearing in a variety of places. Try to use a consistent location in the eBook. This will make your life easier. 

### Name the object styles that you use
Objects such as images or groups will be tagged with a `<div>` name that matches the name of the object style; like this one: `<div class=”figure”>`

### Use the Table of Contents feature to create your table of contents
The TOC needs to be interactive. InDesign will export the correctly formatted TOC for the ePub only if you have used the correct auto-generated TOC.
You may want more sophisticated control and style for the print version, but you can always create a different TOC style for the eBook version.

### Dropcaps
You can use the dropcaps feature of InDesign, but you will need to create a character style for the dropcap letter, and apply to the first letter in that paragraph.

### Empty paragraphs
Don't create space between paragraphs by using a line break (ENTER or RETURN key). Space before or after a paragraph or heading should be provided by the style not with empty paragraphs. You will find `space-before` and `space-after` under the `Indents and Spacing` paragraph style control. 

### Avoid the use of the soft break to make a word go to the next line
In your print version you may have used a soft-break to balance the lines or even to control orphans and widows. This will upset things when someone views in the eBook, because the line may suddenly wrap in the middle of a sentence!

### Use character styles rather than bespoke style over-rides. 
When you import (place) text from MS Word, the author may have italicised some text. If this is still required then create a character style for it, and then use Find/Replace to look for italic and replace with the new character style (see the next item here)

### Avoid using style names that refer to their appearance (like italic)
This obliges you to use that appearance even I'd design dictates otherwise. Of course you can change the style, but for anyone else who needs to edit your ePub, their poor brain will hiccup when they see `<span class=”blue”>` and they need to change the style to underlined red!
When setting the rules for a character style, remember, that it will always inherit the basic formats from its parent; the parent is the paragraph in which it resides.
You should not select the font name again (it will be unusual to have a different font inside a line), because this will make it difficult for you to change the style of that paragraph.
You will also find that it will over complicate the style rules in the ePub CSS.
If you want text in uppercase, do not type as THAT but rather create a style that changes the text to uppercase
A future generation of designers in your publishing company may want to re-publish this work. They may prefer these headings to have small-caps. Now thay need to dig in to the actual text and re-key those capitals — or use GREP.
Avoid handcrafting the table of contents
Use the feature in ID to generate automatically from the headings and subheadings. Even if you want extra features in there like images or intro text, start with the auto generated and then add those features. This will then give you an interactive TOC in the ePub (required). Alternatively, you can build this auto generated TOC on the pasteboard of ID, and it will transfer to the ePub (off the page)
Do not expect to control the appearance of spreads in a flowable eBook
Do not put captions to images on a different page
Although you can attempt to get content to start on a new page, you don't know if this will be verso or recto. Fixed-format books are different!
InDesign CC for print
and ePub from the Same File?
Is it possible to use InDesign creatively so that the same file will produce good quality print (PDF) output, and then, with no modifications export for ePub3?
Often times, book publishers will have their design studios working with InDesign to produce PDFs for print output. At the end of that workflow, comes the decision to create an eBook version.
It is sometimes the case that the book designer has used InDesign in such a way that creating the eBook by exporting from InDesign is impractical unless the file is re-worked, with changes to the styling rules; the removal of style overides, the choice of a different font, the anchoring of pictures etc etc.
What are the pitfalls and can book designers change their habits so publishers will not need to outsource this work?
Just a few facts first.
InDesign is a great wysiwyg page layout tool, but the what-you-see-is-what-you-get only applies to the print or PDF output. You won't see exactly the same in the resulting re-flowable eBook.
Re-flowable ePubs need certain constraints, that PDFs do not, but these constraints are not disadvantageous for the print/PDF version; anchored images (a requirement for the ePUB), will still afford the flexibilty of position that you may need in the print version.
'Drag and drop' was your friend, but now it could be your greatest enemy.
If you use a book panel with book chapters as separate files, the technique for exporting to ePub is slightly different. I will explore this in a later article.
Page Size
If we are starting the production of an eBook without even considering print, then we might start an InDesign file with a 'Digital Publishing Intent' - giving us a page size of 1024x768px portrait for the iPad. Good, if you want to simulate the appearance on the iPad, but really not required at all. So if your page is set up as a 'real' book size: eg. 156mm x 234mm with margins of 24mm top and bottom with 18mm and 16mm inside and outside, then fine for a re-flowable eBook.
Conclusion: Leave as is - you don't need to change the page size.
Orientation and spreads
Re-flowable eBooks are normally viewed portrait. Although the iPad does give us a side-by-side view in landscape mode, this is not the same as spreads that you may see in your InDesign view. You can use spreads in your InDesign file for your print /PDF purposes, but these spreads will not result in a spread view. If your print book is designed as landscape pages, you can leave alone, but your eBook will look nothing like the print version unless you build a fixed-layout eBook.
Conclusion: Leave as is - spreads can stay, the exported ePub will show in portrait. Spreads in InDesign are ignored on export.
The ebook cover
The cover of the eBook can be any shape that you like, although a landscape shaped cover will probably be shrunk down very small in a typical eBook library thumbnail view.
It is likely that InDesign creatives will have cover files separate, maybe as wrap arounds with spine and flaps. You need to extract the front part from this and link at the point of export to ePub. But, one thing you will need to address if you use this method - the image must be in RGB format - InDesign will not convert this linked image when exporting to ePub.
Remember, covers are often seen in thumbnail views, so make sure the title can be read at small sizes.
You will need a large version of the cover for marketing purposes when you deliver through the Apple iBooks. This needs to be 1400pixels on the short side.
Conclusion: Some changes may be required, but the cover is often not included in the main InDesign file for print; it is more likely to be printed separately.
Master pages
When you export to ePub, all of the master page items are ignored. headers, footers, page numbers etc. They won't get exported.
Conclusion: leave your master page items alone.
Pagination
Probably the most difficult of all, is dealing with page beginnings and ends. Book designers will often have finely crafted their InDesign files to get an exact number of pages (book extent) and will have adjusted leading and font spacing to remove orphans and widows. Since many of these adjustments will be ignored, they can stay, but some old habits need to be expunged! For example, if a soft break has been added near the bottom of a page (to remove a paragraph widow), then this will be a disaster in the eBook. It could result in a sudden break in the middle of a line. It is essential that the book design uses a different technique in InDesign. I advise using the keep together options in the paragraph style rules. This should tackle your orphan and widow problems for the print version and will be delivered as CSS rules in the ePub3 file (orphan and widow control has very limited support in eBook readers).
You will certainly want your chapters to start on a new page. For your print version you may have used keep options > Start on Next page. This is good for print, but you will also need to use 'split ePub' for the heading style in order to 'chunk' the ePub into different XHTML files (one for each chapter, typically).
In some versions of InDesign (at the time of writing 9.2), there is an annoyance:
If you use 'start on next page' or 'start in next column' for a heading style, the resulting CSS for the ePub will include the following rule for that style:
page-break-before:always;
This may be very useful where you have a sub-heading that needs to start on the following page, but if you use 'start on next page', and 'split ePub' for a heading style (say a chapter heading), then you will get a blank page!
Conclusion: You can edit out the 'page-break-before:always;' CSS at the end of the process.
Fonts
This could be the subject for a much longer article but generally, if your licences allow it, then you can embed the fonts that are used in print into the ePub. However, not all font types are supported in the ePub, and - further, not all devices support all fonts.
Conclusion: You will need to experiment. You may need to compromise the print version in order to achieve the desired ePub version. On the other hand, you can opt to export without the font embedding, and thus, depend on the eReader device fonts.
Typography
There are many sophisticated typographic controls available in Adobe InDesign, and you may have been using baseline shift, hyphenation and justification fine controls, and even Align to Grid. All of these attributes will be ignored on export to ePub.
If you make a lot of use of 'Align to Grid' and have set up a baseline grid across your spreads, then you need to be aware, that, even though spacing between paragraphs and heading looks great for print, you are going to lose this spacing when exported to ePub. You have to find another way to get the correct spacing. Use space before and space after in the Indents and Spacing section of the paragraph style attributes panel.
Conclusion: Not all of your fine controls will work in the ePub, but, no-matter, in most cases you can ignore, but be careful with alignment to the baseline grid, since you may think you have good spacing, but this will be gone in the ePub.
Illustrations
If you have photographs or other images in the book for print, then you must be sure to anchor these images, so that they will be closely tied the place in the text, when exporting to ePub. It may be that an image is moved on to a facing page, because it does not fit in with the layout concept of the book. This should not be a problem. A picture can be on a previous page but anchored to the text on the opposite page. You will need to use 'Anchored Object Options' with a Custom Position that allows you to manually arrange.
When you export to ePub, you have a range of options for images, but if you opt to Use the Original Image, then you will need to convert those images yourself to RGB jpegs or PNG files. A better option is to use Preserve Appearance from Layout and Relative to Text Flow.
It is a good practice to include alternative text for images within the ePub file. You can get this to work most efficiently if you use metadata within the images themselves. Use Photoshop to add metadata (title, description etc). You can pull this metadata into your alternative text automatically, and, even use in the captions.
Conclusion: InDesign CC does a good job with images on export to ePub, but there are some important details you need to consider.
Text Flow and Structure
For the best results for the simplest of books, is to be sure that all text if threaded in one 'story'. For print book designers who have placed text boxes here and there throughout the document, without anchoring them or threading them into the main story, I have to say, you will struggle to get a good ePub from InDesign. Change your approach. Anchor those text boxes at the appropriate places in the main text, but please get out of the habit of creating headings with separate text boxes and drag/dropping them onto the page. This simply has to stop! Include the text in the structure. Not only will this give the better ePub results, but you also need to think about the table of contents (next section).
Conclusion: Text threading and structure of content does impact significantly on the resulting ePubs. Do try to keep your text threading simple with objects anchored inside those text frames. Multiple stories are possible, and you can use these stories as a way of ordering your 'articles' - which in turn can be used as the Content Order when exporting. Threading and content order should not change the PDF output.
Table of Contents
You may (indeed are likely to) have a table of contents as part of your front matter in the print book. In the eBook version this needs to be interactive, so that users can navigate to their chosen section or chapter. This interactivity will only work if you have used InDesign's clever way of creating this TOC from the heading styles. You must use Layout > Table of Contents to build this TOC.
Technically, there is no need to have the TOC displayed on the page at all, so you can create on (or move to) the pasteboard. Some publishers do prefer to include the TOC on the page as well, but generally this is not required and is doubling up without reason. On the other hand, you might add summary information to the TOC, and then you are really adding value to the page based version.
If you do use a Table of Contents on the page then leave off the page numbers, since they are dynamically changing.
Conclusion: There are some changes that may be required when building the TOC. InDesign CC does have the feature of saving versions of the TOC, so you can have alternatives to choose from when you export to ePub.
Post Editing after Export from InDesign
Avoid, at all costs editing the XHTML files inside the ePub package, otherwise you make it difficult to 'round-trip' to InDesign.
What you should do is to edit he CSS file and then create your own from this base. Export again from InDesign and link this CSS file. Style rules are then overridden by your version.
