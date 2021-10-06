## Creating 3D Models and Animations

Eventually I hope to offer recommendations for creating 3D illustrations
and simple animations for use in instruction. For now I am collecting
information on this page.

## X3D Format Documentation

X3D and its predecessor VRML (Virtual Reality Markup Language) are file
formats for 3D scenes to be displayed in web browsers.

* [X3D Resources](https://www.web3d.org/x3d/content/examples/X3dResources.html)
* [X3D Scene Authoring Hints](http://x3dgraphics.com/examples/X3dSceneAuthoringHints.html)
* [Phong Reflection Model](https://en.wikipedia.org/wiki/Phong_reflection_model)

## Software For Creating VRML/X3D Scenes

* [Blender](https://www.blender.org) --
	Full-featured 3D modeling system. Can import and export in numberous
	formats including X3D.
* [Art of Illusion](http://www.artofillusion.org) --
	Fairly capable 3D modeling system written in Java. Can export in OBJ
	and VRML format.
* [Titania](https://github.com/create3000/titania/wiki) --
	As of 2021 the project as active and moving to Github. A few nits though:
	Snap package is 4.6.9 from December 2019. Though it works on Ubuntu 20.04,
	it suffers from long pauses. The oldest release is marked as the newest.
	Titania uses X\_ITE as the viewer.
* [White Dune](http://wdune.ourproject.org/) --
	Attempt to run on version 1.956 on Ubuntu 20.04 failed.
* [X3D-Edit](https://savage.nps.edu/X3D-Edit/) --
	Appears to be an XML editor for X3D with preview. Written in Java.
	Uses an X3D viewer called Xj3D which is also written in Java.
	(The Xj3D.org website is now a programming news site.)
	As of 2021 website looks dated. Last stable release (4.0) in 2019.
	On Ubuntu 20.04 it throws up warnings when started, crashes.
* [X3DOM Component Editor](https://github.com/x3dom/component-editor) --
	Very basic web scene editor

## Other 3D Editors

* [Maverick Model 3D](https://github.com/zturtleman/mm3d)
* [K-3D](http://www.k-3d.org/)
* [Wings 3D](http://www.wings3d.com/) --
	A "subdivision modeler", whatever that means. Site seems to indicate it
	can create mesh models and add materials. Says there is no support for
	animation.
* [FreeCAD](https://www.freecadweb.org/)
* [BRL-CAD](https://brlcad.org/)

## For displaying 3D Scenes, Animation, and Games in Web Browsers

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
	Game engine written in C++ with scripted in Python.
	Updated website around 2021. Can now load many model formats.
	See this [3D file viewer example](https://github.com/trueprice/python-video-tool).

## Other Animation Tools

* [Monster Mash](https://ai.googleblog.com/2021/04/monster-mash-sketch-based-tool-for.html) --
	Quickly creates crude 3D models by "inflating" 2D outlines drawn by hand	
* [Armory3D](https://armory3d.org/) --
	3D engine, texture tools
* [Maverick Model 3D](https://github.com/zturtleman/mm3d) --
	Model editor
* [MB-Lab](https://github.com/animate1978/MB-Lab) --
	Character creator
* [MeshLab](https://www.meshlab.net/) --
	System for processing and editing 3D triangular meshes
* [PyMesh — Geometry Processing Library for Python](https://pymesh.readthedocs.io/en/latest/) --
	Mesh processing routines. Described on the site as a unified
	inteface to a number of other tools. I do not really understand
	the purpose of the processing functions described, but they sound
	like they are for simplification and cleanup. 

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

## Other Lists

* [A collection of WebGL and WebGPU frameworks and libraries](https://gist.github.com/dmnsgn/76878ba6903cf15789b712464875cfdc)

