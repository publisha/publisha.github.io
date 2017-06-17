# Is this the Final Version?
**Iterative Publishing**

Author: Chris Jennings
Date: 2017-06-15
Version: 0.5

## Abstract

Why do publishing students (or indeed publishers), save their files with such names as *finalversion1*?

Of course, we all know that it can't be the final version - they just hoped that it would be!

Books like other created artefacts go through a number of iterations before being ready for public display. The question is, can we observe and record what those changes are and when they happened, and by whom?

In this article we look at the way that the reader of the book will know what version they are reading and the author / editor will know what version they are editing. We look at this in relation to print, digital and author or editor workflows.

## Introduction

We should start by announcing a couple of quotes.

### Semantic Versioning

First from the organisation known as *semver* - short for Semantic Versioning. The Semantic Versioning[^1] specification is authored by Tom Preston-Werner, inventor of Gravatars and co-founder of GitHub. Here is the quote from Jurgen Van de Moere[^2], who explains semantic versioning better than I can:

> In essence a semantic version looks like this:
> **Major.Minor.Patch**
> So v1.3.8 has a major component with a value of 1, a minor component with a value of 3 and a patch component with a value of 1.

### Apple's Rules for eBook Versions

Apple are very strict when you want to update an eBook on the iBookstoe. Here are the rules from the iBooks Asset Guide[^3]

>In general, the first number of the version number represents a major revision; the second number would be used for a revision containing several changes/new information; the third number would be used to indicate minor changes, such as fixing a typo or formatting issues. For example, if the first version of the book was 1.0, a subsequent minor revision could be 1.0.1; a more substantial revision could be 1.1; a total rewrite could be 2.0.

These 2 quotes set the scene for what is to follow. What do we know about versioning in print and digital publishing and how might we borrow from practices in software development workflows.

## Part 1: Public Facing Versions

### In Print

There are a number of conventions that have been used over the years, and some style guides do attempt to keep this under some kind of order.

In _The Chicago Manual of Style_[^4] we do find:

>The publishing history of a book, which usually follows the copyright notice, begins with the date (year) of original publication, followed by the number and date of any new edition. In books with a long publishing history, it is acceptable to present only the original edition and the latest edition in the publishing history.

and also from _The Chicago Manual of Style_ with reference to impression numbers:

> Impression lines work to the advantage of readers and publishers both—a new impression not only reflects the sales record of a book but also signals that corrections may have been made.

When it comes to marketing advantage, there must always be a benefit it proclaiming *New Edition*, just as there is when we see a food package on the supermarket shelf that announces with a corner stripe *new improved Recipe*.

### Definition of Terms

**Edition** is used together with a date (just the year), to indicate the version of the book. So, if you are reading a later edition of the book then it might say so with the date; thus:

>First published in Great Britain 2012
>This edition published in 2017

Some changes were made to the book between 2012 and 2017. So, *edition* is equivalent to *version* in meaning, although only publicly available, **not** within the editorial workflow. We have only seen the term *version* used in one place, *The Elements of Typographic Style*, Robert Bringhurst, 2012.

**Revise** may be used indicate a stage in the editorial process as in *revise 1*, *revise 2*. Some publishers may also use *revised edition* on the imprint page as a way to promote improvement.

**Impression** is a term used to indicate a new printing. The term is rarely used on the imprint page, although you will see in the illustration here that OUP have recently replaced the *impression sequence numbers* with the term *Impression 4*.

A **Reprint** may be the same book but with some changes, although unless you see something like "with a new preface by ...", then you may not know. A reprint could be same content but reset with new type. It is different from a **facsimile** which is an exact copy (page-by-page).

**Errata** are corrections to a book when it has already been printed. The corrections are printed on a slip of paper and then glued into the front matter of the book before distribution. This happens very rarely, since this give a negative impression of the quality of the book. Since many books now have a companion web site, these corrections are often to found listed there.

### Imprint pages (title page verso)

When we explore imprint pages in the books on our shelves we find some interesting publishing strategies.



Book collectors, of course, prefer to own fist editions, so in their collections there will be limited information; just the first publication date. On the other hand, popular titles (see here 'Treasure Island'), will have many reprints and new editions up to the date of the edition you have. Many reprints are a gauge of the popularity of the title, although imprint pages do not tell us how many were printed. One could argue that many reprints show that the publisher was not confident enough for longer print runs.

