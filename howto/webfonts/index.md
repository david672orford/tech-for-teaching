# Web Fonts

In this article we explain how to select fonts using CSS in your web pages.
We assume you already know how to create a web page by writing HTML and
how to style is using CSS.

# Selecting Existing Fonts

In CSS fonts are selected by specifying the font family and then indicating
the desired variant. For example:

 font-family: Times;
 font-weight: bold;
 font-style: italic;
 font-size: 12pt;

In web browser will take these preferences and select the closest font it has.
When it comes to weight and style this is not difficult, all it has to do
is go through its fonts and find the best match. But if the font family you
request is not available, the next best match is hard to identify.

The browser may consult a font-substitution table. There it may learn that
if "Times" is not available, "Times New Roman" should be used instead which
is fine since they are almost identical.

But if the font family which you requested is not installed on the system
and the web browser has no information about it (such as whether or not
it has serifs), then it will likely just use its default font family which
may be far from what you intended. Therefor it is better to give the web
browser a second and even a third choice. The last choice should be a 
generic font name such as "serif". For example:

 font-family: Times, "Times New Roman", serif;

Hopefully the browser could have done this with its font-substitution tables,
but it does not hurt to give it an explicit search list as we have done here.

A more interesting example:

 font-family: Palatino, "Palatino Linotype", "Palatino LT STD", "Book Antiqua", Georgia, serif;

Here are some sites which suggest font substitution lists:

* [CSS Web Safe Font Combinations](https://www.w3schools.com/cssref/css_websafe_fonts.asp)
* [CSS Fonts from Dan's Tools](https://www.cssfontstack.com)

## Additional References
* [Web Typography](https://en.wikipedia.org/wiki/Web_typography)
* [CSS Fonts Module Level 3](https://www.w3.org/TR/2018/REC-css-fonts-3-20180920/)


