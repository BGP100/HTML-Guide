<a href="/JS/Graphics/Canvas/Gradients.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Graphics/Canvas/Images.md">Next &gt;</a>
<hr>
To draw text on a canvas, the most important property and methods are:
<ul>
  <li><b>font</b> - defines the font properties for the text.</li>
  <li><b>fillText(text,x,y)</b> - draws "filled" text on the canvas.</li>
  <li><b>strokeText(text,x,y)</b> - draws text on the canvas (no fill).</li>
</ul>
<h1>Using fillText()</h1>
<img src="https://i.imgur.com/UkjXVQA.jpg" width="20%">
<pre>
var canvas = document.getElementById("myCanvas");
var ctx = canvas.getContext("2d");
ctx.font = "30px Arial";
ctx.fillText("Hello World", 10, 50);
</pre>
<h1>Using strokeText()</h1>
<img src="https://i.imgur.com/UCaNPsb.jpg" width="20%">
<pre>
var canvas = document.getElementById("myCanvas");
var ctx = canvas.getContext("2d");
ctx.font = "30px Arial";
ctx.fillText("Hello World", 10, 50);
</pre>
<h1>Change Text's Values</h1>
<img src="https://i.imgur.com/L1Fotz8.jpg" width="30%">
<pre>
var canvas = document.getElementById("myCanvas");
var ctx = canvas.getContext("2d");
ctx.font = "30px Arial";
ctx.strokeText("Hello World", 10, 50);
</pre>
