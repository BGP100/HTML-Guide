<a href="/HTML/Graphics/Game/Main.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/HTML/Graphics/Game/Components.md">Next &gt;</a>
<hr>
<a href="/HTML/Graphics/Canvas/">Click Here</a> for more <i>Canvas</i> info.
<hr>
The <b>&lt;canvas&gt;</b> element is perfect for making games in HTML.
<br>
The <b>&lt;canvas&gt;</b> element offers all the functionality you need for making games.
<br>
Use JavaScript to draw, write, insert images, and more, onto the <b>&lt;canvas&gt;</b>.
<h1>.getContext(2d)</h1>
The <b>&lt;canvas&gt;</b> element has a built-in object, called the <b>getContext("2d")</b> object, with methods and properties for drawing.
<h1>Start Making a Game</h1>
To make a game, start by creating a gaming area, and make it ready for drawing:
<pre>
function startGame() {
  myGameArea.start();
}
var myGameArea = {
  canvas : document.createElement("canvas"),
  start : function() {
    this.canvas.width = 480;
    this.canvas.height = 270;
    this.context = this.canvas.getContext("2d");
    document.body.insertBefore(this.canvas, document.body.childNodes[0]);
  }
}
</pre>
The object <b>myGameArea</b> will have more properties and methods later in this tutorial.
<br>
The function <b>startGame()</b> invokes the method <b>start()</b> of the <b>myGameArea</b> object.
<br>
The <b>start()</b> method creates a <b>&lt;canvas&gt;</b> element and inserts it as the first childnode of the <b>&lt;body&gt;</b> element.
