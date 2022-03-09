To add this functionality to our component constructor, first add a gravity property, which sets the current gravity. Then add a gravitySpeed property, which increases everytime we update the frame:
<pre>
function component(width, height, color, x, y, type) {
  this.type = type;
  this.width = width;
  this.height = height;
  this.x = x;
  this.y = y;
  this.speedX = 0;
  this.speedY = 0;
  this.gravity = 0.05;
  this.gravitySpeed = 0;
  this.update = function() {
    ctx = myGameArea.context;
    ctx.fillStyle = color;
    ctx.fillRect(this.x, this.y, this.width, this.height);
  }
  this.newPos = function() {
    this.gravitySpeed += this.gravity;
    this.x += this.speedX;
    this.y += this.speedY + this.gravitySpeed;
  }
}
</pre>
<h1>Hit the Bottom</h1>
To prevent the red square from falling outside of the canvas, stop the falling when it hits the bottom of the game area:
<pre>
this.newPos = function() {
  this.gravitySpeed += this.gravity;
  this.x += this.speedX;
  this.y += this.speedY + this.gravitySpeed;
  this.hitBottom();
}
this.hitBottom = function() {
  var rockbottom = myGameArea.canvas.height - this.height;
  if (this.y > rockbottom) {
    this.y = rockbottom;
  }
}
</pre>
<h1>Accelerate</h1>
In a game, when you have a force that pulls you down, you should have a method to force the component to accelerate up.
<br>
Trigger a function when someone clicks a button, and make the red square fly up in the air:
<pre>
&lt;script&gt;
function accelerate(n) {
  myGamePiece.gravity = n;
}
&lt;/script&gt;
&lt;button onmousedown="accelerate(-0.2)" onmouseup="accelerate(0.1)"&gt;ACCELERATE&lt;/button&gt;
</pre>
