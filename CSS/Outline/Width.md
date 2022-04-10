<a href="/CSS/Outline/Main.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/Outline/Colors.md">Next &gt;</a>
<hr>
The outline-width property specifies the width of the outline, and can have one of the following values:
<ul>
  <li>thin (typically 1px)</li>
  <li>medium (typically 3px)</li>
  <li>thick (typically 5px)</li>
  <li>A specific size (in px, pt, cm, em, etc)</li>
</ul>
The following example shows some outlines with different widths:
<br>
<img src="https://i.imgur.com/5PNuoZe.png">
<br>
<img src="https://i.imgur.com/0PwDRcP.png">
<br>
<img src="https://i.imgur.com/2TOxCLO.png">
<br>
<img src="https://i.imgur.com/qzTDurA.png">
<pre>
p.one {
  border: 1px solid black;
  outline-style: solid;
  outline-color: red;
  outline-width: thin;
}
p.two {
  border: 1px solid black;
  outline-style: solid;
  outline-color: red;
  outline-width: medium;
}
p.three {
  border: 1px solid black;
  outline-style: solid;
  outline-color: red;
  outline-width: thick;
}
p.four {
  border: 1px solid black;
  outline-style: solid;
  outline-color: red;
  outline-width: 4px;
}
</pre>
