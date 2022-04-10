<a href="/HTML/Graphics/Canvas/Coords.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/HTML/Graphics/Canvas/Text.md">Next &gt;</a>
<hr>
Gradients can be used to fill rectangles, circles, lines, text, etc. Shapes on the canvas are not limited to solid colors.
<br>
There are two different types of gradients:
<ul>
  <li>createLinearGradient(<i>x</i>,<i>y</i>,<i>x1</i>,<i>y1</i>) - creates a linear gradient</li>
  <li>createRadialGradient(<i>x</i>,<i>y</i>,<i>r</i>,<i>x1</i>,<i>y1</i>,<i>r1</i>) - creates a radial/circular gradient</li>
</ul>
Once we have a gradient object, we must add two or more color stops.
<br>
The <b>addColorStop()</b> method specifies the color stops, and its position along the gradient. Gradient positions can be anywhere between 0 to 1.
<br>
To use the gradient, set the <b>fillStyle</b> or <b>strokeStyle</b> property to the gradient, then draw the shape (rectangle, text, or a line).
<h1>Using createLinearGradient()</h1>
<img src="https://i.imgur.com/Esm2a0N.jpg" width="27%">
<pre>
var c = document.getElementById("myCanvas");
var ctx = c.getContext("2d");
// Create gradient
var grd = ctx.createLinearGradient(0, 0, 200, 0);
grd.addColorStop(0, "red");
grd.addColorStop(1, "white");
// Fill with gradient
ctx.fillStyle = grd;
ctx.fillRect(10, 10, 150, 80);
</pre>
<h1>Using createRadialGradient()</h1>
<img src="https://i.imgur.com/Vg0hqkU.jpg" width="27%">
<pre>
var c = document.getElementById("myCanvas");
var ctx = c.getContext("2d");
// Create gradient
var grd = ctx.createRadialGradient(75, 50, 5, 90, 60, 100);
grd.addColorStop(0, "red");
grd.addColorStop(1, "white");
// Fill with gradient
ctx.fillStyle = grd;
ctx.fillRect(10, 10, 150, 80);
</pre>
