In these chapters I will build an analog clock using HTML canvas.
<h1>Part I: Create the Canvas</h1>
<img src="https://i.imgur.com/O8zlGN8.jpg" width="40%">
<h1>Code</h1>
Add an HTML <b>&lt;canvas&gt;</b> element to your page:
<pre>&lt;canvas id="canvas" width="400" height="400" style="background-color:#333"&gt;&lt;/canvas&gt;</pre>
Create a canvas object (var canvas for example) from the HTML canvas element:
<pre>var canvas = document.getElementById("canvas");</pre>
Create a 2d drawing object (var ctx) for the canvas object:
<pre>var ctx = canvas.getContext("2d");</pre>
Calculate the clock radius, using the height of the canvas:
<pre>var radius = canvas.height / 2;</pre>
Remap the (0,0) position (of the drawing object) to the center of the canvas:
<pre>ctx.translate(radius, radius);</pre>
Reduce the clock radius (to 90%) to draw the clock well inside the canvas:
<pre>radius = radius * 0.90;</pre>
Create a function to draw the clock:
<pre>
function drawClock() {
  ctx.arc(0, 0, radius, 0 , 2 * Math.PI);
  ctx.fillStyle = "white";
  ctx.fill();
}
</pre>
<h2>All the Code Joined in One</h2>
<pre>
&lt;canvas id="canvas" width="400" height="400" style="background-color:#333"&gt;&lt;/canvas&gt;
&lt;script&gt;
var canvas = document.getElementById("canvas");
var ctx = canvas.getContext("2d");
var radius = canvas.height / 2;
ctx.translate(radius, radius);
radius = radius * 0.90
drawClock();
function drawClock() {
  ctx.arc(0, 0, radius, 0 , 2 * Math.PI);
  ctx.fillStyle = "white";
  ctx.fill();
}
&lt;/script&gt;
</pre>
