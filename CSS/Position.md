The <b>position</b> property specifies the type of positioning method used for an element (static, relative, fixed, absolute or sticky).
<h1>Property</h1>
The position property specifies the type of positioning method used for an element.
<br>
There are five different position values:
<ul>
  <li><b>static</b></li>
  <li><b>relative</b></li>
  <li><b>fixed</b></li>
  <li><b>absolute</b></li>
  <li><b>sticky</b></li>
</ul>
Elements are then positioned using the top, bottom, left, and right properties. However, these properties will not work unless the <b>position</b> property is set first. They also work differently depending on the position value.
<h1>position: static;</h1>
HTML elements are positioned static by default.
<br>
Static positioned elements are not affected by the top, bottom, left, and right properties.
<br>
An element with <b>position: static;</b> is not positioned in any special way; it is always positioned according to the normal flow of the page.
<pre>
div.static {
  position: static;
  border: 3px solid #73AD21;
}
</pre>
<h1>position: relative;</h1>
An element with <b>position: relative;</b> is positioned relative to its normal position.
<br>
Setting the top, right, bottom, and left properties of a relatively-positioned element will cause it to be adjusted away from its normal position. Other content will not be adjusted to fit into any gap left by the element.
<pre>
div.relative {
  position: relative;
  left: 30px;
  border: 3px solid #73AD21;
}
</pre>
<h1>position: fixed;</h1>
An element with <b>position: fixed;</b> is positioned relative to the viewport, which means it always stays in the same place even if the page is scrolled. The top, right, bottom, and left properties are used to position the element.
<br>
A fixed element does not leave a gap in the page where it would normally have been located.
<br>
Notice the fixed element in the lower-right corner of the page. Here is the CSS that is used:
<pre>
div.fixed {
  position: fixed;
  bottom: 0;
  right: 0;
  width: 300px;
  border: 3px solid #73AD21;
}
</pre>
<h1>position: absulute;</h1>
An element with <b>position: absolute;</b> is positioned relative to the nearest positioned ancestor (instead of positioned relative to the viewport, like fixed).
<br>
However; if an absolute positioned element has no positioned ancestors, it uses the document body, and moves along with page scrolling.
<br>
<b>Note:</b> Absolute positioned elements are removed from the normal flow, and can overlap elements.
<pre>
div.relative {
  position: relative;
  width: 400px;
  height: 200px;
  border: 3px solid #73AD21;
}
div.absolute {
  position: absolute;
  top: 80px;
  right: 0;
  width: 200px;
  height: 100px;
  border: 3px solid #73AD21;
}
</pre>
<h1>position: sticky;</h1>
An element with <b>position: sticky;</b> is positioned based on the user's scroll position.
<br>
A sticky element toggles between <b>relative</b> and <b>fixed</b>, depending on the scroll position. It is positioned relative until a given offset position is met in the viewport - then it "sticks" in place (like position:fixed).
<pre>
div.sticky {
  position: -webkit-sticky; /* Safari */
  position: sticky;
  top: 0;
  background-color: green;
  border: 2px solid #4CAF50;
}
</pre>
<h1>Text &amp; Images</h1>
How to position text over an image:
<br>
<img src="https://i.imgur.com/TDpaN0I.jpg" width="69%">
<br>
<b>Top Left:</b>
<pre>
img {
  width: 100%;
  height: auto;
  opacity: 0.3;
}
.topleft {
  position: absolute;
  top: 8px;
  left: 16px;
  font-size: 18px;
}
</pre>
<b>Top Right:</b>
<pre>
img {
  width: 100%;
  height: auto;
  opacity: 0.3;
}
.topright {
  position: absolute;
  top: 8px;
  right: 16px;
  font-size: 18px;
}
</pre>
<b>Bottom Left:</b>
<pre>
img {
  width: 100%;
  height: auto;
  opacity: 0.3;
}
.bottomleft {
  position: absolute;
  bottom: 8px;
  left: 16px;
  font-size: 18px;
}
</pre>
<b>Bottom Right:</b>
<pre>
img {
  width: 100%;
  height: auto;
  opacity: 0.3;
}
.bottomright {
  position: absolute;
  bottom: 8px;
  right: 16px;
  font-size: 18px;
}
</pre>
<b>Centered:</b>
<pre>
img {
  width: 100%;
  height: auto;
  opacity: 0.3;
}
.center {
  position: absolute;
  top: 50%;
  width: 100%;
  text-align: center;
  font-size: 18px;
}
</pre>
