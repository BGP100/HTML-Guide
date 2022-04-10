<a href="/CSS/Advanced/Shadow/Box.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/Advanced/Fonts.md">Next &gt;</a>
<hr>
In this chapter you will learn about the following properties:
<ul>
  <li><a href="#text-overflow">text-overflow</a></li>
  <li><a href="#word-wrap">word-wrap</a></li>
  <li><a href="#word-break">word-break</a></li>
  <li><a href="#writing-mode">writing-mode</a></li>
</ul>
<h1>text-overflow</h1>
The CSS text-overflow property specifies how overflowed content that is not displayed should be signaled to the user.
<br>
It can be clipped:
<br>
<img src="https://i.imgur.com/lhDwwXZ.jpg" width="25%">
<br>
or it can be rendered as an ellipsis (...):
<br>
<img src="https://i.imgur.com/ACfXKrg.jpg" width="25%">
<br>
The CSS code is as follows:
<pre>
p.test1 {
  white-space: nowrap; 
  width: 200px; 
  border: 1px solid #000000;
  overflow: hidden;
  text-overflow: clip; 
}
p.test2 {
  white-space: nowrap; 
  width: 200px; 
  border: 1px solid #000000;
  overflow: hidden;
  text-overflow: ellipsis; 
}
</pre>
The following example shows how you can display the overflowed content when hovering over the element:
<pre>
div.test:hover {
  overflow: visible;
}
</pre>
<h1>word-wrap</h1>
The CSS <b>word-wrap</b> property allows long words to be able to be broken and wrap onto the next line. 
<br>
If a word is too long to fit within an area, it expands outside:
<br>
<img src="https://i.imgur.com/4jv5g1T.jpg" width="50%">
<br>
The word-wrap property allows you to force the text to wrap - even if it means splitting it in the middle of a word:
<br>
<img src="https://i.imgur.com/uzVKBtk.jpg" width="25%">
The CSS code is as follows:
<pre>
p {
  word-wrap: break-word;
}
</pre>
<h1>word-break</h1>
The CSS <b>word-break</b> property specifies line breaking rules.
<br>
<img src="https://i.imgur.com/q1sI37W.jpg" width="25%">
<br>
<img src="https://i.imgur.com/6MmqA4c.jpg" width="25%">
<br>
The CSS code is as follows:
<pre>
p.test1 {
  word-break: keep-all;
}
p.test2 {
  word-break: break-all;
}
</pre>
<h1>writing-mode</h1>
The CSS writing-mode property specifies whether lines of text are laid out horizontally or vertically.
<br>
Some text with a span element with a <b>vertical-rl</b> writing-mode.
<br>
The following example shows some different writing modes:
<pre>
p.test1 {
  writing-mode: horizontal-tb; 
}
span.test2 {
  writing-mode: vertical-rl; 
}
p.test2 {
  writing-mode: vertical-rl; 
}
</pre>
