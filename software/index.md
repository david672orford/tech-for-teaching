## Software for Creating Lessons

The programs listed on this page may proved useful to you for preparing course
materials. They are all available for free as
[opensource software](https://opensource.org/).
We have favored software which works on Linux, Microsoft Windows, and Mac OS X.

Most of these programs we actually use regularly and can recommend.
In a few cases we describe programs which we found unsuitable or
which we are still evaluating.

### Document Preparation and Viewing
* [Libreoffice](https://www.libreoffice.org/) --
	A free office suite. A continuation of the Openoffice project. Includes
	an excellent word processor called Write. Its native document format is
	ODF which is an international standard and can be read and written by
	most other word processors.
* [ODF Format Specification](http://docs.oasis-open.org/office/v1.2/cs01/OpenDocument-v1.2-cs01.html) --
	Technical description of the file format used by Libreoffice. ODF files
	are ZIP archives which contain XML files in a format which is relatively
	easy (for a programmer) to parse and convert into other formats such
	as HTML.
* [Odt2html](https://github.com/david672orford/odt2html) --
	A Python script for converting ODF files to responsive web pages.
	There are a number of ways to convert ODT (ODF word processing) documents to
	HTML. For example, Libreoffice can save in HTML format, but the files it
	produces are intended to produce an exact representation of the printed
	document, not to produce good web pages which look good on screens
	of various sizes. In contrast Odt2html puts the production of good clean
	reflowable HTML first while preserving most formatting. To run this
	program you must have Python 2 installed on your computer.
* [Evince](https://wiki.gnome.org/Apps/Evince/)
	Document viewer for electronic document formats including PDF and DjVu.
	Windows version: (https://www.fosshub.com/Evince.html)
* [Calibre](https://calibre-ebook.com/) --
	High quality ebook reader and ebook management system.

### Audio Processing
* [Audacity](https://www.audacityteam.org/) --
	An excellent audio editor. You can load audio from files in formats
	including MP3 and WAV. If you have a microphone, you can record right
	in Audacity. You can then trim the audio, remove noise, adjust its tone,
	and combine multiple audio clips on a timeline. You can save the project
	to continue working on it later. When you are ready, you can export
	the finished audio in WAV, FLAC, MP3, and OGG formats.
* [Aeneas Forced Aligner](https://github.com/readbeyond/aeneas) --
	Given a recording of speech and a transcript, find the start and end
	time of each utterance. See also detailed instructions at
	[Sil.org](http://software.sil.org/downloads/r/readingappbuilder/Reading-App-Builder-07-Using-aeneas-for-Audio-Text-Synchronization.pdf).
	<br>(Not yet evaluated.)

## Video Processing and Viewing
* [VLC](https://www.videolan.org) --
	A good solid all-around video player which will play most any file.
	Has classic media player controls.
* [FFmpeg](https://www.ffmpeg.org) --
	Very capable command-line program for converting audio and video files
	from one format to another.
* [Handbrake](https://handbrake.fr/) --
	Handbrake is an easy-to-use program for ripping DVD’s and converting video files.
* [Vidcutter](https://github.com/ozmartian/vidcutter) --
	A very basic program for trimming a video file
* [Shotcut](https://www.shotcut.org) --
	A good non-linear video editor. Import a bunch of video clips, arange
	them on a timeline.

### Raster Image Editing
* [GIMP](https://www.gimp.org/) --
	The Classic opensource image editor. An answer to Adobe Photoshop. Can be
	bewildering for the casual user.
* [Pinta](https://pinta-project.com) --
	An easy-to-use image editor. Can be used to draw like MS Paint. Can crop photos
	and adjust their color. Can load and save in BMP, PNG, JPEG, TIFF, and other
	formats, but seeminly not GIF. Recommended.
* [Krita](https://krita.org) --
	Another answer to Photoshop. Has Linux and MS Windows versions, but may
	not have a MacOS X version.
	<br>(Not yet evaluated.)
* [Imagemagick](https://www.imagemagick.org) --
	If you need to convert one or two images, you can use one of the raster
	graphics editors described above. But if you are processing hundreds
	of images, you are better off using Imagemagick. It can be used as a
	command-line program or you can use it as a library from your favorite
	programming language.

### Vector Drawing
* [Inkscape](https://inkscape.org/) --
    An excellent vector drawing program which uses SVG as its native format.
  * [Inkscape: Guide to a Vector Drawing Program](http://tavmjong.free.fr/INKSCAPE/MANUAL/html/) --
      Book describing the features of Inkscape. Written by one of the
      program's authors.
  * [Inkscape](https://en.flossmanuals.net/inkscape/_full/)
      Draft version of a new (as of April 2019) book which explains the
      basic features of Inkscape.
  * [Mastering Inkscape in 2018](http://libregraphicsworld.org/blog/entry/mastering-inkscape-in-2018) --
      Blog posting with recommendations of books and video lessons on how
      to use Inkscape
  * [Isometric Projection in Inkscape](http://ahninniah.blogspot.com/2013/04/isometric-projection-in-inkscape.html) --
      Tutorial in drawing pseudo 3D pictures as done in technical drawings

### 2D Animation
* [Synfig Studio](https://www.synfig.org) --
    2D animation studio. Animation is done by defining keyframes which
    show where the parts of a drawing should be at particular times. The
    program interpolates between these positions to determine where the part
    should be at intermediate times. Exports to video. Attempts to create
    exporters for web animations (SVG) have made little progress.
  * [Synfig Tutorial](https://opensource.com/article/16/12/synfig-studio-animation-software-tutorial) --
      An article which introduces Synfig Studio and shows to to start using it
* [Pencil](https://www.pencil2d.org) --
    <br>(Not yet evaluated.)
* [TupiTube](http://www.tupitube.com/) --
    <br>(Not yet evaluated.)

### Stop Motion Animation
* [qStopMotion](http://www.qstopmotion.org) --
	Program to take a series of photos using a camera connected to your
	computer and later assemble them into a video.

### 3D Modeling
* [Blender](https://www.blender.org) --
	This is the definitive opensource 3D modeling program. It is very capable
	and serious users can get good work done quickly. However it requires a serious
	time commitment to learn it, so it is not a good choice for occasional use
	to create simple models.
* [Art of Illusion](http://www.artofillusion.org) --
	Easy-to-use 3D modeler. Written in Java, so it will run on most computers.
	Saves in its own inscrutible format, but can export in OBJ and VRML formats.
* [Sweet Home 3D](http://www.sweethome3d.com) --
	Easy-to-use program for creating 3D models of rooms with doors, windows, and furniture
* [X3dom](https://www.x3dom.org/) --
	Javascript library for displaying a 3D model on a webpage so it can be
	zoomed and rotated by the viewer.

### Web Animation and Game Platforms
* [Svg.svg](https://svgjs.com/) --
	Javascript library for adding animation to SVG drawings. You can make a drawing in
	Inkscape, put it on your web page, and then use this library to show and hide elements
	(including layers), move things around, scale and rotate, them, all at a time
	and speed you specify. Recommended for basic animation needs were a game platform
	would be overkill.
* [Pixi](https://github.com/kittykatattack/learningPixi) --
	Game plaform with 2D sprite animation
	<br>(Not yet evaluated.)
* [Babylon.js](https://www.babylonjs.com/) --
	Game platform with 3D animation
	<br>(Not yet evaluated.)

### Other Software Lists
* [34 open source tools for creatives](https://opensource.com/article/16/12/yearbook-top-open-source-creative-tools-2016)
* [Sil Language Technology's Products](http://software.sil.org/products/)
* [9 flowchart and diagramming tools for Linux](https://opensource.com/article/18/8/flowchart-diagramming-linux)
