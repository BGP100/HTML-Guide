<a href="/JS/Graphics/Game/Obstacles.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Graphics/Game/Images.md">Next &gt;</a>
<hr>
There are many ways to keep the score in a game, we will show you how to write a score onto the canvas.
<br>
First make a score component:
<pre>
var myGamePiece;
var myObstacles = [];
var myScore;
function startGame() {
  myGamePiece = new component(30, 30, "red", 10, 160);
  myScore = new component("30px", "Consolas", "black", 280, 40, "text");
  myGameArea.start();
}
</pre>
The syntax for writing text on a canvas element is different from drawing a rectangle. Therefore we must call the component constructor using an additional argument, telling the constructor that this component is of type "text".
<br>
In the component constructor we test if the component is of type "text", and use the <b>fillText</b> method instead of the <b>fillText</b> method:
<pre>
function component(width, height, color, x, y, type) {
  this.type = type;
  this.width = width;
  this.height = height;
  this.speedX = 0;
  this.speedY = 0;
  this.x = x;
  this.y = y;
  this.update = function() {
    ctx = myGameArea.context;
    if (this.type == "text") {
      ctx.font = this.width + " " + this.height;
      ctx.fillStyle = color;
      ctx.fillText(this.text, this.x, this.y);
    } else {
      ctx.fillStyle = color;
      ctx.fillRect(this.x, this.y, this.width, this.height);
    }
  }
  var myGamePiece;
  var myObstacles = [];
  var myScore;
  function startGame() {
    myGamePiece = new component(30, 30, "red", 10, 160);
    myScore = new component("30px", "Consolas", "black", 280, 40, "text");
    myGameArea.start();
  }
}
</pre>
At last we add some code in the updateGameArea function that writes the score onto the canvas. We use the frameNo property to count the score:
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
    myObstacles[i].speedX = -1;
    myObstacles[i].newPos();
    myObstacles[i].update();
  }
  myScore.text = "SCORE: " + myGameArea.frameNo;
  myScore.update();
  myGamePiece.newPos();
  myGamePiece.update();
}
</pre>
