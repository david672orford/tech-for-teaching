## Working with PDF Files

Use the [PDF Toolkit](https://www.pdflabs.com/tools/pdftk-the-pdf-toolkit/) to
split and merge PDF files.

### Rotate Page

This is useful if your scanner outputs PDF files and sometimes the image
is on its side:

    $ pdftk printer_001107.pdf rotate 1right output snowman.pdf

### Extract Pages

    $ pdftk document.pdf cat 5-7 12-15 output extract.pdf

### Concatenate PDF Files

    $ pdftk file1.pdf file1.pdf cat output combined.pdf

