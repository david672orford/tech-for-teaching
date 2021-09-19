## Creating 3D Models and Animations

Eventually I hope to offer recommendations for creating 3D illustrations
for use in instruction. Since I have not figured how best to do this
myself yet, for now this is just my notes.

X3D and its predecessor VRML (Virtual Reality Markup Language) are file
formats for 3D scenes to be displayed in web browsers.

## Software For Creating VRML/X3D Scenes

* [Blender](https://www.blender.org) --
	Can import and export in X3D format
* [Art of Illusion](http://www.artofillusion.org) --
	Can export in VRML format
* [White Dune](http://wdune.ourproject.org/) --
	Attempt to run on version 1.956 on Ubuntu 20.04 failed.
* [Titania](https://github.com/create3000/titania/wiki) --
	Snap package works on Ubuntu 20.04. Seems to suffer from
	long pauses.
* [X3D-Edit](https://savage.nps.edu/X3D-Edit/) --
	Appears to be an XML editor for X3D with preview. Written in Java.
	Uses an X3D viewer called Xj3D which is also written in Java.
	(The Xj3D.org website is now a programming news site.)
	As of 2021 website looks dated. Last stable release (4.0) in 2019.
* [X3DOM Component Editor](https://github.com/x3dom/component-editor) --
	Very basic web editor

### For displaying 3D Scenes, Animation, and Games in Web Browsers

* [X3DOM](https://www.x3dom.org/) --
	Javascript library for embedding X3D files in a webpage.
	[Source code](https://github.com/x3dom/x3dom) on Github.
	Some navigation modes appear to be broken. Try them in the
	[Navigation Example](https://doc.x3dom.org/tutorials/animationInteraction/navigation/example.html).
* [X\_ITE](https://github.com/create3000/x_ite/wiki) --
	Display X3D in a web browser. The scene is loaded from an external file.
* [Babylon.js](https://www.babylonjs.com/) --
	Game platform with 3D animation.
	Cannot load X3D scenes.
* [Three.js](https://threejs.org/) --
	With a plugin module has limited ability to load X3D scenes.
* [A-Frame](https://aframe.io/) --
	Higher level layer over Three.js

## Standalone 3D Game Engines and X3D Viewers

* [FreeWRL](http://freewrl.sourceforge.net/) --
	Classic VRML viewer. Last release was in January 2017.
* [Castle Game Engine](https://castle-engine.io/) --
	X3D seems to be its native format. Can load models in various formats.
	Scripting language is Pascal, though they are working on adding Javascript.
	Includes a program **view3dscene** which can display 3D models in a
	wide variety of formats.
* [Godot Engine](https://godotengine.org/) --
	Scripting language is similiar to Python.
	Does not seem to be able to load X3D scenes.
	There is a web version which uses webasm.
* [Panda3D](https://www.panda3d.org/) --
	Game engine written in C++, scripted in Python.
	Updated website around 2021.

## Other Animation Tools

* [Monster Mash](https://ai.googleblog.com/2021/04/monster-mash-sketch-based-tool-for.html)
* [PyMesh — Geometry Processing Library for Python](https://pymesh.readthedocs.io/en/latest/)
* [Armory3D](https://armory3d.org/)

## Animation Tutorials

* [Walk Cycle Tutorial](http://www.angryanimator.com/word/2010/11/26/tutorial-2-walk-cycle/) --
	How to realistically animate a walking character
* [Animation magician: 8 ways to turn cheating into an art form](https://opensource.com/article/17/5/animation-magician-how-turn-cheating-art-form) --
	Techniques for telling a story with less animation
* [How to Make Animated Peeps](http://www.jaanga.com/2012/04/how-to-make-animated-peeps.html) --
	Creating human models with Makehuman and animating them with BVH files in Three.js

## OpenGL Benchmarks

* Glxgears 
* [GLmark2](https://openbenchmarking.org/test/pts/glmark2)
* https://unigine.com/products/heaven/download/

## Wavefront OBJ Files

* [Format Description in Wikipedia](https://en.wikipedia.org/wiki/Wavefront_.obj_file)

## References

* [A collection of WebGL and WebGPU frameworks and libraries](https://gist.github.com/dmnsgn/76878ba6903cf15789b712464875cfdc)

