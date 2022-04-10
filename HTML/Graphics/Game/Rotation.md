<a href="/HTML/Graphics/Game/Bouncing.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/HTML/Graphics/Game/Movement.md">Next &gt;</a>
<hr>
Earlier in this tutorial, the red square was able to move around on the gamearea, but it could not turn or rotate.
<br>
To rotate components, we have to change the way we draw components.
<br>
The only rotation method available for the canvas element will rotate the entire canvas:
<br>
<img src="https://i.imgur.com/BS3lX6B.png">
<br>
Everything else you draw on the canvas will also be rotated, not only the specific component.
<br>
That is why we have to make some changes in the <b>update()</b> method:
<br>
First, we save the current canvas context object:
<br>
<b>ctx.save();</b>
<br>
Then we move the entire canvas to the center of the specific component, using the translate method:
<br>
<b>ctx.translate(x, y);</b>
<br>
<img src="https://i.imgur.com/4UD70yW.png">
<br>
Then we perform the wanted rotation using the rotate() method:
<br>
<b>ctx.rotate(angle);</b>
<br>
<img src="https://i.imgur.com/NKKo6lU.png">
<br>
Now we are ready to draw the component onto the canvas, but now we will draw it with its center position at position 0,0 on the translated (and rotated) canvas:
<br>
<b>ctx.fillRect(width / -2, height / -2, width, height);</b>
<br>
<img src="https://i.imgur.com/T9PFBc7.png">
<br>
When we are finished, we must restore the context object back to its saved position, using the restore method:
<br>
ctx.restore();
<br>
The component is the only thing that is rotated:
<br>
<img src="https://i.imgur.com/NWP0DHb.png">
<h1>The Component Constructor</h1>
The <b>component</b> constructor has a new property called <b>angle</b>, which is radian number that represents the angle of the component.
<br>
The <b>update</b> method of the <b>component</b> constructor is were we draw the component, and here you can see the changes that will allow the component to rotate:
<pre>
function component(width, height, color, x, y) {
  this.width = width;
  this.height = height;
  this.angle = 0;
  this.x = x;
  this.y = y;
  this.update = function() {
    ctx = myGameArea.context;
    ctx.save();
    ctx.translate(this.x, this.y);
    ctx.rotate(this.angle);
    ctx.fillStyle = color;
    ctx.fillRect(this.width / -2, this.height / -2, this.width, this.height);
    ctx.restore();
  }
}
function updateGameArea() {
  myGameArea.clear();
  myGamePiece.angle += 1 * Math.PI / 180;
  myGamePiece.update();
}
</pre>
