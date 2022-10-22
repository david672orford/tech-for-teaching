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
Instead use **Format** ⟶  **Paragraph** ⟶  **Indents &amp; Spacing** to add more
**Spacing** either **Above Paragraph** or **Below Paragraph**.

### Inserting SVG Images

1.  From the menu choose **Insert** ⟶  **Image** ⟶  **From File**
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

1. Go to **View** ⟶  **Toolbars** and enable **Form Controls**.
2. Toggle the **Design Mode** button on on the form controls toolbar.
3. Click on one of the form element buttons on the form controls toolbar.
4. Click and drag on the screen to draw the control.

### Inserting Hyperlinks

1. If the anchor text already exists, select it.
2. Choose **Insert** ⟶  **Hyperlink** from the main menu.
3. If you are linking to another document at ReadyRussian.org, choose
   **Document** in the left-hand pane. Click the folder to the right of
   the **Path** field and select the document. Otherwise choose
   **Internet** and type the URL into the **Target** field.
4. Enter the anchor text into the **Text** field if it is not there
   already.
5. Press **OK**

### Editing Hyperlinks

1. Put the cursor just before the hyperlink.
2. Choose **Edit** ⟶  **Hyperlink** from the main menu.

### Removing Hyperlinks

1. Put the cursor just before the hyperlink.
2. Very carefully right click at the same location.
3. Choose Remove Hyperlink from the context menu.

### Adding Index Entries

1. Place cursor at beginning of word or if it is a phrase, select it
2. Choose **Insert** ⟶  **Table** of Contents and **Index** ⟶  **Index Entry**
3. If you would like the entry to appear under a heading, enter a 1st
   key and possibly 2nd key (for up to two levels)
4. If this is the best treatment of the term, then check the Main Entry
   box
5. Press the Insert button
6. If you wish, leave the dialog box open, select a different word, and
   return to step 3

### Setting Variables in the Text

1. Choose **Insert** ⟶  **Fields** ⟶  **Other** from the main menu.
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
2.  Choose **Edit** ⟶  **Fields** from the main menu.
3.  Change the value and press the OK button.

### Removing Variables from the Text

1.  Move the cursor to the small gray marker which indicates that a
    variable is set.
2.  Delete it using the Delete or Backspace key as if it were a
    character.

### Revision Date and Copyright Notice

Libreofice Writer stores the revision date of the ODT file in the metadata
automatically. You can insert this date in the document automatically. To
do this:

1.  Go to **Insert** ⟶   **Field** ⟶   **More Fields**
2.  Select the DocInformation tab
3.  Choose Modified from the left-hand column and Date from the center
    column.
4.  Press the Insert button.

A grey box will be inserted at the cursor position. If the document has already
been saved, then the date will be displayed in this grey box.

To display the document revision date at the top or bottom of each 
page:

1.  Go to **Format** ⟶  **Page Style**, select the Header or Footer tab,
    check the box to turn the header or footer on, and press the
	OK button.
2.  Returning to the page, click in the header or footer area
    (depending on which you enabled) to move the cursor into it.
3.  Go to **Insert** ⟶  **Field** ⟶  **More Fields**, and insert the Modified
    field using the procedure described above.
4.  Insert other appropriate fields such as page number. Use tabs
    to space them out.

Of course, the file modification date changes whenever you save the document,
whether or not you have made a meaningful change. So you may want to have
a date or version number which you control and change whenever you make a
revision to a document which you consider non-trivial. To do this you can 
create a custom document property which will be stored in the document metadata.

To create a custom document property:

1.  Got to **File** ⟶  **Properties**
2.  Select the **Special Properties** tab
3.  Click on the **Add Property** button and add what you need

You can then insert these custom properties in the text, header, or footer:

1.  Place the cursor in the text, header, or footer where you want the
    special property to be displayed.
2.  Go to **Insert** ⟶  **Field** ⟶  **More Fields**
3.  In the left hand pane click on **Custom** to expand it revealing
    your custom properties.
