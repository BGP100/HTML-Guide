<h1>How to Use'em?</h1>
To add images on a canvas, the <b>getContext("2d")</b> object has built-in image properties and methods.
<br>
In our game, to create the gamepiece as an image, use the component constructor, but instead of referring to a color, you must refer to the url of the image. And you must tell the constructor that this component is of type "image":
<pre>
function startGame() {
  myGamePiece = new component(30, 30, "smiley.gif", 10, 120, "image");
  myGameArea.start();
}
</pre>
In the component constructor we test if the component is of type "image", and create an image object by using the built-in "new Image()" object constructor. When we are ready to draw the image, we use the drawImage method instead of the fillRect method:
<pre>
function component(width, height, color, x, y, type) {
  this.type = type;
  if (type == "image") {
    this.image = new Image();
    this.image.src = color;
  }
  this.width = width;
  this.height = height;
  this.speedX = 0;
  this.speedY = 0;
  this.x = x;
  this.y = y;
  this.update = function() {
    ctx = myGameArea.context;
    if (type == "image") {
      ctx.drawImage(this.image,
        this.x,
        this.y,
        this.width, this.height);
    } else {
      ctx.fillStyle = color;
      ctx.fillRect(this.x, this.y, this.width, this.height);
    }
  }
}
</pre>
<h1>Change'em</h1>
You can change the image whenever you like by changing the src property of the image object of your component.
<br>
<img src="https://i.imgur.com/ixnaQfO.gif">
<br>
<img src="https://i.imgur.com/AfhF7be.gif">
If you want to change the smiley everytime it moves, change the image source when the user clicks a button, and back to normal when the button is not clicked:
<pre>
function move(dir) {
  myGamePiece.image.src = "angry.gif";
  if (dir == "up") {myGamePiece.speedY = -1; }
  if (dir == "down") {myGamePiece.speedY = 1; }
  if (dir == "left") {myGamePiece.speedX = -1; }
  if (dir == "right") {myGamePiece.speedX = 1; }
}
function clearmove() {
  myGamePiece.image.src = "smiley.gif";
  myGamePiece.speedX = 0;
  myGamePiece.speedY = 0;
}
</pre>
<h1>Background Images</h1>
Add a background image to your game area by adding it as a component, and also update the background in every frame:
<pre>
var myGamePiece;
var myBackground;
function startGame() {
  myGamePiece = new component(30, 30, "smiley.gif", 10, 120, "image");
  myBackground = new component(656, 270, "citymarket.jpg", 0, 0, "image");
  myGameArea.start();
}
function updateGameArea() {
  myGameArea.clear();
  myBackground.newPos();
  myBackground.update();
  myGamePiece.newPos();
  myGamePiece.update();
}
</pre>
<h1>Moving Background</h1>
Change the background component's <b>speedX</b> property to make the background move:
<pre>
function updateGameArea() {
  myGameArea.clear();
  myBackground.speedX = -1;
  myBackground.newPos();
  myBackground.update();
  myGamePiece.newPos();
  myGamePiece.update();
}
</pre>
<h1>Background Loop</h1>
To make the same background loop forever, we must use a specific technique.
<br>
Start by telling the component constructor that this is a <i>background</i>. The component constructor will then add the image twice, placing the second image immediately after the first image.
<br>
In the <b>newPos()</b> method, check if the <b>x</b> position of the component has reach the end of the image, if it has, set the <b>x</b> position of the component to 0:
<pre>
function component(width, height, color, x, y, type) {
  this.type = type;
  if (type == "image" || type == "background") {
    this.image = new Image();
    this.image.src = color;
  }
  this.width = width;
  this.height = height;
  this.speedX = 0;
  this.speedY = 0;
  this.x = x;
  this.y = y;
  this.update = function() {
    ctx = myGameArea.context;
    if (type == "image" || type == "background") {
      ctx.drawImage(this.image, this.x, this.y, this.width, this.height);
      if (type == "background") {
        ctx.drawImage(this.image, this.x + this.width, this.y, this.width, this.height);
      }
    } else {
      ctx.fillStyle = color;
      ctx.fillRect(this.x, this.y, this.width, this.height);
    }
  }
  this.newPos = function() {
    this.x += this.speedX;
    this.y += this.speedY;
    if (this.type == "background") {
      if (this.x == -(this.width)) {
        this.x = 0;
      }
    }
  }
}
</pre>
