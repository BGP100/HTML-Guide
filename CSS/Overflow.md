<a href="/CSS/Z-index.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/Float/Main.md">Next &gt;</a>
<hr>
The CSS <b>overflow</b> property controls what happens to content that is too big to fit into an area.
<hr>
The overflow property specifies whether to clip the content or to add scrollbars when the content of an element is too big to fit in the specified area.
<br>
The overflow property has the following values:
<ul>
  <li><b>visible</b> - Default. The overflow is not clipped. The content renders outside the element's box</li>
  <li><b>hidden</b> - The overflow is clipped, and the rest of the content will be invisible</li>
  <li><b>scroll</b> - The overflow is clipped, and a scrollbar is added to see the rest of the content</li>
  <li><b>auto</b> - Similar to <b>scroll</b>, but it adds scrollbars only when necessary</li>
</ul>
<h1>visible</h1>
By default, the overflow is <b>visible</b>, meaning that it is not clipped and it renders outside the element's box:
<br>
<img src="https://i.imgur.com/xWmY4dU.jpg" width="25%">
<pre>
div {
  overflow: visible;
}
</pre>
<h1>hidden</h1>
With the <b>hidden</b> value, the overflow is clipped, and the rest of the content is hidden:
<br>
<img src="https://i.imgur.com/lAGIs6J.jpg" width="25%">
<pre>
div {
  overflow: hidden;
}
</pre>
<h1>scroll</h1>
Setting the value to <b>scroll</b>, the overflow is clipped and a scrollbar is added to scroll inside the box. Note that this will add a scrollbar both horizontally and vertically (even if you do not need it):
<br>
<img src="https://i.imgur.com/vx537xV.jpg" width="25%">
<pre>
div {
  overflow: scroll;
}
</pre>
<h1>auto</h1>
The <b>auto</b> value is similar to <b>scroll</b>, but it adds scrollbars only when necessary:
<br>
<img src="https://i.imgur.com/7NBcZ06.jpg" width="25%">
<pre>
div {
  overflow: auto;
}
</pre>
<h1>x &amp; y</h1>
The <b>overflow-x</b> and <b>overflow-y</b> properties specifies whether to change the overflow of content just horizontally or vertically (or both):
<ul>
  <li>overflow-x specifies what to do with the left/right edges of the content.</li>
  <li>overflow-y specifies what to do with the top/bottom edges of the content.</li>
</ul>
<br>
<img src="https://i.imgur.com/83lxxuf.jpg" width="25%">
<pre>
div {
  overflow-x: hidden; /* Hide horizontal scrollbar */
  overflow-y: scroll; /* Add vertical scrollbar */
}
</pre>
