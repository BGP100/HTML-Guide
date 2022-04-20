<a href="/JS/Graphics/Game/Canvas.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Graphics/Game/Controller.md">Next &gt;</a>
<hr>
Add a red square onto the game area:
<br>
<img src="https://i.imgur.com/uc7pjUB.jpg" width="40%">
<h1>Add a Component</h1>
Make a component constructor, which lets you add components onto the gamearea.
<br>
The object constructor is called component, and we make our first component, called <b>myGamePiece</b>:
<pre>
var myGamePiece;
function startGame() {
  myGameArea.start();
  myGamePiece = new component(30, 30, "red", 10, 120);
}
function component(width, height, color, x, y) {
  this.width = width;
  this.height = height;
  this.x = x;
  this.y = y; 
  ctx = myGameArea.context;
  ctx.fillStyle = color;
  ctx.fillRect(this.x, this.y, this.width, this.height);
}
</pre>
The components have properties and methods to control their appearances and movements.
<h1>Frames</h1>
To make the game ready for action, we will update the display 50 times per second, which is much like frames in a movie.
<br>
First, create a new function called <b>updateGameArea()</b>.
<br>
In the <b>myGameArea</b> object, add an interval which will run the <b>updateGameArea()</b> function every 20th millisecond (50 times per second). Also add a function called <b>clear()</b>, that clears the entire canvas.
<br>
In the <b>component</b> constructor, add a function called <b>update()</b>, to handle the drawing of the component.
<br>
The <b>updateGameArea()</b> function calls the <b>clear()</b> and the <b>update()</b> method.
<br>
The result is that the component is drawn and cleared 50 times per second:
<pre>
var myGameArea = {
  canvas : document.createElement("canvas"),
  start : function() {
    this.canvas.width = 480;
    this.canvas.height = 270;
    this.context = this.canvas.getContext("2d");
    document.body.insertBefore(this.canvas, document.body.childNodes[0]);
    this.interval = setInterval(updateGameArea, 20);
  },
  clear : function() {
    this.context.clearRect(0, 0, this.canvas.width, this.canvas.height);
  }
}
function component(width, height, color, x, y) {
  this.width = width;
  this.height = height;
  this.x = x;
  this.y = y; 
  this.update = function(){
    ctx = myGameArea.context;
    ctx.fillStyle = color;
    ctx.fillRect(this.x, this.y, this.width, this.height);
  }
}
function updateGameArea() {
  myGameArea.clear();
  myGamePiece.update();
}
</pre>
<h1>Make it Move</h1>
To prove that the red square is being drawn 50 times per second, we will change the x position (horizontal) by one pixel every time we update the game area:
<pre>
function updateGameArea() {
  myGameArea.clear();
  myGamePiece.x += 1;
  myGamePiece.update();
}
</pre>
<h1>Why Clear The Game Area?</h1>
It might seem unnecessary to clear the game area at every update. However, if we leave out the <b>clear()</b> method, all movements of the component will leave a trail of where it was positioned in the last frame:
<pre>
function updateGameArea() {
  // myGameArea.clear();
  myGamePiece.x += 1;
  myGamePiece.update();
}
</pre>
<h1>Change the Size</h1>
You can control the width and height of the component:
<pre>
function startGame() {
  myGameArea.start();
  myGamePiece = new component(140, 10, "red", 10, 120);
}
</pre>
<h1>Change the Color</h1>
You can control the color of the component:
<pre>
function startGame() {
  myGameArea.start();
  myGamePiece = new component(30, 30, "blue", 10, 120);
}
</pre>
You can also use other colorvalues like hex, rgb, or rgba:
<pre>
function startGame() {
  myGameArea.start();
  myGamePiece = new component(30, 30, "rgba(0, 0, 255, 0.5)", 10, 120);
}
</pre>
<h1>Change the Position</h1>
We use x- and y-coordinates to position components onto the game area.
<br>
The upper-left corner of the canvas has the coordinates (0,0)
<br>
Mouse over the game area below to see its x and y coordinates:
<img src="https://i.imgur.com/eAWvqEI.jpg" width="27%">
You can position the components wherever you like on the game area:
<pre>
function startGame() {
  myGameArea.start();
  myGamePiece = new component(30, 30, "red", 2, 2);
}
</pre>
<h1>Many Components</h1>
You can put as many components as you like on the game area:
<pre>
var redGamePiece, blueGamePiece, yellowGamePiece;
function startGame() {
  redGamePiece = new component(75, 75, "red", 10, 10);
  yellowGamePiece = new component(75, 75, "yellow", 50, 60); 
  blueGamePiece = new component(75, 75, "blue", 10, 110);
  myGameArea.start();
}
function updateGameArea() {
  myGameArea.clear();
  redGamePiece.update();
  yellowGamePiece.update(); 
  blueGamePiece.update();
}
</pre>
<h1>Moving Components</h1>
Make all three components move in different directions:
<pre>
function updateGameArea() {
  myGameArea.clear();
  redGamePiece.x += 1;
  yellowGamePiece.x += 1; 
  yellowGamePiece.y += 1; 
  blueGamePiece.x += 1; 
  blueGamePiece.y -= 1; 
  redGamePiece.update();
  yellowGamePiece.update(); 
  blueGamePiece.update();
}
</pre>
