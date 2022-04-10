<a href="/CSS/Outline/Width.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/Outline/Shorthand.md">Next &gt;</a>
<hr>
The outline-color property is used to set the color of the outline.
<br>
The color can be set by:
<ul>
  <li>name - specify a color name, like "red"</li>
  <li>HEX - specify a hex value, like "#ff0000"</li>
  <li>RGB - specify a RGB value, like "rgb(255,0,0)"</li>
  <li>HSL - specify a HSL value, like "hsl(0, 100%, 50%)"</li>
  <li>invert - performs a color inversion (which ensures that the outline is visible, regardless of color background)</li>
</ul>
The following example shows some different outlines with different colors. Also notice that these elements also have a thin black border inside the outline:
<br>
<img src="https://i.imgur.com/pkJTwCa.png">
<br>
<img src="https://i.imgur.com/ELPImGd.png">
<br>
<img src="https://i.imgur.com/JXiFzLv.png">
<pre>
p.one {
  border: 2px solid black;
  outline-style: solid;
  outline-color: red;
}
p.two {
  border: 2px solid black;
  outline-style: dotted;
  outline-color: blue;
}
p.three {
  border: 2px solid black;
  outline-style: outset;
  outline-color: grey;
}
</pre>
<h1>HEX</h1>
The outline color can also be specified using a hexadecimal value (HEX):
<pre>
p.example {
  outline-style: solid;
  outline-color: #ff0000; /* red */
}
</pre>
<h1>RGB</h1>
Or by using RGB values:
<pre>
p.example {
  outline-style: solid;
  outline-color: rgb(255, 0, 0); /* red */
}
</pre>
<h1>HSL</h1>
You can also use HSL values:
<pre>
p.example {
  outline-style: solid;
  outline-color: hsl(0, 100%, 50%); /* red */
}
</pre>
