# How to Make Series

* How to make web pages
  * Simple web page
  * Boilerplate
  * SEO
  * Markdown
  * Images: resolution, retina displays, avoiding reflow, adaptive size
* How to make handouts
  * Use Openoffice Writer
  * Convert to HTML using odt2html
* How to record audio
  * Microphone
  * Hum and noise
  * Level and clipping
  * Editing with Audacity
  * Encoding in MP3 and Ogg-Vorbis format
* How to make photographs
  * Compact cameras, smartphones, DSLR
  * White balance
  * Editing with Pinta
  * Embedding in Openoffice
  * Embedding in webpages
* How to make videos
  * Compact cameras, smartphones, DSLR
  * Narration added with Audacity
  * Editing with Openshot
  * Subtitling
* How to make screenshots
  * Why not to use JPEG format
  * Use video-screencast.py script as an example
  * Use Cutycapt to capture web pages in SVG format
* How to make screencasts
  * Limit size of window
  * Use Ffmpeg's x11grab
* How to make drawings
  * Using Inkscape
  * Inkscape tutorials
  * Embedding in Openoffice Writer documents
  * Embedding and scaling SVG in HTML
    * See https://css-tricks.com/scale-svg/
    * Having height and width in the &lt;svg&gt; tag can cause scaling problems in Safari
    * Set at least height or width of the &lt;img&gt; or &lt;svg&gt; tag, otherwise IE will
      set the size to 300px x 150px.
    * Use generic font family names or convert fonts to paths
  * Animation
    * Manipulating the SVG DOM from JavaScript in browser
    * Manipulating the SVG text using a script and rendering to video
    * Using Synfig
* How to make 3D models
   * Sweethome
   * Art of Illusion
* The Seven Sins of Safari
  * SVG swallows mouse clicks if it is in a &lt;button&gt;
  * Desktop Safari 6 does not scale up SVG &lt;img&gt; if it has height and width
    attributes in the &lt;svg&gt; tag
  * Mobile Safari 8 does not seem to support CSS unicode-range since without
    subset=cyrillic Google fonts do not have Cyrillic glyphs
  * iOS home screen apps open links in new Safari tab even if their target
    is an &lt;iframe&gt; in the very same page
  * In mobile Safari the assigned size of an &lt;iframe&gt; is ignored. Instead it
    is expanded to the size of the document which it contains.
  * iOS home screen apps have an ugly "elastic scrolling" effect in which 
    the whole app shifts up and down exposing a grey background to show
    that it is not scrollable.
  * No support for Service Workers

