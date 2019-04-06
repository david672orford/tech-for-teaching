# Understanding and Selecting Typefaces

A typeface is a set of letters for typesetting. Originally a font was a set
of metal type of a particular typeface in a particular size, but today
the terms are generally used interchangably.

Typefaces come in sets called families. The typefaces within a family will
share a common design of the letter shapes but differ from one another
in regular ways.

The similarities without the family likely include:

* Whether the letters all occupy the same width on the page, like on a type
writer, or whether they occupy only the space they need, like in a newspaper.
If they all occupy the same width, the typeface is <b>monospaced</b>.
If the 'W' takes more space than the 'i' or the 'l', then the typeface
is <b>proportionally spaced</b>.
* Whether the letters has <b>serifs</b>. Serifs are the little caps on the
ends of the long strokes of the typefaces used in books and newspapers.
* The length and width of the serifs, if present, in relationship to the
lengths and widths of the main strokes.
* The height of the lower-case letters in relationship to the upper-case
letters. This is known as the <b>x-height</b> because it is expressed
as the lower-case letter 'x'.
* Regular differences in widths of strokes, such as horizontal verses
vertical strokes or strokes along the two diagonals.

The regular variations include:

* Weight: light, medium, and dark variants are created by varying the width
of the strokes.
* Width: the family may include versions of the typeface which have been 
squeezed or stretched horizontally.
* Slant: The letters may be slanted a few degrees to the right. If they are
slanted without significantly altering their forms, they are said to be
<b>oblique</b>. If some of the strokes are curved to make the whole letter
appear rounder, then the typeface is said to be <b>italic</b>.

## Basic Typefaces

While modern computer systems often have hundreds of fonts installed, they will
almost always have versions of the following typeface families:

