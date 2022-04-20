<a href="/JS/Graphics/Game/Images.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Graphics/Game/Gravity.md">Next &gt;</a>
<hr>
Use the <b>&lt;audio&gt;</b> element to add sound and music to your games.
<br>
In our examples, we create a new object constructor to handle sound objects:
<pre>
function sound(src) {
  this.sound = document.createElement("audio");
  this.sound.src = src;
  this.sound.setAttribute("preload", "auto");
  this.sound.setAttribute("controls", "none");
  this.sound.style.display = "none";
  document.body.appendChild(this.sound);
  this.play = function(){
    this.sound.play();
  }
  this.stop = function(){
    this.sound.pause();
  }
}
</pre>
To create a new sound object use the sound constructor, and when the red square hits an obstacle, play the sound:
<pre>
var myGamePiece;
var myObstacles = [];
var mySound;

function startGame() {
  myGamePiece = new component(30, 30, "red", 10, 120);
  mySound = new sound("bounce.mp3");
  myGameArea.start();
}

function updateGameArea() {
  var x, height, gap, minHeight, maxHeight, minGap, maxGap;
  for (i = 0; i < myObstacles.length; i += 1) {
    if (myGamePiece.crashWith(myObstacles[i])) {
      mySound.play();
      myGameArea.stop();
      return;
    }
  }
  function sound(src) {
    this.sound = document.createElement("audio");
    this.sound.src = src;
    this.sound.setAttribute("preload", "auto");
    this.sound.setAttribute("controls", "none");
    this.sound.style.display = "none";
    document.body.appendChild(this.sound);
    this.play = function(){
      this.sound.play();
    }
    this.stop = function(){
      this.sound.pause();
    }
  }
}
</pre>
<h1>Background Music</h1>
To add background music to your game, add a new sound object, and start playing when you start the game:
<pre>
var myGamePiece;
var myObstacles = [];
var mySound;
var myMusic;
function startGame() {
  myGamePiece = new component(30, 30, "red", 10, 120);
  mySound = new sound("bounce.mp3");
  myMusic = new sound("gametheme.mp3");
  myMusic.play();
  myGameArea.start();
}
</pre>
