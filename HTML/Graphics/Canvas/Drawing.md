All drawing on the HTML canvas must be done with JavaScript:
<pre>
var canvas = document.getElementById("myCanvas");
var ctx = canvas.getContext("2d");
ctx.fillStyle = "#FF0000";
ctx.fillRect(0, 0, 150, 75);
</pre>
<h1>Step 1: Find the Element</h1>
First of all, you must find the <b>&lt;canvas&gt;</b> element.
<br>
This is done by using the HTML DOM method <b>getElementById()</b>:
<pre>var canvas = document.getElementById("myCanvas");</pre>
<h1>Step 2: Create a Drawing Object</h1>
Secondly, you need a drawing object for the canvas.
<br>
The <b>getContext()</b> is a built-in HTML object, with properties and methods for drawing:
<pre>var ctx = canvas.getContext("2d");</pre>
<h1>Step 3: Draw on the Canvas</h1>
Finally, you can draw on the canvas.
<br>
Set the fill style of the drawing object to the color red:
<pre>ctx.fillStyle = "#FF0000";</pre>
The fillStyle property can be a CSS color, a gradient, or a pattern. The default fillStyle is black.
<br>
The fillRect(<i>x</i>, <i>y</i>, <i>width</i>, <i>height</i>) method draws a rectangle, filled with the fill style, on the canvas:
<pre>ctx.fillRect(0, 0, 150, 75);</pre>
