---
author: David Chappell
---

## Web Fonts

In this article we explain how to select fonts using CSS in your web pages.
We assume you already know how to create a web page by writing HTML and
how to style is using CSS.

### Selecting Fonts Built-in to the Browser

In CSS fonts are selected by specifying the font family and then indicating
the desired variant. For example:

```css
font-family: Times;
font-weight: bold;
font-style: italic;
font-size: 12pt;
```

In web browser will take these preferences and select the closest font it has.
When it comes to weight and style this is not difficult, all it has to do
is go through its fonts and find the best match. But if the font family you
request is not available, the next best match is hard to identify.

The browser may consult a font-substitution table. There it may learn that
if "Times" is not available, "Times New Roman" should be used instead which
is fine since they are almost identical.

But if the requested family is not installed and is not listed in the
substitution table, you will probably get the web browser's default font
which may be far from what you want. To avoid this, specify a list of
font families sending with one of the generic family names:
"serif", "sans-serif", "monospace", "cursive" or "fantasy". For example,
if we want Times New Roman, but will settle for any serif font:

```css
font-family: Times, "Times New Roman", serif;
```

We look for Times New Roman under the Linotype and then the Monotype
names and if neither is found, we settle for any serif typeface.

A more complicated example:

```css
font-family: Palatino, "Palatino Linotype", "Palatino LT STD", "Book Antiqua", Georgia, serif;
```

In this example we ask for Palatino under three different names, and if
that fails, we ask for Monotype's clone (Book Antiqua), before settling for
Georgia, and if that fails, any serif typeface.

Here are some sites which suggest font substitution lists:

* [CSS Web Safe Font Combinations](https://www.w3schools.com/cssref/css_websafe_fonts.asp)
suggests a few substitution lists
* [CSS Fonts from Dan's Tools](https://www.cssfontstack.com)
gives dozens of substitution lists and sample pages so you can see what
each will look like on your browser

### Downloading Additional Fonts

While you can generally get something acceptable by specifying fonts
from the standard sets decribed in our article on
[Standard Typefaces on Personal Computers](../standard/),
you get more control if you ask the browser to download fonts you choose.
There are hundreds of fonts available for free, many of them of high
quality.

TODO: Explain how to use web fonts

### Additional References
* [Web Typography](https://en.wikipedia.org/wiki/Web_typography)
Wikipedia article describes the history of the support for fonts in web browsers
* [CSS Fonts Module Level 3](https://www.w3.org/TR/2018/REC-css-fonts-3-20180920/)
Standard for font support in CSS

