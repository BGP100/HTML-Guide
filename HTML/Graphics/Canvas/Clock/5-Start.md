<h1>Part V - Start the Clock</h1>
To start the clock, call the drawClock function at intervals:
<img src="https://i.imgur.com/s3fYuMy.gif" width="40%">
<h1>Code</h1>
The only thing you have to do (to start the clock) is to call the drawClock function at intervals.
<p></p>
Substitute:
<pre>drawClock();</pre>
With:
<pre>setInterval(drawClock, 1000);</pre>
<h2>All the Code Joined in One</h2>
<pre>
var canvas = document.getElementById("canvas");
var ctx = canvas.getContext("2d");
var radius = canvas.height / 2;
ctx.translate(radius, radius);
radius = radius * 0.90
//drawClock();
setInterval(drawClock, 1000);
</pre>
