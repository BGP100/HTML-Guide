<h1>Part II - Draw a Clock Face</h1>
The clock needs a clock face. Create a JavaScript function to draw a clock face:
<img src="https://i.imgur.com/DLxokQJ.jpg" width="40%">
<h1>Code</h1>
Create a drawFace() function for drawing the clock face:
<pre>
function drawClock() {
  drawFace(ctx, radius);
}
function drawFace(ctx, radius) {
}
</pre>
Draw the white circle:
<pre>
ctx.beginPath();
ctx.arc(0, 0, radius, 0, 2 * Math.PI);
ctx.fillStyle = 'white';
ctx.fill();
</pre>
Create a radial gradient (95% and 105% of original clock radius):
<pre>grad = ctx.createRadialGradient(0, 0, radius * 0.95, 0, 0, radius * 1.05);</pre>
Create 3 color stops, corresponding with the inner, middle, and outer edge of the arc:
<pre>
grad.addColorStop(0, '#333');
grad.addColorStop(0.5, 'white');
grad.addColorStop(1, '#333');
</pre>
Define the gradient as the stroke style of the drawing object:
<pre>ctx.strokeStyle = grad;</pre>
Define the line width of the drawing object (10% of radius):
<pre>ctx.lineWidth = radius * 0.1;</pre>
Draw the circle:
<pre>ctx.stroke();</pre>
Draw the clock center:
<pre>
ctx.beginPath();
ctx.arc(0, 0, radius * 0.1, 0, 2 * Math.PI);
ctx.fillStyle = '#333';
ctx.fill();
</pre>
<h2>All the Code Joined in One</h2>
<pre>
function drawClock() {
  drawFace(ctx, radius);
}
function drawFace(ctx, radius) {
  var grad;
  ctx.beginPath();
  ctx.arc(0, 0, radius, 0, 2 * Math.PI);
  ctx.fillStyle = 'white';
  ctx.fill();
  grad = ctx.createRadialGradient(0, 0 ,radius * 0.95, 0, 0, radius * 1.05);
  grad.addColorStop(0, '#333');
  grad.addColorStop(0.5, 'white');
  grad.addColorStop(1, '#333');
  ctx.strokeStyle = grad;
  ctx.lineWidth = radius*0.1;
  ctx.stroke();
  ctx.beginPath();
  ctx.arc(0, 0, radius * 0.1, 0, 2 * Math.PI);
  ctx.fillStyle = '#333';
  ctx.fill();
}
</pre>
