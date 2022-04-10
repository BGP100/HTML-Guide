<a href="/HTML/Graphics/Canvas/Text.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/HTML/Graphics/Canvas/Clock/1-Main.md">Next &gt;</a>
<hr>
To draw an image on a canvas, use the following method:
<p></p>
drawImage(image,x,y)
<h1>Example</h1>
<img src="https://i.imgur.com/bvSk9bc.jpg">
<pre>
window.onload = function() {
  var canvas = document.getElementById("myCanvas");
  var ctx = canvas.getContext("2d");
  var img = document.getElementById("scream");
  ctx.drawImage(img, 10, 10);
};
</pre>