* A proportional-width typeface with serifs, some version of
  [Times New Roman](https://en.wikipedia.org/wiki/Times_New_Roman)
  which <i>The Times</i> of London commissioned from Monotype and started
  using in 1932. Times typefaces are commonly used for the body text
  of articles and books.
* A proportional-width typeface without serifs, similar to
  [Helvetica](https://en.wikipedia.org/wiki/Helvetica Helvetica). Typefaces like
  this have traditionally used for signs. They may also be used sparingly in
  books to set off certain parts of the text such as chapter titles, captions
  to illustrations, or additional information in boxes. Today typefaces
  like Helvetica are also widely used in computer interaces to label the
  controls.
* A monospaced slab-serif similar to
  [Courier](https://en.wikipedia.org/wiki/Courier_(typeface)) of the IBM
  Selectric typewriter. Typefaces like this are used when it is desirable
  for the letters on a page to line up in rows and columns, such as when
  writing computer code, or where tradition demands that the printed document
  look like it was produced with a typewriter.

Each of these three typeface families will have at least four variants:
regular, bold, slanted (oblique or italic), and both bold and slanted.
In total, there are 12 fonts which should always be available to your
document no matter where it is displayed.

The typeface actually used may not look exactly the same as the one on
your computer, but it will be close and most importantly, the letters
will have the same width. This is important when the line breaks cannot
or should not be changed. This is particulary important in PDF documents
where each line break and frequently the placement of each letter are
fixed. In this case the substitution of a typeface with different letter
widths can be disastrous as letters run into one another or weird gaps
open which looks awful and even destroy legibility.

These four typeface families each in four variants are sufficient for
ordinary books and documents. You can safely assume that they are acceptable
substitutes will always be present. If you choose to use other typefaces,
you will either have to provided them to recipients of electronic
documents by embedding them or accept the fact that one of the typefaces
above may be automatically substituted.

Android devices are a notable exception to the above in that they do not
seem to have typefaces width-compatible with Times and Helvetica. In
particular Google Chrome for Android will simply provide the system
default serif font when asked for Times and the system default sans-serif
font when asked for Helvetica. This can occasionally cause problems because
Droid Serif is a bit wider than Times. This is particularly troublesome in
SVG illustrations were the right sides of lines of text can be cut off.

## Adobe PostScript Fonts

The precedent for computer typeface was set by the Apple Macintosh computer
and the LaserWriter printer which used the Adobe PostScript printer language.
Together they were widely used for desktop publishing.

The original LaserWriter and other printers with PostScript level 1 contained
these build in fonts:

* [Times](https://en.wikipedia.org/wiki/Times_New_Roman) (4 variants)
* [Helvetica](https://en.wikipedia.org/wiki/Helvetica) (4 variants)
* [Courier](https://en.wikipedia.org/wiki/Courier_(typeface)) (4 variants)
* Symbol (1 variant, Greek letters and mathematical symbols)

Times and Helvetica were licensed from Linotype. Originally these
fonts included only the Latin alphabets of Western European languages.

Times is dignified and legible typeface which is widely used. However, the
later 35-font version of the PostScript set provides other choices which
are less ornate and even more legible.

The PDF standard defines a base set of fonts which include the origin 13 fonts
from Adobe PostScript plus Zapf Dingbats (see below).

For PostScript level 2 Adobe licensed 22 more typefaces:

* Helvetica (4 new narrow variants)
* New Century Schoolbook (4 variants) (is there an MS equivalent?)
* Palatino (4 variants)
* Bookman (4 variants)
* Avant Garde Gothic (4 variants)
* Zapf Chancery (1 variant, medium italic) (is there an MS equivalent?)
* Zapf Dingbats (1 variant, decorative elements)

New Century Schoolbook is a member of the
[Century family](https://en.wikipedia.org/wiki/Century_type_family)
of *very* readable typeface designed for
grammar school textbooks. [Palatino](https://en.wikipedia.org/wiki/Palatino)
is considered a good typefaces for body text. Both are less ornate that
Times New Roman.

[Bookman](https://en.wikipedia.org/wiki/Bookman_(typeface)) or
Bookman Old Style is a serif typeface. It is most used at
large sizes in headings and at small sizes in advertising. It is
generaly not used for body text.

[Avant Garde Gothic](https://en.wikipedia.org/wiki/ITC_Avant_Garde)
is a sans-serif typeface used in logos.

[Zaph Chancery](https://en.wikipedia.org/wiki/ITC_Zapf_Chancery)
is a script typeface (it looks like it was written
with a wedge-shaped pen.) Only the italic form is included.

It is usually safe to use any of the basic 35 PostScript fonts in your documents
and web pages. They are installed by default on devices from Apple. As explained
below, Linux and Microsoft Windows computers have substitutes which look very
similiar and have letters of the same width so the formatting of the document
should not change.

## The URW Fonts and GNU Freefont ==

The increasing standardization on the Postscript typefaces created a problem.
Indepently licensing a full set was difficult and expensive. This was
particularly a problem for users of Ghostscript, a free close of PostScript.
Since the software was distributed free-of-charge, its authors could
not license the now standard 35 fonts.

In 1996 [URW++ Design and Development Incorporated](http://www.urwpp.de/)
came to the rescue. They released as free software their own set of 35
fonts which were visually similiar to those which Adobe had licensed and
most importantly had been adjusted to have the same letter widths.

* Nimbus Roman No9 L = Times
* Nimbus Sans L = Helvetica
* Nimbus Mono L = Courier
* Standard Symbols L = Symbol
* Century Schoolbook L = New Century Schoolbook
* Palladio L = Palatino
* Gothic L = Avant Garde Gothic
* Bookman L = Bookman
* Chancery L = Zapf Chancery
* Dingbats = Zapf Dingbats

These are high-quality fonts from a respected foundary. URW decided to
offer them for free distribution because the bulk licensing of similar
fonts by Adobe and Apple had depressed their commerical value. The
company decided that they would be more valuable in mass free distribution
as a way of advertising the company name.

Like the PostScript fonts of the time they covered only Latin alphabets.
The three font families which coorespond to Times, Helvetica, and Courier
have since been expaneded and released as
[GNU FreeFont](https://www.gnu.org/software/freefont/):

* FreeSerif (4 variants, 10,537 symbols)
* FreeSans (4 variants, 6,272 symbols)
* FreeMono (4 variants, 4,178 symbols)

In 2016 URW released [new versions of their 35 fonts](https://github.com/URWTypeFoundry/Core_35/)
TODO: find out more about these fonts, their names, etc.

## Microsoft Fonts

Microsoft licensed typefaces from Monotype (the inventor of Times
New Roman) instead of Linotype. These typefaces were created
or adjusted so that each letter would have the same width as in
the PostScript fonts. That way either set of typefaces could
be used to display the document without reformatting it.

The fonts in Microsoft Windows 3.1 in 1992 were:

* Times New Roman: a special version adjusted to have the same
character widths as Linotype's Times licensed by Adobe and Apple.
* [Arial](https://en.wikipedia.org/wiki/Arial): Monotype's answer
to Linotype's Helvetica. Has the same character widths.
* Courier New
* Symbol
* Wingdings

Because these fonts have the same widths as the PostScript fonts
and the URW fonts, they are very safe to use. If they are missing,
the equivalent font from another vendor will probably be 
substituted automatically.

In time Microsoft started distributing additional fonts compatible
with members of the standard set of 35 PostScript fonts:

* Book Antiqua: Monotype clone of Linotype's Palatino
* Palatino Linotype: expanded version of Linotype's Palatino produced for Microsoft
* Century Gothic: Monotype clone of ITC's Avant Garde
* Bookman Old Style: Monotype clone of ITC's Bookman

In 1996 Microsoft released its
[Core Fonts for the Web](https://en.wikipedia.org/wiki/Core_fonts_for_the_Web).
These included the 14 fonts listed above plus:

* Arial Black (1 variant)
* Andalé Mono (1 variant)
* Impact (1 variant)
* Comic Sans MS (regular, bold)
* Georgia (4 variants)
* Trebuchet MS (4 variants)
* Veranda (4 variants)

Microsoft's intent in releasing the Core Fonts for the Web
was to expand the base set of typefaces which all web designers could use
and thereby make web typography less boring. They become very popular and
are used on numerous websites.

Since then two changes have reduced the relevance of the Core Fonts. One is
the prominence of Android devices on which they are not installed by default.
The second is that modern web browsers can download and display fonts
specified by the web designer. Microsoft's license
[does not allow](https://docs.microsoft.com/en-us/typography/fonts/font-faq#web)
you to use these fonts in that manner. (Though you may be able to
license them from the foundary for a fee.) There are many other fonts
available for use on websites for free as described in our article
about [Web Fonts](../webfonts/).

For more information on typefaces distributed with Microsoft Windows see Wikipedia's article
[List of typefaces included with Microsoft Windows](https://en.wikipedia.org/wiki/List_of_typefaces_included_with_Microsoft_Windows)
and Microsoft's article
[Fonts and supported products](https://docs.microsoft.com/en-us/typography/font-list/).

## Liberation Fonts and Derivatives

These fonts are metrically compatible with the PostScript and Microsoft
equivalents:

* Liberation Serif = Times = Times New Roman
* Liberation Sans = Helvetica = Arial
* Liberation Mono = Courier = Courier New

They were created by Ascender Corporation under the name Ascender. RedHat
arranged for them to be licensed under the GPL. Google later also licensed them for use
as the Chrome OS Core Fonts. Version 2.0 of the Liberation fonts is based on the version
licensed by Google.

[Liberastika](https://github.com/eugeneai/Liberastika-fonts) is a derivative of Liberation
Sans with the Cyrillic portion redesigned to look better. Metric compatibility of the
Cyrillic letters with Arial was deliberatly not preserved since in the opinion of those
who did the redesign this was necessary to produce a good-quality Cyrillic typeface.

## Bitstream Vera and Decendants

[Bitstream Vera](https://www.gnome.org/fonts/)
has 300 glyphs covering the Latin alphabet. Families in the Bitstream
version collection include:

* Bitstream Vera Sans (4 variants)
* Bitstream Vera Sans Mono (4 variants)
* Bitstream Vera Serif (regular and bold)

An expanded version known as [DejaVu](https://dejavu-fonts.github.io/)
which has almost 3500 glyphs and additional styles.

## Other Noteworthy Typefaces

* [Opensource Typefaces](https://en.wikipedia.org/wiki/Category:Open-source_typefaces)
  Category page at Wikipedia
* [Garamond](https://garamond.org/)
  URW version is free for non-commercial purposes
* [Hershey Fonts](https://en.wikipedia.org/wiki/Hershey_fonts)
  Early vector font widely used in computer graphics. Includes Latin,
  Greek, Cyrillic, and Japanese letters.
* [Bitstream Charter](https://en.wikipedia.org/wiki/Bitstream_Charter)
  A simplified serif typeface designed in 1987 for good performance
  and high legibility on 300dpi laser printers. An expanded version
  is known as [Charis SIL](https://en.wikipedia.org/wiki/Charis_SIL).
* [Utopia](https://en.wikipedia.org/wiki/Utopia_(typeface))
  A serif typeface a version of which was released by Adobe as opensource
  software in 1989.
* [Computer Modern](https://en.wikipedia.org/wiki/Computer_Modern)
  A set of typefaces created by Donald Knuth. Widely used with the TeX
  typesetting system to typeset mathematical papers.
* [Gentium](https://en.wikipedia.org/wiki/Gentium)
  An award-winning typeface released in 2007 which in the Plus version
  has over 5500 symbols
* [Adobe's Source Family](https://en.wikipedia.org/wiki/Source_Sans_Pro)
  A set of serif, sans-serif, and monospace fonts with good alphabet coverage.
  The serif and sans-serif versions are also available in expanded versions
  with CJK coverage.
* [Droid Fonts](https://en.wikipedia.org/wiki/Droid_fonts)
  A set of serif, sans-serif, and monospace fonts 
* [Open Sans](https://en.wikipedia.org/wiki/Open_Sans)
  Popular sans-serif typeface for web pages and mobile apps. Highly legible on screens
  and at small sizes. Similar to Droid Sans, but with an italic variant
  and wider characters.
* [Roboto](https://en.wikipedia.org/wiki/Roboto)
  A sans-serif typeface family used as the default system font in Android since
  version 4.0. Also used on many Google web sites including YouTube and Google Maps.
  Provided in six weights.
* [Noto Fonts](https://en.wikipedia.org/wiki/Noto_fonts)
  A typeface family consisting of over a hundred individual fonts. It is intended
  to cover all of the script in the Unicode standard. It is used as a fallback
  font on Android devices. It is has serif and sans-serif variants. The Latin,
  Greek, and Cyrillic characters are derived from the Droid fonts. Noto CJK
  fonts are derived from the Adobe Source fonts.

## Other References

* [What Font Should I Use?](http://drmarkwomack.com/a-writing-handbook/style/typography/)

