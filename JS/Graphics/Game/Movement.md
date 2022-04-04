Add a <b>speed</b> property to the <b>component</b> constructor, which represents the current speed of the component.
<br>
Also make some changes in the <b>newPos()</b> method, to calculate the position of the component, based on <b>speed</b> and <b>angle</b>.
<br>
By default, the components are facing up, and by setting the speed property to 1, the component will start moving forward.
<pre>
function component(width, height, color, x, y) {
  this.gamearea = gamearea;
  this.width = width;
  this.height = height;
  this.angle = 0;
  this.speed = 1;
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
  this.newPos = function() {
    this.x += this.speed * Math.sin(this.angle);
    this.y -= this.speed * Math.cos(this.angle);
  }
}
</pre>
<h1>Turning</h1>
We also want to be able to make left and right turns. Make a new property called moveAngle, which indicates the current moving value, or rotation angle. In the newPos() method calculate the angle based on the moveAngle property:
<pre>
function component(width, height, color, x, y) {
  this.width = width;
  this.height = height;
  this.angle = 0;
  this.moveAngle = 1;
  this.speed = 1;
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
  this.newPos = function() {
    this.angle += this.moveAngle * Math.PI / 180;
    this.x += this.speed * Math.sin(this.angle);
    this.y -= this.speed * Math.cos(this.angle);
  }
}
</pre>
<h1>Use the Keyboard</h1>
How does the red square move when using the keyboard? Instead of moving up and down, and from side to side, the red square moves forward when you use the "up" arrow, and turns left and right when pressing the left and right arrows.
