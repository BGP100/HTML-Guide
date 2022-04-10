<a href="/CSS/Margin.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/HeightAndWidth.md">Next &gt;</a>
<hr>
Padding is used to create space around an element's content, inside of any defined borders.
<br>
<img src="https://i.imgur.com/oiDjJRK.png">
<br>
The CSS padding properties are used to generate space around an element's content, inside of any defined borders.

With CSS, you have full control over the padding. There are properties for setting the padding for each side of an element (top, right, bottom, and left).
<p></p>
CSS has properties for specifying the padding for each side of an element:
<ul>
  <li><b>padding-top</b></li>
  <li><b>padding-right</b></li>
  <li><b>padding-bottom</b></li>
  <li><b>padding-left</b></li>
</ul>
All the padding properties can have the following values:
<ul>
  <li>length - specifies a padding in px, pt, cm, etc.</li>
  <li>% - specifies a padding in % of the width of the containing element</li>
  <li>inherit - specifies that the padding should be inherited from the parent element</li>
</ul>
<b>Note:</b> Negative values are not allowed.
<pre>
div {
  padding-top: 50px;
  padding-right: 30px;
  padding-bottom: 50px;
  padding-left: 80px;
}
</pre>
To shorten the code, it is possible to specify all the padding properties in one property.
<br>
The padding property is a shorthand property for the following individual padding properties:
<ul>
  <li><b>padding-top</b></li>
  <li><b>padding-right</b></li>
  <li><b>padding-bottom</b></li>
  <li><b>padding-left</b></li>
</ul>
So, here is how it works:
<br>
If the padding property has four values:
<br>
<b>padding: 25px 50px 75px 100px;</b>
<ul>
  <li>top padding is 25px</b></li>
  <li>right padding is 50px</b></li>
  <li>bottom padding is 75px</b></li>
  <li>left padding is 100px</b></li>
</ul>
<pre>
div {
  padding: 25px 50px 75px 100px;
}
</pre>
If the padding property has three values:
<br>
<b>padding: 25px 50px 75px;</b>
<ul>
top padding is 25px
right and left paddings are 50px
bottom padding is 75px
</ul>
<pre>
div {
  padding: 25px 50px 75px;
}
</pre>
If the padding property has two values:
<br>
<b>padding: 25px 50px;</b>
<ul>
  <li>top and bottom paddings are 25px</li>
  <li>right and left paddings are 50px</li>
</ul>
<pre>
div {
  padding: 25px 50px;
}
</pre>
If the padding property has one value:
<br>
padding: 25px;
<ul>
  <li>all four paddings are 25px</li>
</ul>
<pre>
div {
  padding: 25px;
}
</pre>
<h1>Element Width</h1>
The CSS <b>width</b> property specifies the width of the element's content area. The content area is the portion inside the padding, border, and margin of an element (the box model).
<br>
So, if an element has a specified width, the padding added to that element will be added to the total width of the element. This is often an undesirable result.
<pre>
div {
  width: 300px;
  padding: 25px;
}
</pre>
To keep the width at 300px, no matter the amount of padding, you can use the box-sizing property. This causes the element to maintain its actual width; if you increase the padding, the available content space will decrease.
<pre>
div {
  width: 300px;
  padding: 25px;
  box-sizing: border-box;
}
</pre>
