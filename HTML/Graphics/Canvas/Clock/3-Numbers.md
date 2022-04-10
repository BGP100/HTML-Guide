<a href="/HTML/Graphics/Canvas/Clock/2-Face.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/HTML/Graphics/Canvas/Clock/4-Hands.md">Next &gt;</a>
<hr>
<h1>Part III - Draw Clock Numbers</h1>
The clock needs numbers. Create a JavaScript function to draw clock numbers:
<img src="https://i.imgur.com/kNyWl4Z.jpg" width="40%">
<h1>Code</h1>
Set the font size (of the drawing object) to 15% of the radius:
<pre>ctx.font = radius * 0.15 + "px arial";</pre>
Set the text alignment to the middle and the center of the print position:
<pre>
ctx.textBaseline = "middle";
ctx.textAlign = "center";
</pre>
Calculate the print position (for 12 numbers) to 85% of the radius, rotated (PI/6) for each number:
<pre>
for(num = 1; num < 13; num++) {
  ang = num * Math.PI / 6;
  ctx.rotate(ang);
  ctx.translate(0, -radius * 0.85);
  ctx.rotate(-ang);
  ctx.fillText(num.toString(), 0, 0);
  ctx.rotate(ang);
  ctx.translate(0, radius * 0.85);
  ctx.rotate(-ang); 
}
</pre>
<h2>All the Code Joined in One</h2>
<pre>
function drawClock() {
  drawFace(ctx, radius);
  drawNumbers(ctx, radius);
}
function drawNumbers(ctx, radius) {
  var ang;
  var num;
  ctx.font = radius * 0.15 + "px arial";
  ctx.textBaseline = "middle";
  ctx.textAlign = "center";
  for(num = 1; num < 13; num++){
    ang = num * Math.PI / 6;
    ctx.rotate(ang);
    ctx.translate(0, -radius * 0.85);
    ctx.rotate(-ang);
    ctx.fillText(num.toString(), 0, 0);
    ctx.rotate(ang);
    ctx.translate(0, radius * 0.85);
    ctx.rotate(-ang);
  }
}
</pre>
