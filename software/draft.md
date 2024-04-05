## Unfinished Evaluations

These entries are here because, while I found these programs interesting,
I have not used them enough to recommend them.

### Web Browsers

* [Chromium](chromium/)

### Web Development Libraries
* [Toast UI](https://ui.toast.com/)
  * [Markdown Editor](https://github.com/nhn/tui.editor)
  * [Auto Complete](https://ui.toast.com/tui-auto-complete)
  * [Context Menu](https://ui.toast.com/tui-context-menu)
  * [Image Editor](https://ui.toast.com/tui-image-editor)
  * [Grid](https://ui.toast.com/tui-grid)
  * [Chart](https://ui.toast.com/tui-chart)
* [CSSScript.com](https://www.cssscript.com/)
  * [Markdown Editors](https://www.cssscript.com/tag/markdown-editor/)
  * [Menu and Navigation](https://www.cssscript.com/categories/menu-navigation/)
  * [Suneditor](https://www.cssscript.com/minimal-wysiwyg-editor-pure-javascript-suneditor/)
  * [Fully Styled UI Component Library – PCUI](https://www.cssscript.com/ui-component-library-pcui/)
  * [Elegant File Input Enhancement Plugin With JavaScript – filepond](https://www.cssscript.com/elegant-file-input-enhancement-plugin-javascript-filepond/)
  * [Draw SVG Paths Between Two Elements – leader-line](https://www.cssscript.com/draw-svg-paths-two-elements-leader-line/)
  * [Feature-rich Event Calendar In JavaScript – Calendar.js](https://www.cssscript.com/feature-rich-event-calendar/)
* [Anvil](https://anvil.works/) some kind of framework based on Python
* [Twinery](https://twinery.org/) may be a framework for interactive fiction
* [Web Component Libraries](https://www.webcomponents.org/libraries)

### Web Office Suites
* [Onlyoffice](https://helpcenter.onlyoffice.com/server/docker/opensource/opensource-script-installation.aspx?_ga=2.171818464.1118353405.1597510942-615934063.1597510942)
* [Nextcloud](https://hub.docker.com/_/nextcloud/)

### Raster Graphics
* [MyPaint](http://mypaint.org/) -- Tested version 2.0.1 in May 2021 on Ubuntu
    20.04. Worked but drawing was laggy. Bar at top for selecting tools gave no
    visual indication that a tool had been successfully selected.
* [Photopea](https://www.photopea.com/) -- Online photo editor

### Video Production
* [Natron](https://natrongithub.github.io/) --
	Compose effects shots. Keying, tracking, etc.
	As 2021 this program has not been actively developed for several years.
* [Storyboarder](https://wonderunit.com/storyboarder/) --
	Assemble drawings into storyboards.
	Can generate basic drawings of characters automatically.
	Owner feudes online with those who object to dirty words in the program.
* [qStopMotion](http://www.qstopmotion.org) --
	Program to take a series of photos using a camera connected to your
	computer and later assemble them into a video. Works with webcams
	and some SLR's.

### 2D Animation Editors
* [Glaxnimate](https://glaxnimate.mattbas.org/) --
	Vector animation with tweening. Has a "record" mode in which all changes
	(supposedly) produce keyframes.
	Saves in some kind of JSON format.
	Can export in Lottie and Telegram animated stickers formats, animated SVG, and video.
	Scriptable in Python.
	Has fairly good documentation.
* [Blender](https://blender.org) --
	2D animation can be done in blender using the Grease Pencil. 2D objects
	can also be placed in 3D scenes and animated.
* [Synfig Studio](https://www.synfig.org/)
	Vector and cutout animation. Supports tweening. Now has vector export.
	Interfaces seems cluttered and chaotic.
* [Wick Editor](https://www.wickeditor.com/) --
    A promising web application for creating animations. Can export the finished
	animation as a video file or as a player which draws the animation in real
	time to an HTML5 canvas.
* [Enve](https://maurycyliebner.github.io/) --
	Very promising vector animation. As of May 2021 tweens do not have
	easing. Developer says he is in poor health, project has slowed
	and may not continue. Frustration attempting to create keyframes.
	Can export to SVG format with animation.
	No meaningful documentation. Tutorials on Youtube.
* [OpenToonz](https://opentoonz.github.io/e/) --
	Seems to be for hand-drawn 2D animation.
* [Tahoma2D](https://tahoma2d.org/) --
	Seems to support hand-drawn, vector, and stop-motion animation.
	Author describes it as "based on OpenToonz".
* [Krita](https://krita.org/) --
	Krita has support for 2D animation drawn frame-by-frame. Can export to video.
* [Pencil2D Animation](https://www.pencil2d.org/) --
	Raster and vector "hand drawn" animation. Does it support tweening?
* [TupiTube](http://www.tupitube.com/) --
	Site does not impress. Linux version has a sub-1.0 version number.

### 2D Animation Libraries
* [Svg.svg](https://svgjs.com/) --
	Javascript library for adding animation to SVG drawings. You can make a drawing in
	Inkscape, put it on your web page, and then use this library to show and hide elements
	(including layers), move things around, scale and rotate, them, all at a time
	and speed you specify. Recommended for basic animation needs where a game platform
	would be overkill.
* [Python Lottie](https://pypi.org/project/lottie/) --
	A Python framework for working with Telegraph animated stickers which
	are in a subset of Lottie format. Includes a Blender export plugin.
	By the author of Glaxnimate.

### 2D Game Libraries with Sprite Animation for Web Browsers
* [Pixi](https://www.pixijs.com/) --
	This is a sprite renderer. A sprite is a 2D image which is moved around the
	screen in a video game. Think of the of the invaders, canon, and bullets
	in Space Invaders. To use Pixi you write Javascript code to load your
	sprite image and to move then around, changes their size, rotate them, etc.
	Pixi alone is sufficient for animation. If you want to make a game, you can
	use additional libraries (suggested in the documentation) to detect
	collisions, make sounds, and simulate physics, or you can use one of
	several game engines which incorporate Pixi while providing these functions.
    * [Learning Pixi](https://github.com/kittykatattack/learningPixi)
* [Phaser](https://phaser.io/) --
	Phaser is a complete system for creating games which run in a web browser.
	Games are created by writing code in Javascript, so a basic understanding
	of that language is required. Phaser 2 uses Pixi as the sprite renderer.
	Developement of Phaser 2 continues under the name Phaser CE. Phaser 3
	uses its own sprite renderer.
    [Flavio Tutorials](https://flaviocopes.com/tags/phaser/)
* [Gdevelop](https://gdevelop-app.com/) --
	Gdevelop is another system for 2D games run in a web browser. Like Phaser,
	it uses Pixi to render the sprites.	

### 3D Game Engines
* [Defold](https://defold.com/) -- Scriptable in Lua

### Audio Processing
* [Aeneas Forced Aligner](https://github.com/readbeyond/aeneas) --
	Given a recording of speech and a transcript, find the start and end
	time of each utterance. See also detailed instructions at
	[Sil.org](http://software.sil.org/downloads/r/readingappbuilder/Reading-App-Builder-07-Using-aeneas-for-Audio-Text-Synchronization.pdf).

### Web Content Management Systems
* [Nikola](https://getnikola.com/) --
	Static site generator in Python

### References
* [Libre Arts](https://librearts.org/)
* [Self-Hosted Photo Management](https://arstechnica.com/gadgets/2021/06/the-big-alternatives-to-google-photos-showdown/)

