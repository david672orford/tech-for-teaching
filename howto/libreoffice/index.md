---
author: David Chappell
---

## Libreoffice Writer Cookbook

Here are some notes on things we have had to do in Libreoffice when
creating classroom handouts.

### Escaping from Tables

If the the last item on a page is a table, it can be difficult to insert
something after it. The trick is to move the cursor to the far bottom 
right cell of the table and press Alt-Enter.

If the page begings with a table and you want to insert something before it,
go to the top left cell and press Alt-Enter.

### Using Stylesheets

Each handout should have a document title at the top with a style of
**Heading 1**. The style of each subheading should be **Heading 2**. Neither
heading should contain manual formatting.

The use of blank lines to increase vertical space should be avoided.
Instead use Format ⟶ Paragraph ⟶ Indents & Spacing to add more
Spacing Above Paragraph or Below Paragraph.

### Inserting SVG Images

1.  From the menu choose **Insert ⟶ Image ⟶ From File**
2.  Choose the file and press the **Open** button.

A copy of the image will be stored inside the ODT file. A PNG fall-back
image will also be created and stored along with it.

### SVG Image Performance Problems

Starting with version 4.0 Libreoffice has a serious problem with the way it
renders SVG images in the page. Above a certain number of images or a certain
level of complexity it slows to a crawl.  Users who complain about this on the
Internet are frequently advised to increase the size of the graphics cache to
128MB, but this does not seem to help. There is a
[bug report](https://bugs.documentfoundation.org/show_bug.cgi?id=83426)
open since September 2014. Though the bug causes Writer to lock up for
seconds or minutes at a time it is categorized as of "low minor" importance!

### Creating PDF Forms

1. Go to View ⟶ Toolbars and enable Form Controls.
2. Toggle the “Design Mode” button on on the Form Controls toolbar.
3. Click on one of the form element buttons on the Form Controls toolbar.
4. Click and drag on the screen to draw the control.

### Inserting Hyperlinks

1. If the anchor text already exists, select it.
2. Choose Insert ⟶ Hyperlink from the main menu.
3. If you are linking to another document at ReadyRussian.org, choose
   “Document” in the left-hand pane. Click the folder to the right of
   the “Path” field and select the document. Otherwise choose
   “Internet” and type the URL into the “Target” field.
4. Enter the anchor text into the “Text” field if it is not there
   already.
5. Press OK

### Editing Hyperlinks

1. Put the cursor just before the hyperlink.
2. Choose Edit ⟶ Hyperlink from the main menu.

### Removing Hyperlinks

1. Put the cursor just before the hyperlink.
2. Very carefully right click at the same location.
3. Choose Remove Hyperlink from the context menu.

### Adding Index Entries

1. Place cursor at beginning of word or if it is a phrase, select it
2. Choose Insert ⟶ Table of Contents and Index ⟶ Index Entry
3. If you would like the entry to appear under a heading, enter a 1st
   key and possibly 2nd key (for up to two levels)
4. If this is the best treatment of the term, then check the Main Entry
   box
5. Press the Insert button
6. If you wish, leave the dialog box open, select a different word, and
   return to step 3

### Setting Variables in the Text

1. Choose Insert ⟶ Fields ⟶ Other... from the main menu.
2. Choose the Variables tab.
3. Set Type to Set variable.
4. Enter the variable Name. If it is already set elsewhere in the text,
   you may choose its name from the Select list.
5. Enter the desired Value.
6. Press the Insert button (only once).
7. Press the Close button.

### Editing Variables in the Text

1.  Move the cursor to the small gray marker which indicates that a
    variable is set.
2.  Choose Edit ⟶ Fields from the main menu.
3.  Change the value and press the OK button.

### Removing Variables from the Text

1.  Move the cursor to the small gray marker which indicates that a
    variable is set.
2.  Delete it using the Delete or Backspace key as if it were a
    character.

### Document Thumbnails

By default Libreoffice takes a screenshot of the first page of the document
and saves it in the ODT file. While this may be used somewhere as a preview
image, it is not required and makes the ODT file larger. To disable document
thumbnails, go to Tools ⟶ Options ⟶ Libreoffice ⟶ Advanced ⟶ Expert Configuration
and search for “GenerateThumbnail”. Set it to false.

### Revision Date and Copyright Notice

TODO

### Adding Accent Marks

TODO

### Using Tables for Layout

TODO


