<a href="/JS/Graphics/Game/Controller.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Graphics/Game/Scores.md">Next &gt;</a>
<hr>
Now we want to add some obstacles to our game.
<br>
Add a new component to the gaming area. Make it green, 10px wide, 200px high, and place it 300px to the right and 120px down.
<br>
Also update the obstacle component in every frame:
<h1>Add Some</h1>
Now we want to add some obstacles to our game.
<br>
Add a new component to the gaming area. Make it green, 10px wide, 200px high, and place it 300px to the right and 120px down.
<br>
Also update the obstacle component in every frame:
<pre>
var myGamePiece;
var myObstacle;
function startGame() {
  myGamePiece = new component(30, 30, "red", 10, 120);
  myObstacle = new component(10, 200, "green", 300, 120);
  myGameArea.start();
}
function updateGameArea() {
  myGameArea.clear();
  myObstacle.update();
  myGamePiece.newPos();
  myGamePiece.update();
}
</pre>
<h1>Game Over</h1>
In the example above, nothing happens when you hit the obstacle. In a game, that is not very satisfying.
<br>
How do we know if our red square hits the obstacle?
<br>
Create a new method in the component constructor, that checks if the component crashes with another component. This method should be called every time the frames updates, 50 times per second.
<br>
Also add a <b>stop()</b> method to the <b>myGameArea</b> object, which clears the 20 milliseconds interval.
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
  },
  stop : function() {
    clearInterval(this.interval);
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
  this.newPos = function() {
    this.x += this.speedX;
    this.y += this.speedY;
  }
  this.crashWith = function(otherobj) {
    var myleft = this.x;
    var myright = this.x + (this.width);
    var mytop = this.y;
    var mybottom = this.y + (this.height);
    var otherleft = otherobj.x;
    var otherright = otherobj.x + (otherobj.width);
    var othertop = otherobj.y;
    var otherbottom = otherobj.y + (otherobj.height);
    var crash = true;
    if ((mybottom < othertop) ||
    (mytop > otherbottom) ||
    (myright < otherleft) ||
    (myleft > otherright)) {
      crash = false;
    }
    return crash;
  }
}
function updateGameArea() {
  if (myGamePiece.crashWith(myObstacle)) {
    myGameArea.stop();
  } else {
    myGameArea.clear();
    myObstacle.update();
    myGamePiece.newPos();
    myGamePiece.update();
  }
}
</pre>
<h1>Moving Obstacles</h1>
The obstacle is of no danger when it is static, so we want it to move.
<br>
Change the property value of <b>myObstacle.x</b> at every update:
<pre>
function updateGameArea() {
  if (myGamePiece.crashWith(myObstacle)) {
    myGameArea.stop();
  } else {
    myGameArea.clear();
    myObstacle.x += -1;
    myObstacle.update();
    myGamePiece.newPos();
    myGamePiece.update();
  }
}
</pre>
<h1>Multiple Obstacles</h1>
How about adding multiple obstacles?
<br>
For that we need a property for counting frames, and a method for execute something at a given frame rate.
<pre>
var myGameArea = {
  canvas : document.createElement("canvas"),
  start : function() {
    this.canvas.width = 480;
    this.canvas.height = 270;
    this.context = this.canvas.getContext("2d");
    document.body.insertBefore(this.canvas, document.body.childNodes[0]);
    this.frameNo = 0;       
    this.interval = setInterval(updateGameArea, 20);
  },
  clear : function() {
    this.context.clearRect(0, 0, this.canvas.width, this.canvas.height);
  },
  stop : function() {
    clearInterval(this.interval);
  }
}
function everyinterval(n) {
  if ((myGameArea.frameNo / n) % 1 == 0) {return true;}
  return false;
}
</pre>
The everyinterval function returns true if the current framenumber corresponds with the given interval.
<br>
To define multiple obstacles, first declare the obstacle variable as an array.
<br>
Second, we need to make some changes in the updateGameArea function.
<pre>
var myGamePiece;
var myObstacles = [];
function updateGameArea() {
  var x, y;
  for (i = 0; i < myObstacles.length; i += 1) {
    if (myGamePiece.crashWith(myObstacles[i])) {
      myGameArea.stop();
      return;
    }
  }
  myGameArea.clear();
  myGameArea.frameNo += 1;
  if (myGameArea.frameNo == 1 || everyinterval(150)) {
    x = myGameArea.canvas.width;
    y = myGameArea.canvas.height - 200
    myObstacles.push(new component(10, 200, "green", x, y));
  }
  for (i = 0; i < myObstacles.length; i += 1) {
    myObstacles[i].x += -1;
    myObstacles[i].update();
  }
  myGamePiece.newPos();
  myGamePiece.update();
}
</pre>
In the <b>updateGameArea</b> function we must loop through every obstacle to see if there is a crash. If there is a crash, the <b>updateGameArea</b> function will stop, and no more drawing is done.
<br>
The <b>updateGameArea</b> function counts frames and adds an obstacle for every 150th frame.
<h1>Random Size Obstacles</h1>
To make the game a bit more difficult, and fun, we will send in obstacles of random sizes, so that the red square must move up and down to not crash.
<pre>
function updateGameArea() {
  var x, height, gap, minHeight, maxHeight, minGap, maxGap;
  for (i = 0; i < myObstacles.length; i += 1) {
    if (myGamePiece.crashWith(myObstacles[i])) {
      myGameArea.stop();
      return;
    }
  }
  myGameArea.clear();
  myGameArea.frameNo += 1;
  if (myGameArea.frameNo == 1 || everyinterval(150)) {
    x = myGameArea.canvas.width;
    minHeight = 20;
    maxHeight = 200;
    height = Math.floor(Math.random()*(maxHeight-minHeight+1)+minHeight);
    minGap = 50;
    maxGap = 200;
    gap = Math.floor(Math.random()*(maxGap-minGap+1)+minGap);
    myObstacles.push(new component(10, height, "green", x, 0));
    myObstacles.push(new component(10, x - height - gap, "green", x, height + gap));
  }
  for (i = 0; i < myObstacles.length; i += 1) {
    myObstacles[i].x += -1;
    myObstacles[i].update();
  }
  myGamePiece.newPos();
  myGamePiece.update();
}
</pre>
