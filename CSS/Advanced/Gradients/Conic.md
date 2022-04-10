<a href="/CSS/Advanced/Gradients/Radial.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/Advanced/Shadow/Effects.md">Next &gt;</a>
<hr>
A conic gradient is a gradient with color transitions rotated around a center point.
<br>
To create a conic gradient you must define at least two colors.
<br>
<b>Syntax:</b>
<pre>background-image:conic-gradient([from angle] [at position,] color [degree], color [degree], ...);</pre>
By default, angle is 0deg and position is center.
<br>
If no degree is specified, the colors will be spread equally around the center point.
<h1>3 Colors</h1>
The following example shows a conic gradient with three colors:
<br>
<img src="https://i.imgur.com/QvEDork.jpg" width="17%">
<pre>
#grad {
  background-image: conic-gradient(red, yellow, green);
}
</pre>
<h1>5 Colors</h1>
The following example shows a conic gradient with five colors:
<br>
<img src="https://i.imgur.com/VRqdJy4.jpg" width="17%">
<pre>
#grad {
  background-image: conic-gradient(red, yellow, green, blue, black);
}
</pre>
<h1>3 Colors with Degrees</h1>
The following example shows a conic gradient with three colors and a degree for each color:
<br>
<img src="https://i.imgur.com/omRnFQJ.jpg" width="17%">
<pre>
#grad {
  background-image: conic-gradient(red 45deg, yellow 90deg, green 210deg);
}
</pre>
<h1>Pie Charts</h1>
Just add <b>border-radius: 50%</b> to make the conic gradient look like a pie:
<br>
<img src="https://i.imgur.com/ll5esxd.jpg" width="17%">
<pre>
#grad {
  background-image: conic-gradient(red, yellow, green, blue, black);
  border-radius: 50%;
}
</pre>
Here is another pie chart with defined degrees for all the colors:
<br>
<img src="https://i.imgur.com/i957ISr.jpg" width="17%">
<pre>
#grad {
  background-image: conic-gradient(red 0deg, red 90deg, yellow 90deg, yellow 180deg, green 180deg, green 270deg, blue 270deg);
  border-radius: 50%;
}
</pre>
<h1>Specified Angles</h1>
The <b>[from angle]</b> specifies an angle that the entire conic gradient is rotated by.
<br>
The following example shows a conic gradient with a from angle of <b>90deg</b>:
<br>
<img src="https://i.imgur.com/PKHAjqS.jpg" width="17%">
<pre>
#grad {
  background-image: conic-gradient(from 90deg, red, yellow, green);
}
</pre>
<h1>Specified Center Position</h1>
The <b>[at position]</b> specifies the center of the conic gradient.
<br>
The following example shows a conic gradient with a center position of <b>60% 45%</b>:
<br>
<img src="https://i.imgur.com/Nl5AHYD.jpg" width="17%">
<pre>
#grad {
  background-image: conic-gradient(at 60% 45%, red, yellow, green);
}
</pre>
<h1>Repeating</h1>
The <b>repeating-conic-gradient()</b> function is used to repeat conic gradients:
<br>
<img src="https://i.imgur.com/8EFbs7x.jpg" width="17%">
<pre>
#grad {
  background-image: repeating-conic-gradient(red 10%, yellow 20%);
  border-radius: 50%;
}
</pre>
Here is a repeating conic gradient with defined color-starts and color-stops:
<img src="https://i.imgur.com/UuYnVAo.jpg" width="17%">
<pre>
#grad {
  background-image: repeating-conic-gradient(red 0deg 10deg, yellow 10deg 20deg, blue 20deg 30deg);
  border-radius: 50%;
}
</pre>
