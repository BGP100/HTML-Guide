The <b>border-color</b> property is used to set the color of the four borders.
<br>
The color can be set by:
<ul>
  <li>name - specify a color name, like "red"</li>
  <li>HEX - specify a HEX value, like "#ff0000"</li>
  <li>RGB - specify a RGB value, like "rgb(255,0,0)"</li>
  <li>HSL - specify a HSL value, like "hsl(0, 100%, 50%)"</li>
  <li>transparent</li>
</ul>
<b><i>Note:</i></b> If <b>border-color</b> is not set, it inherits the color of the element.
<pre>
p.one {
  border-style: solid;
  border-color: red;
}
p.two {
  border-style: solid;
  border-color: green;
}
p.three {
  border-style: dotted;
  border-color: blue;
}
</pre>
<img src="https://i.imgur.com/3OLbS5t.png">
<br>
<img src="https://i.imgur.com/VICYNdV.png">
<br>
<img src="https://i.imgur.com/0ou1mia.png">
<h1>Specific Side Colors</h1>
The <b>border-color</b> property can have from one to four values (for the top border, right border, bottom border, and the left border).
<pre>
p.mix {
  border-style: solid;
  border-color: red green blue yellow; /* red top, green right, blue bottom and yellow left */
}
</pre>
<img src="https://i.imgur.com/Ti1NNfk.png">
<h1>HEX</h1>
<pre>
p.red {
  border-style: solid;
  border-color: #ff0000; /* red */
}
</pre>
<h1>RGB</h1>
<pre>
p.red {
  border-style: solid;
  border-color: rgb(255, 0, 0); /* red */
}
</pre>
<h1>HSL</h1>
<pre>
p.red {
  border-style: solid;
  border-color: hsl(0, 100%, 50%); /* red */
}
</pre>
