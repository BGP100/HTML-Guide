<a href="/JS/Graphics/Game/Gravity.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Graphics/Game/Rotation.md">Next &gt;</a>
<hr>
Another functionallity we want to add is the <b>bounce</b> property.
<br>
The <b>bounce</b> property indicates if the component will <b>bounce</b> back when gravity makes it fall down to the ground.
<br>
The <b>bounce</b> property value must be a number. 0 is no bounce at all, and 1 will make the component <b>bounce</b> all the way backto where it start falling.
<pre>
function component(width, height, color, x, y, type) {
  this.type = type;
  this.width = width;
  this.height = height;
  this.x = x;
  this.y = y;
  this.speedX = 0;
  this.speedY = 0;
  this.gravity = 0.1;
  this.gravitySpeed = 0;
  this.bounce = 0.6;
  this.update = function() {
    ctx = myGameArea.context;
    ctx.fillStyle = color;
    ctx.fillRect(this.x, this.y, this.width, this.height);
  }
  this.newPos = function() {
    this.gravitySpeed += this.gravity;
    this.x += this.speedX;
    this.y += this.speedY + this.gravitySpeed;
    this.hitBottom();
  }
  this.hitBottom = function() {
    var rockbottom = this.gamearea.canvas.height - this.height;
    if (this.y > rockbottom) {
      this.y = rockbottom;
      this.gravitySpeed = -(this.gravitySpeed * this.bounce);
    }
  }
}
</pre>
