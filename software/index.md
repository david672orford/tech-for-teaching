## Software for Creating Lessons

The programs listed on this page may proved useful to you for preparing course
materials. They are all available for free as [opensource software](https://opensource.org/).
We have favored software which works on Linux, Microsoft Windows, and Mac OS X.

Software for creating course materials should be easy-to-use. You should not
have to spend years learning how to produces decent results. It should also be
readily available to all so that you can share what you produce with your
colleges who can then modify them for their needs. Finally it is best if your
work can be stored in widely accepted formats which you will be able to open
and use again for years.

There requirements are not easy to meet. Programs for creative endevors can be
very expensive. They often save your work in files which only they can open.
Sometimes the format of these files changes between versions making it hard to
open files you created only a few years ago.

We also know that our readers use a variety of computers. While Microsoft
Windows is widely used, Apple Macintosh computers are very popular in
education. A few, including your author use Linux. For these reason, we try to
only recommend programs which run well on all three platforms.  All of the
programs recommended are available free-of-charge on the Internet from
reputable web sites.  Finally, to the maximum extent possible we have chosen
programs which either save in industry-standard formats or can export to such
formats.

Most of these programs we actually use regularly and can recommend.
In a few cases we describe well-known programs which we found unsuitable or
which we are still evaluating.

### Document Preparation and Viewing
* [Libreoffice](https://www.libreoffice.org/) --
	Libreoffice is a version of the popular [Openoffice](https://www.openoffice.org/) suite.
	This version is updated more frequently than the original.
	We particularly recommend the word processor which is called Write. Its native
	document format is ODF which is an international standard and can be read and
	written by most other word processors including Microsoft Word. See our
	[Libreoffice Cookbook](libreoffice/) for hints on using Write to produce
	classroom handouts.
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
	[Windows version](https://www.fosshub.com/Evince.html) --
	Document viewer for electronic document formats including PDF and DjVu.
* [Calibre](https://calibre-ebook.com/) --
	High quality ebook reader and ebook management system.

Other programs:
	[Abiword](),
	[Calgra Words](https://www.calligra.org/words/),
	[OnlyOffice](https://github.com/ONLYOFFICE/),
	[WordGrinder](https://cowlark.com/wordgrinder/)

### Lecture Slides
* [Revealjs](https://github.com/hakimel/reveal.js) --
	Javascript library which makes it easier to create presentation slides
	in HTML. Scales them properly to fit the screen and provides controls
	for switching slides, revealing points one at a time, etc. The library
	is free. If you do not know how to write HTML, there is an online
	presentation editor, but that requires a paid subscription.
* [Jessyink](http://tavmjong.free.fr/INKSCAPE/MANUAL/html/Extensions-JessyInk.html)
	An Inkscape extension (included) which makes each layer a slide in an
	presentation. It adds Javascript to the SVG file so that when it is
	viewed in a web browser one can page through the slides.

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

### Video Processing and Viewing
* [VLC](https://www.videolan.org) --
	A good solid all-around video player which will play most any file.
	Has classic media player controls.
* [FFmpeg](https://www.ffmpeg.org) --
	Very capable command-line program for converting audio and video files
	from one format to another or making them smaller in preparation for
	distribution. It has numerous options for cropping video, selecting
	start and end times, and much more. As a command-line tool, FFmpeg takes
	more effort to use the first few times, but once you have figured out
	the commands you need, you can make a cheat sheet or a script so that
	you can use them quickly without struggling to figure out what buttons
	you pressed in some GUI conversion tool. There are FFmpeg cookbooks on the
	web where you can find most of the commands you will need. These include
	[FFmprovisr](https://amiaopensource.github.io/ffmprovisr/) and our
	own [FFmpeg Cookbook](ffmpeg/).
* [Handbrake](https://handbrake.fr/) --
	Handbrake is an easy-to-use program for ripping DVD’s and converting
	video files from one format to another.
* [Shotcut](https://www.shotcut.org) --
	This is a good video non-linear video editor. Such editors are used to
	assembled recorded video into a finished film. You load your video files
	into the program, trim off unwanted material, and arrange them on a
	timeline. You can then add transitions (such as fads and wipes), titles,
	sound effects, and music. Then you can export the finished product as a
	single video file.
* [Youtube-DL](https://ytdl-org.github.io/youtube-dl/index.html) --
	A command-line program for downloading videos from Youtube and other
	websites. Useful if you want to show a video in class. You give it
	the URL of the video's webpage and it does the rest.

### Raster Image Editing
* [GIMP](https://www.gimp.org/) --
	The Classic opensource image editor. An answer to Adobe Photoshop. Can be
	bewildering for the casual user which is why we recommend Pinta.
* [Pinta](https://pinta-project.com) --
	An easy-to-use image editor. Can be used to draw like MS Paint. Can crop photos
	and adjust their color. Can load and save in BMP, PNG, JPEG, TIFF, and other
	formats, but seeminly not GIF. Recommended.
* [Imagemagick](https://www.imagemagick.org) --
	If you need to convert one or two images, you can use one of the raster
	graphics editors described above. But if you are processing hundreds
	of images, you are better off using Imagemagick. It can be used as a
	command-line program or you can use it as a library from your favorite
	programming language.

Other programs:
	[Krita](https://krita.org/),
	[MyPaint](http://mypaint.org/)

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
* [Dia Diagram Editor](http://dia-installer.de/) --
	Program for drawing flowchards, circuit diagrams, etc.

### 2D Animation
* [Svg.svg](https://svgjs.com/) --
	Javascript library for adding animation to SVG drawings. You can make a drawing in
	Inkscape, put it on your web page, and then use this library to show and hide elements
	(including layers), move things around, scale and rotate, them, all at a time
	and speed you specify. Recommended for basic animation needs were a game platform
	would be overkill.
* [Wick Editor](https://www.wickeditor.com/) --
    A promising web application for creating animations.

Other programs: [Synfig Studio](https://www.synfig.org/), [Pencil](https://www.pencil2d.org/),
	[TupiTube](http://www.tupitube.com/)

### Stop Motion Animation
* [qStopMotion](http://www.qstopmotion.org) --
	Program to take a series of photos using a camera connected to your
	computer and later assemble them into a video. Works with webcams
	and some SLR's.

### 3D Modeling
* [Blender](https://www.blender.org) --
	This is the definitive opensource 3D modeling program. It is very capable
	and serious users can get good work done quickly. However it requires a serious
	time commitment to learn it, so it is not a good choice for occasional use
	to create simple models.
* [Art of Illusion](http://www.artofillusion.org) --
	An easy-to-use 3D modeler. Written in Java, so it will run on most computers.
	Saves in its own inscrutible format, but can export in OBJ and VRML formats.
* [Sweet Home 3D](http://www.sweethome3d.com) --
	An easy-to-use program for creating 3D models of rooms with doors, windows, and furniture.
	See our article [Using Sweethome 3D](sweethome/).
* [X3dom](https://www.x3dom.org/) --
	Javascript library for displaying a 3D model on a webpage so it can be
	zoomed and rotated by the viewer.

### Web Game Platforms
* [Pixi](https://github.com/kittykatattack/learningPixi) --
	Game plaform with 2D sprite animation
	<br>(Not yet evaluated.)
* [Babylon.js](https://www.babylonjs.com/) --
	Game platform with 3D animation
	<br>(Not yet evaluated.)

### Other Software Lists
* [34 open source tools for creatives](https://opensource.com/article/16/12/yearbook-top-open-source-creative-tools-2016) --
	Describes applications for creating documents, drawings, videos, music, typefaces, and 3D models
* [Sil Language Technology's Products](http://software.sil.org/products/) --
	Software to help produce texts in languages for which adequate typefaces, dictionaries, and
	other tools are not yet available.
* [9 flowchart and diagramming tools for Linux](https://opensource.com/article/18/8/flowchart-diagramming-linux) --
	Describes programs for producing diagrams such as flowcharts, organizational charts, and circuit schematics.	
* [Pixls](https://pixls.us/software/) --
	A photographer's list of opensource tools

