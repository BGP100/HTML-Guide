The float property is used for positioning and formatting content e.g. let an image float left to the text in a container.
<br>
The float property can have one of the following values:
<ul>
  <li>left - The element floats to the left of its container</li>
  <li>right - The element floats to the right of its container</li>
  <li>none - The element does not float (will be displayed just where it occurs in the text). This is default</li>
  <li>inherit - The element inherits the float value of its parent</li>
</ul>
In its simplest use, the float property can be used to wrap text around images.
<br>
<img src="https://i.imgur.com/QAeV4Er.jpg" width="100%">
<h1>Example 1</h1>
<img src="https://i.imgur.com/b9LJGzJ.jpg" width="100%">
<pre>
img {
  float: right;
}
</pre>
<h1>Example 2</h1>
Normally div elements will be displayed on top of each other. However, if we use <b>float: left;</b> we can let elements float next to each other:
<pre>
div {
  float: left;
  padding: 15px; 
}
.div1 {
  background: red;
}
.div2 {
  background: yellow;
}
.div3 {
  background: green;
}
</pre>
