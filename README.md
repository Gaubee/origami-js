origami-js
==========

###Raphael-based 3D micro-library

Origami generates 2D vector images that are projections of 3D objects defined by flat surfaces (thus: origami). Origami is very lightweight and works on browsers that don't support HTML5 CANVAS tags.

For really advanced 3D in Javascript, see [Three.js](http://mrdoob.github.com/three.js/). 

###Dependencies

Uses [Raphaël](raphaeljs.com) for rendering SVG/VML.

###Usage:

	origami = new Origami("paperplane", 90, 60);

	function paperplane(scale){
		scale=scale || 0.4;
		var midspan = 20*scale;
		var depth = 20*scale;
		var length= 70*scale;
		var wingspan = 100*scale;
		origami.face({x: -wingspan, y:-length, z:depth},
		            {x: -midspan, y:-length, z:depth},
		            {x:0, y:length, z:depth},200); 
		origami.face({x: wingspan, y:-length, z:depth},
		            {x:0, y:length, z:depth},
		            {x:midspan, y:-length, z:depth},200);
		origami.face({x: -midspan, y:-length, z:depth},
		            {x:0, y:length, z:depth},
		            {x:0, y:-length, z:-depth},200); 
		origami.face({x: midspan, y:-length, z:depth},
		            {x:0, y:-length, z:-depth},
		            {x:0, y:length, z:depth},200); 
	}
	
	origami.camera.setAngles(1.0,-2.5);
	origami.camera.cull = false;
	paperplane();

###TODO: 

- quad faces,
- lines, points
- light position (currently: the camera is the light source)
- objects - grouped faces
- a real documentation

### Legal stuff

> **Copyright (C) 2012 Leszek Rybicki**

> Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

> The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

> THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.