As an alternative to taking a lot of space on the page, you see here from the 1949 edition of *Winnie the Pooh*, that it had been reprinted 38 times (presumably in that first edition), before this "Thirty-ninth edition".



**Impression Lines** are a string of numbers on the imprint page, that are incrementally erased, to show the current printing. It is interesting again, to flip over the title pages of our books to see this little cryptic message that is there for us to interpret. The publisher needs to first decide the highest number, because this suggests how many reprints might possible happen; a _pessimism / optimism_ indicator, I suppose.

For each printing the lowest number is erased.

You will see in the illustrations here that Oxford University Press have used impression numbers, and the popular *Economics* title in their *Very Short Introductions* series has lost all numbers 1 through 8, an indication that my copy is the 9th printing.

Oxford University Press have followed this convention until their *Microeconomics* title, in this same series. This now uses the less cryptic notation; my copy: *Impression: 4*. A rather sensible strategy, because the purchaser gets clear evidence that this is a popular title and must be good.

## Part 2: Workflow Versioning

As in the previous section, we can refer to the way authors worked in the past. You can see here a typed manuscript of *The Waste Land*, T.S. Eliot[^5], with notes and edits by himself, his wife Vivien Eliot and Ezra Pound. There is no timeline for the notes; in which order they were applied.

This is also the case when proof-readers use standard notation to markup corrections to a printed copy. The British standard (BS 5261)[^6] is adopted beyond the UK, but rarely provides times or staging for the corrections.

### Digital Tools

Many authors and editors will use **Microsoft Word** and the *track changes* feature of that software has become the often used method to get changes, additions or corrections approved. The system provides the means to edit the text and leave comments. Individuals involved in the process are named with their comments. There is no hierarchical control; we can can each accept changes or not with no overall approval workflow. It does work up to a point, but can get very complex when changes overlay one another.

Another approach may be to annotate a PDF of the pages. **Adobe's Acrobat Reader** software (there are others on the market) provides sophisticated annotation tools, as you can see here in the images. Not all software can easily edit the text within the PDF, so the proof reader is simply making suggestions for the editor to make in the original text.

#### eBook Editing

I add this as a slight deviation, but in my own experience, publishers of eBooks really need a good method of proof reading and annotating eBooks ready for distribution. Apple's iBooks software, does provide annotation tools (see in this attached figure from my own book), but sharing these annotations is not currently so easy. The annotations are nicely overlaid, but you can (as a write) only email the annotations as a text; detached from the pages themselves.

#### Editing in the the cloud

Cloud services such as **Google Drive** and **DropBox** do provide some version control although Google do provide apps that allow direct editing of files (Google Docs and Google Sheets), when those documents are shared for editing. Sharing documents is a nod forward to `Part 5: Collaborative Editing.`

Systems can be built and customised for revision control using Content Management Systems. Illustrated here are screens from an application that I have used to manage remote authors contributing to a global cookery book. Authors can input and edit their own recipes, with overall editorial control given to the chief editor, who then exports the data out as XML for use in page layout software for final 'print-ready' output.



## Part 3: Publishing Incrementally


## Part 4: Editing Incrementally


## Part 5: Collaborative Editing


[^1]: semver.org

[^2]: https://www.jvandemo.com/a-simple-guide-to-semantic-versioning/

[^3]: https://help.apple.com/itc/booksassetguide/


[^4]: http://press.uchicago.edu/ucp/books/book/chicago/C/bo8540260.html


[^5]: _The Waste Land Facsimile_, T.S. Eliot  (Author), Valerie Eliot (Editor) - Faber and Faber 2011


[^6]: Further details can be found on the Society for Editors and Proofreaders web site:  https://www.sfep.org.uk/standards/standards-in-proofreading/

Version control for ebook publishing
Pierre Thierry July 2013

https://www.w3.org/2012/12/global-publisher/statements-of-interest/34-vc.pdf

An Introduction to Version Control Using GitHub Desktop

By Daniel van Strien

http://programminghistorian.org/lessons/getting-started-with-github-desktop
