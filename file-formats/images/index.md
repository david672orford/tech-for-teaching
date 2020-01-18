## Image Formats

Image files are used to store photographs, drawings, and scans of documents.
Computer image file formats can be divided into two basic groups: raster
formats and vector formats.

GIF, JPEG, and PNG are raster image formats. SVG and EPS are vector formats.

### Raster Verses Vector Formats

To understand the difference between raster and vector graphics, imaging that
you drew a picture on graph paper and had to instruct someone over the phone to
duplicate the picture on a blank piece of graph paper. You would have to
options: 1) You could ask him to label the rows and columns and then tell him
what color to make each square, or 2) you could tell him what shapes to draw,
how big to make them, and where they should be placed on the grid. The first
option is the way raster images work: They describe a grid of dots. The second
option is how vector images work: they describe what shapes to draw and where.

Digital photographs are stored in raster format. If you scan a drawing done on
paper, or a page from a book, that is in effect a photograph and will be in
raster format too. Only drawings done on the computer will be in vector format.

Images in raster format have one big disadvantage. Unless many small dots are
used, they will be visible. If a small raster image is enlarged, the dots may
be come very visible. This effect can be disguised by bluring the dots, but
that makes the whole image blurry.  Another disadvantage of raster images is
that they are difficult to modify.  If we want to remove an object, we have to
draw or paint what was behind it.  This is labor-intensive and requires
considerable skill.

Vector images have neither of these disadvantages. If they are enlarged, they
are redrawn using however many dots the display or printer can display. If we
remove an object from a raster image, it will be automatically redrawn without
that object and whatever was behind it becomes visible.

Vector images can be and frequently are converted to raster format. If you do
this, you should keep the original vector image somewhere in case you ever want
to improve or change. You can then regenerate the raster version.

Raster images can sometimes be converted to vector format, but this is tricky.
The objects in them have to be traced, either by hand, or automatically. When
this is done automatically, the resulting vector shapes can sometimes be
interlocked or broken up in unexpected and illogical ways which makes the
drawing difficult to modify. This is why it is important not to loose the
vector versions of your drawings.

### Vector Formats

The most common vector formats are SVG, EPS, and Adobe Illustrator format.
SVG is the most modern format. Images in this format can be edited in a variety
of programs and can be embedded in web pages without conversion.

### Raster Formats

GIF format is one of the first used on the World Wide Web. It used to be the
dominant format for photographs. It keeps the details of a photograph sharp,
but it reduces the number of colors to no more than 256. The remaining colors
are replaced with the nearest color of the 256. Most of the time, this is OK,
but color gradients such as skin or sand dunes can get a stair-step effect.
GIF is not used much more except for images which play a looped animation.

JPEG has almost entirely replaced GIF for photographs. JPEG format can preserve
more colors than GIF. If also reduces the size of the file by discarding some
of the fine detail, hopefully in a way which is not noticable to the human eye.

The person who creates a JPEG file can choose how much detail to throw away
by choosing a quality setting. This is a number such as 85. If this number is
made larger than it needs to be, the file will be excessively larger which
is a problem when the photograph is used on a web page since it may take
too long to download. If the quality setting is reduced too aggressively,
then the photograph will start to blur in a splotching way and in extreme
cases fuzz and wiskers will sprout from some of the objects shown.

If you distribute photographs in JPEG format, you should choose an appropriate
resolution and level of compression, but be sure to keep the high-quality
originals for when you want to make changes or when the resolution of computer
monitors improves and your distribution versions start looking bad.

JPEG is designed to handle the smooth contours and smooth color changes of
natural photographs or computer renderings which are intended to look like
photographs. It does not perform well on images with many sharp edges. These
include screenshots, line art, and logos. For these you should use PNG format.
This format is designed to deal well with the large areas of the same color
followed by a clean switch to another color which characterize such images.

In summary, use JPEG for photographs and things which look like photographs.
Use PNG drawings created in a computer, including screenshots of user interfaces.

