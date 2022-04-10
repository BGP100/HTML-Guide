<a href="/CSS/Text/Colors.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/Text/Decoration.md">Next &gt;</a>
<hr>
In this chapter you will learn about the following properties:
<ul>
  <li><b>text-align</b></li>
  <li><b>text-align-last</b></li>
  <li><b>direction</b></li>
  <li><b>unicode-bidi</b></li>
  <li><b>vertical-align</b></li>
</ul>
<h1>text-align</h1>
The <b>text-align</b> property is used to set the horizontal alignment of a text.
<br>
A text can be left or right aligned, centered, or justified.
<br>
The following example shows center aligned, and left and right aligned text (left alignment is default if text direction is left-to-right, and right alignment is default if text direction is right-to-left):
<pre>
h1 {
  text-align: center;
}
h2 {
  text-align: left;
}
h3 {
  text-align: right;
}
</pre>
When the <b>text-align</b> property is set to "justify", each line is stretched so that every line has equal width, and the left and right margins are straight (like in magazines and newspapers):
<pre>
div {
  text-align: justify;
}
</pre>
<h1>text-align-last</h1>
The <b>text-align-last</b> property specifies how to align the last line of a text.
<pre>
p.a {
  text-align-last: right;
}
p.b {
  text-align-last: center;
}
p.c {
  text-align-last: justify;
}
</pre>
<h1>direction & unicode-bidi</h1>
The <b>direction</b> and <b>unicode-bidi</b> properties can be used to change the text direction of an element:
<pre>
p {
  direction: rtl;
  unicode-bidi: bidi-override;
}
</pre>
<h1>vertical-align</h1>
The <b>vertical-align</b> property sets the vertical alignment of an element.
<pre>
img.a {
  vertical-align: baseline;
}
img.b {
  vertical-align: text-top;
}
img.c {
  vertical-align: text-bottom;
}
img.d {
  vertical-align: sub;
}
img.e {
  vertical-align: super;
}
</pre>
