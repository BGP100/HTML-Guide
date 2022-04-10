<a href="/CSS/Icons.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/Lists/Main.md">Next &gt;</a>
<hr>
With CSS, links can be styled in many different ways.
<br>
<a href="#">text link
<b><i><s>text link</s></i></b>
<img src="https://i.imgur.com/bcORF04.jpg" width="15%">
<img src="https://i.imgur.com/ScIdbHK.jpg" width="15%"></a>
<h1>Styling</h1>
Links can be styled with any CSS property (e.g. <b>color</b>, <b>font-family</b>, <b>background</b>, etc.).
<pre>
a {
  color: hotpink;
}
</pre>
In addition, links can be styled differently depending on what state they are in.
<br>
The four links states are:
<ul>
  <li><b>a:link</b> - a normal, unvisited link</li>
  <li><b>a:visited</b> - a link the user has visited</li>
  <li><b>a:hover</b> - a link when the user mouses over it</li>
  <li><b>a:active</b> - a link the moment it is clicked</li>
</ul>
<pre>
/* unvisited link */
a:link {
  color: red;
}
/* visited link */
a:visited {
  color: green;
}
/* mouse over link */
a:hover {
  color: hotpink;
}
/* selected link */
a:active {
  color: blue;
}
</pre>
When setting the style for several link states, there are some order rules:
<ul>
  <li>a:hover MUST come after a:link and a:visited</li>
  <li>a:active MUST come after a:hover</li>
</ul>
<h1>Text Decoration</h1>
The <b>text-decoration</b> property is mostly used to remove underlines from links:
<pre>
a:link {
  text-decoration: none;
}
a:visited {
  text-decoration: none;
}
a:hover {
  text-decoration: underline;
}
a:active {
  text-decoration: underline;
}
</pre>
<h1>Background Color</h1>
The <b>background-color</b> property can be used to specify a background color for links:
<pre>
a:link {
  background-color: yellow;
}
a:visited {
  background-color: cyan;
}
a:hover {
  background-color: lightgreen;
}
a:active {
  background-color: hotpink;
}
</pre>
<h1>Buttons</h1>
This example demonstrates a more advanced example where we combine several CSS properties to display links as boxes/buttons:
<pre>
button {
  background-color: #ffffff;
  color: #000000;
}
button:hover {
  background-color: #858585;
  color: #ffffff;
}
</pre>
<h1>More Examples</h1>
<pre>
a.one:link{color:#ff0000;}
a.one:visited{color:#0000ff;}
a.one:hover{color:#ffcc00;}
a.two:link{color:#ff0000;}
a.two:visited{color:#0000ff;}
a.two:hover{font-size:150%;}
a.three:link{color:#ff0000;}
a.three:visited{color:#0000ff;}
a.three:hover{background:#66ff66;}
a.four:link{color:#ff0000;}
a.four:visited{color:#0000ff;}
a.four:hover{font-family:monospace;}
a.five:link{color:#ff0000;text-decoration:none;}
a.five:visited{color:#0000ff;text-decoration:none;}
a.five:hover{text-decoration:underline;}
</pre>
<pre>
a:link, a:visited {
  background-color: white;
  color: black;
  border: 2px solid green;
  padding: 10px 20px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
}
a:hover, a:active {
  background-color: green;
  color: white;
}
</pre>
<pre>
&lt;span style="cursor:auto"&gt;auto&lt;/span&gt;&lt;br&gt;
&lt;span style="cursor:crosshair"&gt;crosshair&lt;/span&gt;&lt;br&gt;
&lt;span style="cursor:default"&gt;default&lt;/span&gt;&lt;br&gt;
&lt;span style="cursor:e-resize"&gt;e-resize&lt;/span&gt;&lt;br&gt;
&lt;span style="cursor:help"&gt;help&lt;/span&gt;&lt;br&gt;
&lt;span style="cursor:move"&gt;move&lt;/span&gt;&lt;br&gt;
&lt;span style="cursor:n-resize"&gt;n-resize&lt;/span&gt;&lt;br&gt;
&lt;span style="cursor:ne-resize"&gt;ne-resize&lt;/span&gt;&lt;br&gt;
&lt;span style="cursor:nw-resize"&gt;nw-resize&lt;/span&gt;&lt;br&gt;
&lt;span style="cursor:pointer"&gt;pointer&lt;/span&gt;&lt;br&gt;
&lt;span style="cursor:progress"&gt;progress&lt;/span&gt;&lt;br&gt;
&lt;span style="cursor:s-resize"&gt;s-resize&lt;/span&gt;&lt;br&gt;
&lt;span style="cursor:se-resize"&gt;se-resize&lt;/span&gt;&lt;br&gt;
&lt;span style="cursor:sw-resize"&gt;sw-resize&lt;/span&gt;&lt;br&gt;
&lt;span style="cursor:text"&gt;text&lt;/span&gt;&lt;br&gt;
&lt;span style="cursor:w-resize"&gt;w-resize&lt;/span&gt;&lt;br&gt;
&lt;span style="cursor:wait"&gt;wait&lt;/span&gt;&lt;br&gt;
</pre>
