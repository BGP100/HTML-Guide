<a href="/JS/Graphics/Game/Components.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Graphics/Game/Obstacles.md">Next &gt;</a>
<hr>
Push the buttons to move the red square:
<br>
<sup>(It's just an image, GitHub does not support these things...)</sup>
<br>
<img src="https://i.imgur.com/su4lzbA.jpg" width="40%">
<h1>Get it</h1>
Now we want to control the red square.
<br>
Add four buttons, up, down, left, and right.
<br>
Write a function for each button to move the component in the selected direction.
<br>
Make two new properties in the <b>component</b> constructor, and call them <b>speedX</b> and <b>speedY</b>. These properties are being used as speed indicators.
<br>
Add a function in the <b>component</b> constructor, called <b>newPos()</b>, which uses the <b>speedX</b> and <b>speedY</b> properties to change the component's position.
<br>
The newpos function is called from the updateGameArea function before drawing the component:
<pre>
&lt;script&gt;
function component(width, height, color, x, y) {
  this.width = width;
  this.height = height;
  this.speedX = 0;
  this.speedY = 0;
  this.x = x;
  this.y = y;
  this.update = function() {
    ctx = myGameArea.context;
    ctx.fillStyle = color;
    ctx.fillRect(this.x, this.y, this.width, this.height);
  }
  this.newPos = function() {
    this.x += this.speedX;
    this.y += this.speedY;
  }
}
function updateGameArea() {
  myGameArea.clear();
  myGamePiece.newPos();
  myGamePiece.update();
}
function moveup() {
  myGamePiece.speedY -= 1;
}
function movedown() {
  myGamePiece.speedY += 1;
}
function moveleft() {
  myGamePiece.speedX -= 1;
}
function moveright() {
  myGamePiece.speedX += 1;
}
&lt;/script&gt;
&lt;button onclick="moveup()"&gt;UP&lt;/button&gt;
&lt;button onclick="movedown()"&gt;DOWN&lt;/button&gt;
&lt;button onclick="moveleft()"&gt;LEFT&lt;/button&gt;
&lt;button onclick="moveright()"&gt;RIGHT&lt;/button&gt;
</pre>
<h1>Stop Moving</h1>
If you want, you can make the red square stop when you release a button.
<br>
Add a function that will set the speed indicators to 0.
<br>
To deal with both normal screens and touch screens, we will add code for both devices:
<pre>
function stopMove() {
  myGamePiece.speedX = 0;
  myGamePiece.speedY = 0;
}
</pre>
<pre>
&lt;button onmousedown="moveup()" <b>onmouseup="stopMove()" ontouchstart="moveup()"</b>&gt;UP&lt;/button&gt;
&lt;button onmousedown="movedown()" <b>onmouseup="stopMove()" ontouchstart="movedown()"</b>&gt;DOWN&lt;/button&gt;
&lt;button onmousedown="moveleft()" <b>onmouseup="stopMove()" ontouchstart="moveleft()"</b>&gt;LEFT&lt;/button&gt;
&lt;button onmousedown="moveright()" <b>onmouseup="stopMove()" ontouchstart="moveright()"</b>&gt;RIGHT&lt;/button&gt;
</pre>
<h1>Keyboard as Controller</h1>
We can also control the red square by using the arrow keys on the keyboard.
<br>
Create a method that checks if a key is pressed, and set the <b>key</b> property of the <b>myGameArea</b> object to the key code. When the key is released, set the <b>key</b> property to <b>false</b>:
<pre>
var myGameArea = {
  canvas : document.createElement("canvas"),
  start : function() {
    this.canvas.width = 480;
    this.canvas.height = 270;
    this.context = this.canvas.getContext("2d");
    document.body.insertBefore(this.canvas, document.body.childNodes[0]);
    this.interval = setInterval(updateGameArea, 20);
    window.addEventListener('keydown', function (e) {
      myGameArea.key = e.keyCode;
    })
    window.addEventListener('keyup', function (e) {
      myGameArea.key = false;
    })
  },
  clear : function(){
    this.context.clearRect(0, 0, this.canvas.width, this.canvas.height);
  }
}
</pre>
Then we can move the red square if one of the arrow keys are pressed:
<pre>
function updateGameArea() {
  myGameArea.clear();
  myGamePiece.speedX = 0;
  myGamePiece.speedY = 0;
  if (myGameArea.key && myGameArea.key == 37) {myGamePiece.speedX = -1; }
  if (myGameArea.key && myGameArea.key == 39) {myGamePiece.speedX = 1; }
  if (myGameArea.key && myGameArea.key == 38) {myGamePiece.speedY = -1; }
  if (myGameArea.key && myGameArea.key == 40) {myGamePiece.speedY = 1; }
  myGamePiece.newPos();
  myGamePiece.update();
}
</pre>
<h1>Multiple Pressing</h1>
What if more than one key is pressed at the same time?
<br>
In the example above, the component can only move horizontally or vertically. Now we want the component to also move diagonally.
<br>
Create a <b>keys</b> array for the <b>myGameArea</b> object, and insert one element for each key that is pressed, and give it the value <b>true</b>, the value remains true untill the key is no longer pressed, the value becomes <b>false</b> in the keyup event listener function:
<pre>
var myGameArea = {
  canvas : document.createElement("canvas"),
  start : function() {
    this.canvas.width = 480;
    this.canvas.height = 270;
    this.context = this.canvas.getContext("2d");
    document.body.insertBefore(this.canvas, document.body.childNodes[0]);
    this.interval = setInterval(updateGameArea, 20);
    window.addEventListener('keydown', function (e) {
      myGameArea.keys = (myGameArea.keys || []);
      myGameArea.keys[e.keyCode] = true;
    })
    window.addEventListener('keyup', function (e) {
      myGameArea.keys[e.keyCode] = false;
    })
  },
  clear : function(){
    this.context.clearRect(0, 0, this.canvas.width, this.canvas.height);
  }
}
</pre>
<h1>Using The Mouse Cursor as a Controller</h1>
If you want to control the red square by using the mouse cursor, add a method in myGameArea object that updates the x and y coordinates of the mouse cursor:
<pre>
var myGameArea = {
  canvas : document.createElement("canvas"),
  start : function() {
    this.canvas.width = 480;
    this.canvas.height = 270;
    this.canvas.style.cursor = "none"; //hide the original cursor
    this.context = this.canvas.getContext("2d");
    document.body.insertBefore(this.canvas, document.body.childNodes[0]);
    this.interval = setInterval(updateGameArea, 20);
    window.addEventListener('mousemove', function (e) {
      myGameArea.x = e.pageX;
      myGameArea.y = e.pageY;
    })
  },
  clear : function(){
    this.context.clearRect(0, 0, this.canvas.width, this.canvas.height);
  }
}
</pre>
Then we can move the red square using the mouse cursor:
<pre>
function updateGameArea() {
  myGameArea.clear();
  if (myGameArea.x && myGameArea.y) {
    myGamePiece.x = myGameArea.x;
    myGamePiece.y = myGameArea.y;
  }
  myGamePiece.update();
}
</pre>
<h1>Touch The Screen to Control The Game</h1>
We can also control the red square on a touch screen.
<br>
Add a method in the <b>myGameArea</b> object that uses the x and y coordinates of where the screen is touched:
<pre>
var myGameArea = {
  canvas : document.createElement("canvas"),
  start : function() {
    this.canvas.width = 480;
    this.canvas.height = 270;
    this.context = this.canvas.getContext("2d");
    document.body.insertBefore(this.canvas, document.body.childNodes[0]);
    this.interval = setInterval(updateGameArea, 20);
    window.addEventListener('touchmove', function (e) {
      myGameArea.x = e.touches[0].screenX;
      myGameArea.y = e.touches[0].screenY;
    })
  },
  clear : function(){
    this.context.clearRect(0, 0, this.canvas.width, this.canvas.height);
  }
}
</pre>
Then we can move the red square if the user touches the screen, by using the same code as we did for the mouse cursor:
<pre>
function updateGameArea() {
  myGameArea.clear();
  if (myGameArea.x && myGameArea.y) {
    myGamePiece.x = myGameArea.x;
    myGamePiece.y = myGameArea.y;
  }
  myGamePiece.update();
}
</pre>
<h1>Controllers on The Canvas</h1>
We can also draw our own buttons on the canvas, and use them as controllers:
<pre>
function startGame() {
  myGamePiece = new component(30, 30, "red", 10, 120);
  myUpBtn = new component(30, 30, "blue", 50, 10);
  myDownBtn = new component(30, 30, "blue", 50, 70);
  myLeftBtn = new component(30, 30, "blue", 20, 40);
  myRightBtn = new component(30, 30, "blue", 80, 40);
  myGameArea.start();
}
</pre>
Add a new function that figures out if a component, in this case a button, is clicked.
<br>
Start by adding event listeners to check if a mouse button is clicked (<b>mousedown</b> and <b>mouseup</b>). To deal with touch screens, also add event listeners to check if the screen is clicked on (<b>touchstart</b> and <b>touchend</b>):
<pre>
var myGameArea = {
  canvas : document.createElement("canvas"),
  start : function() {
    this.canvas.width = 480;
    this.canvas.height = 270;
    this.context = this.canvas.getContext("2d");
    document.body.insertBefore(this.canvas, document.body.childNodes[0]);
    this.interval = setInterval(updateGameArea, 20);
    window.addEventListener('mousedown', function (e) {
      myGameArea.x = e.pageX;
      myGameArea.y = e.pageY;
    })
    window.addEventListener('mouseup', function (e) {
      myGameArea.x = false;
      myGameArea.y = false;
    })
    window.addEventListener('touchstart', function (e) {
      myGameArea.x = e.pageX;
      myGameArea.y = e.pageY;
    })
    window.addEventListener('touchend', function (e) {
      myGameArea.x = false;
      myGameArea.y = false;
    })
  },
  clear : function(){
    this.context.clearRect(0, 0, this.canvas.width, this.canvas.height);
  }
}
</pre>
Now the <b>myGameArea</b> object has properties that tells us the x- and y-coordinates of a click. We use these properties to check if the click was performed on one of our blue buttons.
<br>
The new method is called <b>clicked</b>, it is a method of the <b>component</b> constructor, and it checks if the component is being clicked.
<br>
In the <b>updateGameArea</b> function, we take the neccessarry actions if one of the blue buttons is clicked:
<pre>
function component(width, height, color, x, y) {
  this.width = width;
  this.height = height;
  this.speedX = 0;
  this.speedY = 0;
  this.x = x;
  this.y = y;
  this.update = function() {
    ctx = myGameArea.context;
    ctx.fillStyle = color;
    ctx.fillRect(this.x, this.y, this.width, this.height);
  }
  this.clicked = function() {
    var myleft = this.x;
    var myright = this.x + (this.width);
    var mytop = this.y;
    var mybottom = this.y + (this.height);
    var clicked = true;
    if ((mybottom < myGameArea.y) || (mytop > myGameArea.y) || (myright < myGameArea.x) || (myleft > myGameArea.x)) {
      clicked = false;
    }
    return clicked;
  }
}
function updateGameArea() {
  myGameArea.clear();
  if (myGameArea.x && myGameArea.y) {
    if (myUpBtn.clicked()) {
      myGamePiece.y -= 1;
    }
    if (myDownBtn.clicked()) {
      myGamePiece.y += 1;
    }
    if (myLeftBtn.clicked()) {
      myGamePiece.x += -1;
    }
    if (myRightBtn.clicked()) {
      myGamePiece.x += 1;
    }
  }
  myUpBtn.update();
  myDownBtn.update();
  myLeftBtn.update();
  myRightBtn.update();
  myGamePiece.update();
}
</pre>
<h1>All the Code Joined in One</h1>
<pre>
&lt;script&gt;
var myGameArea = {
  canvas : document.createElement("canvas"),
  start : function() {
    this.canvas.width = 480;
    this.canvas.height = 270;
    this.canvas.style.cursor = "none"; //hide the original cursor
    this.context = this.canvas.getContext("2d");
    document.body.insertBefore(this.canvas, document.body.childNodes[0]);
    this.interval = setInterval(updateGameArea, 20);
    window.addEventListener('mousemove', function (e) {
      myGameArea.x = e.pageX;
      myGameArea.y = e.pageY;
    })
  },
  clear : function(){
    this.context.clearRect(0, 0, this.canvas.width, this.canvas.height);
  }
}
function component(width, height, color, x, y) {
  this.width = width;
  this.height = height;
  this.speedX = 0;
  this.speedY = 0;
  this.x = x;
  this.y = y;
  this.update = function() {
    ctx = myGameArea.context;
    ctx.fillStyle = color;
    ctx.fillRect(this.x, this.y, this.width, this.height);
  }
  this.clicked = function() {
    var myleft = this.x;
    var myright = this.x + (this.width);
    var mytop = this.y;
    var mybottom = this.y + (this.height);
    var clicked = true;
    if ((mybottom < myGameArea.y) || (mytop > myGameArea.y) || (myright < myGameArea.x) || (myleft > myGameArea.x)) {
      clicked = false;
    }
    return clicked;
  }
}
function updateGameArea() {
  myGameArea.clear();
  if (myGameArea.x && myGameArea.y) {
    if (myUpBtn.clicked()) {
      myGamePiece.y -= 1;
    }
    if (myDownBtn.clicked()) {
      myGamePiece.y += 1;
    }
    if (myLeftBtn.clicked()) {
      myGamePiece.x += -1;
    }
    if (myRightBtn.clicked()) {
      myGamePiece.x += 1;
    }
  }
  myUpBtn.update();
  myDownBtn.update();
  myLeftBtn.update();
  myRightBtn.update();
  myGamePiece.update();
}
function stopMove() {
  myGamePiece.speedX = 0;
  myGamePiece.speedY = 0;
}
function updateGameArea() {
  myGameArea.clear();
  myGamePiece.speedX = 0;
  myGamePiece.speedY = 0;
  if (myGameArea.keys && myGameArea.keys[37]) {myGamePiece.speedX = -1; }
  if (myGameArea.keys && myGameArea.keys[39]) {myGamePiece.speedX = 1; }
  if (myGameArea.keys && myGameArea.keys[38]) {myGamePiece.speedY = -1; }
  if (myGameArea.keys && myGameArea.keys[40]) {myGamePiece.speedY = 1; }
  myGamePiece.newPos();
  myGamePiece.update();
}
&lt;/script&gt;
&lt;button onmousedown="moveup()" onmouseup="stopMove()" ontouchstart="moveup()"&gt;UP&lt;/button&gt;
&lt;button onmousedown="movedown()" onmouseup="stopMove()" ontouchstart="movedown()"&gt;DOWN&lt;/button&gt;
&lt;button onmousedown="moveleft()" onmouseup="stopMove()" ontouchstart="moveleft()"&gt;LEFT&lt;/button&gt;
&lt;button onmousedown="moveright()" onmouseup="stopMove()" ontouchstart="moveright()"&gt;RIGHT&lt;/button&gt;
</pre>
