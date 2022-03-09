The HTML canvas is a two-dimensional grid.

The upper-left corner of the canvas has the coordinates (0,0)

In the previous chapter, you saw this method used: fillRect(0,0,150,75).

This means: Start at the upper-left corner (0,0) and draw a 150x75 pixels rectangle.
<h1>Example</h1>
<img src="https://i.imgur.com/eAWvqEI.jpg">
Coords: x,y
<h1>Draw a Line</h1>
To draw a straight line on a canvas, use the following methods:
<ul>
  <li>moveTo(x,y) - defines the starting point of the line.</li>
  <li>lineTo(x,y) - defines the ending point of the line.</li>
</ul>
To actually draw the line, you must use one of the "ink" methods, like stroke().
<pre>
var canvas = document.getElementById("myCanvas");
var ctx = canvas.getContext("2d");
ctx.moveTo(0, 0);
ctx.lineTo(200, 100);
ctx.stroke();
</pre>
<h1>Draw a Circle</h1>
To draw a circle on a canvas, use the following methods:

beginPath() - begins a path
arc(<i>x</i>, <i>y</i>, </i>r</i>, <i>startangle</i>, </i>endangle</i>) - creates an arc/curve. To create a circle with arc(): Set start angle to 0 and end angle to <code>2*Math.PI</code>. The x and y parameters define the x- and y-coordinates of the center of the circle. The r parameter defines the radius of the circle.
<pre>
var canvas = document.getElementById("myCanvas");
var ctx = canvas.getContext("2d");
ctx.beginPath();
ctx.arc(95, 50, 40, 0, 2 * Math.PI);
ctx.stroke();
</pre>