4.  Highlight the custom property you want and press the **Insert** button.

### Inserting Special Characters and Accent Marks

Go to **Insert** ⟶  **Special Character** to open Writer's built-in character map.
Find the character you want, possibly by using the search function, and
press the Insert button.

You can also insert special characters using any of the methods described
in our article [Entering Special Characters](../special-characters).

### Document Thumbnails

By default Libreoffice takes a screenshot of the first page of the document and
saves it in the ODT file as a 198x256 pixel PNG file with the name
"Thumbnails/thumbnail.png". In theory these images can be used instead of a
generic icon to represent the file in a file manager. It is unclear whether
any file managers actually use it.

If you wish to disable the embeded thumbnails, go to **Tools** ⟶  **Options** ⟶  **Libreoffice**
⟶  **Advanced** ⟶  **Expert Configuration** and search for “GenerateThumbnail”. Set it to
false. This will reduce the size of the file by about 15000 bytes which can be
significant since the rest of the ODT file may not be much larger than that.

### Importing Address Lists

Open the CVS file. When the import dialog comes up, click on the ZIP code column
in the example and change the column type to **Text**.

### Using Mail Merge

Here is a simple way to do a mail merge:

1.  Create a list of names and address in tabular format. You can use Libreoffice
    Calc or Base or a CSV file.
2.  Open your document in Write and go to **Edit** ⟶  **Exchange Database**.
3.  Click on Browse, and select the file created in step one.
4.  Find the file in the list of available **Available Databases**, select a sheet,
    and press **Define**.
5.  Open the **View** menu and turn on **Data Sources**. A list of data sources
    and a table showing the data will appear at the top.
6.  Find the columns you want and drag the column headers into your document.

When you connect databases in Libreoffice, they remain connnected indefinitely.
To disconnect them, go to **Tools** ⟶   **Options** in the menu. Then open
the **LibreOffice Base** category in the left-hand panel and choose
**Databases**. Select the unwanted database connection and press **Delete**.

More information about mail merging can be found in the
[Libreoffice Writer Guide Chapter 11](https://documentation.libreoffice.org/assets/Uploads/Documentation/en/WG4.2/PDF/WG4211-UsingMailMerge.pdf).

### Hiding Blank Lines in Mail Merge Labels

* Open the data sources
* Got to **Insert** ⟶   **Field** ⟶   **More Fields**, select the 
  **Functions** tab, and then **Hidden Paragraph**.
* Drag the data field which is sometimes blank from the data sources to
  the **Condition** field. This will insert the name of the field in
  square brackets.
* Append a space and EQ "" to define the condition for hiding the paragraph.
* Click the **Insert** button.
* If the hidden paragraph is now empty, reinsert the data field.

### Multiple Mail Merge Labels Per Page

You can print multiple labels per page by repeating the template. However, you must
insert an invisible "next record" field in front of all templates after the
first. Otherwise you will get a whole page of labels for each address.

To insert the "next record" field, go to **Insert** ⟶  **Field** ⟶  **Other**. Switch
to the **Database** tab and choose **Next Record** and press **Insert**.

### Toggling Display of Hidden Paragraphs

There used to be an option in the **View** menu for toggling the display
of hidden paragraphs, but it was removed at some point. To get it back,
go to **Options** ⟶   **Customize** ⟶   **Menus**. There is you find
the command and insert it into the **View** menu.

### Import CSV File with ZIP Codes

When you open a CSV file, an import dialog will appear. If you simply press
OK, the ZIP codes will be converted into decimal numbers which means that
the leading zero of East-Coast ZIP codes will be lost. To prevent this,
right click on the heading of the ZIP code column and change the type to
<b>Text</b>.

### Macros

* [Recording Macros](https://help.libreoffice.org/6.2/en-US/text/shared/guide/macro_recording.html?DbPAR=SHARED)
* [Assigning a Macro to a Toolbar](https://ask.libreoffice.org/t/assign-macro-to-toolbar/33575)


