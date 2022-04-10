<a href="/CSS/Advanced/Colors.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/Advanced/Gradients/Linear.md">Next &gt;</a>
<hr>
This page will explain the <b>transparent</b>, <b>currentcolor</b>, and <b>inherit</b> keywords.
<h1>transparent</h1>
The <b>transparent</b> keyword is used to make a color transparent. This is often used to make a transparent background color for an element.
<pre>
body {
  background-image: url("paper.gif");
}
div {
  background-color: transparent;
}
</pre>
<h1>currentcolor</h1>
The <b>currentcolor</b> keyword is like a variable that holds the current value of the color property of an element.
<br>
This keyword can be useful if you want a specific color to be consistent in an element or a page.
<pre>
div {
  color: blue;
  border: 10px solid currentcolor;
}
</pre>
<pre>
body {
  color: purple;
}
div {
  background-color: currentcolor;
}
</pre>
<pre>
body {
 color: green;
}
div {
  box-shadow: 0px 0px 15px currentcolor;
  border: 5px solid currentcolor;
}
</pre>
<h1>inherit</h1>
The <b>inherit</b> keyword specifies that a property should inherit its value from its parent element.
<br>
The <b>inherit</b> keyword can be used for any CSS property, and on any HTML element.
<pre>
div {
  border: 2px solid red;
}
span {
  border: inherit;
}
</pre>
