---
author: David Chappell
---

## Document Formats

There are many different file formats for creating and storing documents
in offices and on the Internet. Here we describe some of the most important.


### Plain Text Files

The simplest format is a plain text file. It is called plain text because
that is all it contains: the letters, numbers, symbols, and spaces which
make up the document, one after another. You can think of it as instructions
to a robot typewriter telling it what keys to press. Actually, that is what
it is. It is the codes a teletype machine would need to receive in order
to type out your document.

In plain text format there is almost no provision for formatting. We can start
a new line by pressing the **Return** key, but there is no separate way to
start a new paragraph. If we don't press **Return** until the end of the
paragraph, the editor may wrap it and it may not. Worse, if we send someone a
plain text file, the program he uses to view it may not wrap it and instead
display it as a really long line. So most people press **Return** at the end of
each line as if they were using a typewritter.

You can also use tabs, but there is no way to set the tab stops and no solid
agreement on where they will be, though most of the time there is one every
eight columns.

On a typewriter you can backspace or move the carriage back to type over what
you have already typed. If you type the same thing you get bold.  If you go
back and type underlines, you underline the words. While in theory plain text
format allows this, it practice you can't since plain-text editors have no
provision for these complexities.

So no bold, no italics, no underline, and no font changes. Plain text format
is suitable only for very simple documents. It's one strength is that a
plain text document using the ASCII characterset can be read on practically
any computer.

If you want to go beyond plain text format, you have three choices. You can
1) Add elaborate markup codes to the text, 2) follow a simple markup convention,
or 3) use a word processor. We will discuss these options below.

### Wordprocessor Formats

A word processor is an advanced text editor designed to more fully exploit the
capabilities of the output device, be it a teletype, a laser printer, or a
high-resolution screen.  Files produced by word processors contain snippets of
plain text inside, but it is surrounded by instructions about how it should be
styled and placed.

From the time of their invention in the 1970's, word processors have grown and
developed to cover the the capabilities of new output devices and the requirements
of new uses. Their file formats have changed with them. Initially each word
processor had its own format. But with the wide use of the Internet exchanging
documents between offices became more common and it was necessary to standardize
on a few formats.

Today the most widely used word processor is Microsoft Word. Consequently its file
format, or rather its file formats, for there are several, are de-facto standards.

DOC files are simply a dump of what Word has in memory when you are editing a
document.  As a consequence the DOC format changed a little with each major
version of Word and it changed completely with Word 97. Because it these are ad
hock formats which is ultimately defined by the code of the current version
Microsoft Word, they have never been fully documented. Modern competing world
processors can load DOC files, but they may not preserve all of the formatting
correctly.

Microsoft has long been aware that the DOC format is a mess inside and has
offered a second format called Rich Text Format (RTF). This format is intended
to represent the text and formatting in a clean way more suitable for
interchange with other programs. Microsoft could have made RTF the default
format in Word, but did not. This is unfortunate since very many programs can
read and write RTF format.

