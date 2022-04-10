<a href="/CSS/Advanced/ColorKeywords.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/Advanced/Gradients/Radial.md">Next &gt;</a>
<hr>
<img src="https://i.imgur.com/7DHWHNj.jpg" width="100%">
<br>
CSS gradients let you display smooth transitions between two or more specified colors.
<br>
CSS defines three types of gradients:
<ul>
  <li><b>Linear Gradients (goes down/up/left/right/diagonally)</b></li>
  <li><b>Radial Gradients (defined by their center)</b></li>
  <li><b>Conic Gradients (rotated around a center point)</b></li>
</ul>
<h1>Linear</h1>
To create a linear gradient you must define at least two color stops. Color stops are the colors you want to render smooth transitions among. You can also set a starting point and a direction (or an angle) along with the gradient effect.
<br>
<b>Syntax:</b>
<pre>background-image: linear-gradient(direction, color-stop1, color-stop2, ...);</pre>
<b>Direction - Top to Bottom (this is default)</b>
<br>
The following example shows a linear gradient that starts at the top. It starts red, transitioning to yellow:
<br>
<img src="https://i.imgur.com/4RKkK0i.jpg" width="100%">
<pre>
#grad {
  background-image: linear-gradient(red, yellow);
}
</pre>
<b>Direction - Left to Right</b>
<br>
The following example shows a linear gradient that starts from the left. It starts red, transitioning to yellow:
<br>
<img src="https://i.imgur.com/w8VuobN.jpg" width="100%">
<pre>
#grad {
  background-image: linear-gradient(to right, red, yellow);
}
</pre>
<b>Direction - Diagonal</b>
<br>
You can make a gradient diagonally by specifying both the horizontal and vertical starting positions.
<br>
The following example shows a linear gradient that starts at top left (and goes to bottom right). It starts red, transitioning to yellow:
<br>
<img src="https://i.imgur.com/uBpfFCc.jpg" width="100%">
<pre>
#grad {
  background-image: linear-gradient(to bottom right, red, yellow);
}
</pre>
<h1>Angles</h1>
If you want more control over the direction of the gradient, you can define an angle, instead of the predefined directions (to bottom, to top, to right, to left, to bottom right, etc.). A value of 0deg is equivalent to "to top". A value of 90deg is equivalent to "to right". A value of 180deg is equivalent to "to bottom".
<br>
<b>Syntax:</b>
<pre>background-image: linear-gradient(angle, color-stop1, color-stop2);</pre>
The following example shows how to use angles on linear gradients:
<br>
<img src="https://i.imgur.com/FFGQ8Ti.jpg" width="100%">
<pre>
#grad {
  background-image: linear-gradient(180deg, red, yellow);
}
</pre>
<h1>Multiple</h1>
The following example shows a linear gradient (from top to bottom) with multiple color stops:
<br>
<img src="https://i.imgur.com/s08v4LG.jpg" width="100%">
<pre>
#grad {
  background-image: linear-gradient(red, yellow, green);
}
</pre>
The following example shows how to create a linear gradient (from left to right) with the color of the rainbow and some text:
<br>
<img src="https://i.imgur.com/SmamwUZ.jpg" width="100%">
<pre>
#grad {
  background-image: linear-gradient(to right, red,orange,yellow,green,blue,indigo,violet); 
}
</pre>
<h1>Transparency</h1>
CSS gradients also support transparency, which can be used to create fading effects.
<br>
To add transparency, we use the rgba() function to define the color stops. The last parameter in the rgba() function can be a value from 0 to 1, and it defines the transparency of the color: 0 indicates full transparency, 1 indicates full color (no transparency).
<br>
The following example shows a linear gradient that starts from the left. It starts fully transparent, transitioning to full color red:
<br>
<img src="https://i.imgur.com/PvavA9T.jpg" width="100%">
<pre>
#grad {
  background-image: linear-gradient(to right, rgba(255,0,0,0), rgba(255,0,0,1));
}
</pre>
<h1>Repeating</h1>
The repeating-linear-gradient() function is used to repeat linear gradients:
<br>
<img src="https://i.imgur.com/Jjh3nLr.jpg" width="100%">
<pre>
#grad {
  background-image: repeating-linear-gradient(red, yellow 10%, green 20%);
}
</pre>
