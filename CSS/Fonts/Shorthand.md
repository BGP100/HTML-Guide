<a href="/CSS/Fonts/Pairing.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/Icons.md">Next &gt;</a>
<hr>
To shorten the code, it is also possible to specify all the individual font properties in one property.
<br>
The <b>font</b> property is a shorthand property for:
<ul>
  <li><b>font-style</b></li>
  <li><b>font-variant</b></li>
  <li><b>font-weight</b></li>
  <li><b>font-size/line-height</b></li>
  <li><b>font-family</b></li>
</ul>
<b><i>Note:</i></b> The <b>font-size</b> and <b>font-family</b> values are required. If one of the other values is missing, their default value are used.
<pre>
p.a {
  font: 20px Arial, sans-serif;
}
p.b {
  font: italic small-caps bold 12px/30px Georgia, serif;
}
</pre>
