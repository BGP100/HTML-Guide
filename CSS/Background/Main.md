<a href="/CSS/Colors/HSL.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/Background/Color.md">Next &gt;</a>
<hr>
To shorten the code, it is also possible to specify all the background properties in one single property. This is called a shorthand property.
<br>
Instead of writing:
<pre>
body {
  background-color: #ffffff;
  background-image: url("img_tree.png");
  background-repeat: no-repeat;
  background-position: right top;
}
</pre>
You can use the shorthand property <b>background</b>:
<pre>
body {
  background: #ffffff url("img_tree.png") no-repeat right top;
}
</pre>
When using the shorthand property the order of the property values is:
<ul>
  <li>background-color</b>
  <li>background-image</b>
  <li>background-repeat</b>
  <li>background-attachment</b>
  <li>background-position</b>
</ul>
It does not matter if one of the property values is missing, as long as the other ones are in this order. Note that we do not use the background-attachment property in the examples above, as it does not have a value.
