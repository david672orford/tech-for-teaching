Libreoffice Writer Cookbook
===========================


Using Stylesheets
-----------------

Each handout should have a document title at the top with a style of
Heading 1. The style of each subheading should be Heading 2. Neither
heading should contain manual formatting.

The use of blank lines to increase vertical space should be avoided.
Instead use Format-&gt;Paragraph-&gt;Indents & Spacing to add more
Spacing Above Paragraph or Below Paragraph.

Revision Date and Copyright Notice
----------------------------------

TODO

Adding Accent Marks
-------------------

TODO

Tables for Layout
-----------------

TODO

Inserting SVG Images
--------------------

1.  Insert-&gt;Image-&gt;From File
2.  Choose the file and press Open.

A copy of the image will be stored inside the ODT file. A PNG fall-back
image will also be created and stored along with it.

If you have several complex SVG images, it can slow Openoffice to a
crawl. If this happens, go to
Tools-&gt;Options-&gt;Libreoffice-&gt;Memory and increase the graphics
cache size to at least 128MB.

Creating PDF Forms
------------------

1.  Go to View-&gt;Toolbars and enable Form Controls.
2.  Toggle the “Design Mode” button on on the Form Controls toolbar.
3.  Click on one of the form element buttons on the Form Controls
    toolbar.
4.  Click and drag on the screen to draw the control.

Inserting Hyperlinks
--------------------

1.  If the anchor text already exists, select it.
2.  Choose Insert-&gt;Hyperlink from the main menu.
3.  If you are linking to another document at ReadyRussian.org, choose
    “Document” in the left-hand pane. Click the folder to the right of
    the “Path” field and select the document. Otherwise choose
    “Internet” and type the URL into the “Target” field.
4.  Enter the anchor text into the “Text” field if it is not there
    already.
5.  Press OK

Editing Hyperlinks
------------------

1.  Put the cursor just before the hyperlink.
2.  Choose Edit-&gt;Hyperlink from the main menu.

Removing Hyperlinks
-------------------

1.  Put the cursor just before the hyperlink.
2.  Very carefully right click at the same location.
3.  Choose Remove Hyperlink from the context menu.

Adding Index Entries
--------------------

1.  Place cursor at beginning of word or if it is a phrase, select it
2.  Choose Insert-&gt;Table of Contents and Index-&gt;Index Entry
3.  If you would like the entry to appear under a heading, enter a 1st
    key and possibly 2nd key (for up to two levels)
4.  If this is the best treatment of the term, then check the Main Entry
    box
5.  Press the Insert button
6.  If you wish, leave the dialog box open, select a different word, and
    return to step 3

Setting Variables in the Text
-----------------------------

1.  Choose Insert-&gt;Fields-&gt;Other... from the main menu.
2.  Choose the Variables tab.
3.  Set Type to Set variable.
4.  Enter the variable Name. If it is already set elsewhere in the text,
    you may choose its name from the Select list.
5.  Enter the desired Value.
6.  Press the Insert button (only once).
7.  Press the Close button.

Editing Variables in the Text
-----------------------------

1.  Move the cursor to the small gray marker which indicates that a
    variable is set.
2.  Choose Edit-&gt;Fields from the main menu.
3.  Change the value and press the OK button.

Removing Variables from the Text
--------------------------------

1.  Move the cursor to the small gray marker which indicates that a
    variable is set.
2.  Delete it using the Delete or Backspace key as if it were a
    character.

Document Thumbnails
-------------------

To disable document thumbnails, go to
Tools-&gt;Options-&gt;Libreoffice-&gt;Advanced-&gt;Expert Configuration
and search for “GenerateThumbnail”. Set it to false.

