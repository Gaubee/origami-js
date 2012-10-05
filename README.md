origami-js
==========

###Raphael-based 3D micro-library

Usage:

	origami = new Origami("paperplane", 90, 60);

	function paperplane(){
		var scale=0.4;
		var midspan = 20*scale;
		var depth = 20*scale;
		var length= 70*scale;
		var wingspan = 100*scale;
		origami.face({x: -wingspan, y:-length, z:depth},{x: -midspan, y:-length, z:depth},{x:0, y:length, z:depth},200); 
		origami.face({x: wingspan, y:-length, z:depth},{x:0, y:length, z:depth},{x:midspan, y:-length, z:depth},200);
		origami.face({x: -midspan, y:-length, z:depth},{x:0, y:length, z:depth},{x:0, y:-length, z:-depth},200); 
		origami.face({x: midspan, y:-length, z:depth},{x:0, y:-length, z:-depth},{x:0, y:length, z:depth},200); 
	}
	
	origami.camera.setAngles(1.0,-2.5);
	origami.camera.cull = false;
	paperplane();



> **Copyright (C) 2012 Leszek Rybicki**

> Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

> The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

> THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.