Most other word processors have standardized on a different format. This is the
[Open Document Format for Office Applications (ODF)](https://en.wikipedia.org/wiki/OpenDocument).
It has been an international standard since May 2005. The standard has been updated
several times since. The standard is supported by numerous organizations. Documents
in ODF format can be read and written by practically any word processor including
Openoffice, Libreoffice, Microsoft Word, and Google Drive. To a large extent it
has taken over from RTF format.

In 2008 Microsoft switched Word and the rest of Microsoft Office to new formats
known as [Office Open XML](https://en.wikipedia.org/wiki/Office_Open_XML) or
DOCX. This format had also been adopted as an international standard in December
2006 despite concerted opposition from those who felt that it was of low quality
and that a second international office document standard was not need. Critism
of its quality centered around the idea that it was simply a repackaged version
of the old inscrutible DOC format. That the documentation stretched for two
thousand pages while still leaving some features undescribed lent credence to this
view. Though some of the competing word processors can load these files, they still
format them imperfectly which may indicate that these criticism are justified.

### Portable Document Format (PDF)

PDF is not so much a document format as a phototypesetting format. It captures
the appearance of a document as it would be printed by a program such as a word
processor. But a PDF file does not have explicit information about columns,
paragraphs, or sometimes even words. These higher-order groupings can only be
infered from how the letters are positioned on the page.

PDF files are good for distributing documents, such as classroom worksheets, which
the recipient will print out. For this purpose PDF is better than a word processing
format because the recipient is far more likely to have a program which can open and
print PDF files than he is to have the word processor you used. In most cases
the document will look exactly as it did when you printed it. The only exception
is if you used fonts which he does not have. But you can avoid even this problem
by embedding the font in the PDF file.

As we said above, PDF files are not meant for editing. But this does not mean that
they cannot be edited at all. Because the letters, lines, and pictures on the page
are all separate elements, they can be deleted and moved around and other elements
can be added. What you cannot do is add or delete a word and expect the surrounding
text to adjust itself as it would in a word processor.

If you need to make major revisions to a document and all you have is the PDF file,
you have to somehow reconstruct the original editable document. There are programs
which will look at the PDF file and try to extract the text and some of the formatting,
but the results are hit-or-miss. In the end you will probably have to redo most
of the formatting.

Some people mistakenly believe that PDF is a multi-page raster image format for storing
scanned documents. This is because it is sometimes used in exactly that way. In this
case each page contains nothing but a large image which shows the scanned document.
This is not the normal way to use PDF. It is used in this case as a convenience because
PDF viewers are more readily available than viewers for multi-page raster image formats
such as TIFF.

PDF is a vector format which means that it when used as intended a PDF document describes
what to draw on the page rather than conveying a picture. It is closely related to the
earlier PostScript format and the later SVG vector image format. All three formats
describe what to draw using the same semantics.

### Hypertext Markup Language (HTML)

Word processors are not the only way to go beyond plain text. Markup languages are another
approach. In markup languages the person writing the document types codes which give 
instructions for formatting the document. The most famous is the Hypertext Markup Language
(HTML) in which web pages are written.

The codes in HTML are known as tags. The are very obvious, even intrusive. For example,
here are two paragraphs in HTML:

    <p>This paragraph goes on for more than one line. There is
    no doubt that all these lines are part of the same
    paragraph because they are surrounded by <b>p</b> tags.</p>
    <p>We can print in <b>bold</b> or <i>italic</i>. We can even
    do <b><i>both at once</i></b>.</p>

This produces the following:

<p>This paragraph goes on for more than one line. There is
no doubt that all these lines are part of the same
paragraph because they are surrounded by <b>p</b> tags.</p>
<p>We can print in <b>bold</b> or <i>italic</i>. We can even
do <b><i>both at once</i></b>.</p>

Writing all the tags in HTML can be tedious. There are editors which make the job easier.
You can even write a document in a word processor and save it as HTML, though the result
may be poor. If you plan on creating web pages, you should take the time to learn some
HTML so you understand what is going on, even if you use an HTML editor to make the
process less tedious.

### Markdown

One way to make writing HTML pages less tedious is to write them in a simpler
format with less intrusive codes and then convert that to HTML. It is similiar
to what writers with typewritters did years ago when preparing their
manuscripts. They might use equal signs to underline subheadings or use
asterisks to represent the bullets in a bulleted list. Later the typesetter at
the publisher would see this and select the proper typeface and weight.

One popular convention is called Markdown. Markdown is pretty simple. For
example, a blank line ends a paragraph. Putting asterisks around a word makes
it italic.  Putting double asterisks around a word makes it bold. Putting one
or more pound signs and a space in front of a line makes it a heading of a
particular level. If markdown lacks a convention for what you want to do, you
can always fall back to HTML codes. They will appear as-is in the final HTML
document.

The number-one goal of Markdown is readability. A document in Markdown can look
reasonably presentable as is, even without conversion to HTML. 

Markdown is used on a number of websites. There are small differences from site to
site in the way Markdown works. Sites will often provide a guide to their particular
dialect. There are also programs which you can run on your computer so that you
can write documents in Markdown using a text editor and convert them to HTML
or some other format.

For more information about writing in Markdown, see the online
[Markdown Guide](https://www.markdownguide.org/).

### Wiki Markup

Wiki Markup, like Markdown, is a set of simple conventions for indicating how a
document should be formated. Versions of Wiki Markup are used on numerous
collaborative websites known as wikis, the most famous of which is Wikipedia.
The [Wikitext Examples](https://meta.wikimedia.org/wiki/Help:Wikitext_examples)
will give you an idea of how it works.


