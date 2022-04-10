<a href="/CSS/Advanced/Gradients/Linear.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/Advanced/Gradients/Conic.md">Next &gt;</a>
<hr>
<h1>Radial</h1>
A radial gradient is defined by its center.
<br>
To create a radial gradient you must also define at least two color stops.
<br>
<b>Syntax:</b>
<pre>background-image: radial-gradient(shape size at position, start-color, ..., last-color);</pre>
By default, shape is ellipse, size is farthest-corner, and position is center.
<br>
<b>Radial Gradient - Evenly Spaced Color Stops (this is default)</b>
<br>
The following example shows a radial gradient with evenly spaced color stops:
<br>
<img src="https://i.imgur.com/D7zVqv5.jpg" width="100%">
<pre>
#grad {
  background-image: radial-gradient(red, yellow, green);
}
</pre>
<b>Radial Gradient - Differently Spaced Color Stops</b>
<br>
The following example shows a radial gradient with differently spaced color stops:
<br>
<img src="https://i.imgur.com/SVg4H1o.jpg" width="100%">
<pre>
#grad {
  background-image: radial-gradient(red 5%, yellow 15%, green 60%);
}
</pre>
<h1>Set the Shape</h1>
The shape parameter defines the shape. It can take the value circle or ellipse. The default value is ellipse.
<br>
The following example shows a radial gradient with the shape of a circle:
<br>
<img src="https://i.imgur.com/4QELJXT.jpg" width="30%">
<pre>
#grad {
  background-image: radial-gradient(circle, red, yellow, green);
}
</pre>
<h1>Use of Different Size Keywords</h1>
The size parameter defines the size of the gradient. It can take four values:
<ul>
  <li><b>closest-side</b></li>
  <li><b>farthest-side</b></li>
  <li><b>closest-corner</b></li>
  <li><b>farthest-corner</b></li>
</ul>
<pre>
#grad1 {
  background-image: radial-gradient(closest-side at 60% 55%, red, yellow, black);
}
#grad2 {
  background-image: radial-gradient(farthest-side at 60% 55%, red, yellow, black);
}
</pre>
<h1>Repeating</h1>
The repeating-radial-gradient() function is used to repeat radial gradients:
<br>
<img src="https://i.imgur.com/j3Fg4Kg.jpg" width="100%">
<pre>
#grad {
  background-image: repeating-radial-gradient(red, yellow 10%, green 15%);
}
</pre>
