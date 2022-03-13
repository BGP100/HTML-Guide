In this chapter you will learn about the following properties:
<ul>
  <li><b>text-decoration-line</b></li>
  <li><b>text-decoration-color</b></li>
  <li><b>text-decoration-style</b></li>
  <li><b>text-decoration-thickness</b></li>
  <li><b>text-decoration</b></li>
</ul>
<h1>Deco Lines</h1>
The <b>text-decoration-line</b> property is used to add a decoration line to text.
<br>
<b>Tip:</b> You can combine more than one value, like overline and underline to display lines both over and under a text.
<pre>
line1up {
  text-decoration-line: overline;
}
line2through {
  text-decoration-line: line-through;
}
line3down {
  text-decoration-line: underline;
}
line4mixed {
  text-decoration-line: overline underline;
}
</pre>
<h2>Specify a Color</h2>
The <b>text-decoration-color</b> property is used to set the color of the decoration line.
<pre>
line1up.red {
  text-decoration-line: overline;
  text-decoration-color: red;
}
line2through.blue {
  text-decoration-line: line-through;
  text-decoration-color: blue;
}
line3down.green {
  text-decoration-line: underline;
  text-decoration-color: green;
}
line4mixed.purple {
  text-decoration-line: overline underline;
  text-decoration-color: purple;
}
</pre>
<h2>Specify a Style</h2>
The <b>text-decoration-style</b> property is used to set the style of the decoration line.
<pre>
line1down.solid {
  text-decoration-line: underline;
  text-decoration-style: solid;
}
line1down.double {
  text-decoration-line: underline;
  text-decoration-style: double;
}
line1down.dotted {
  text-decoration-line: underline;
  text-decoration-style: dotted;
}
line1down.dashed {
  text-decoration-line: underline;
  text-decoration-style: dashed;
}
line1down.wavy {
  text-decoration-line: underline;
  text-decoration-style: wavy;
}
line1down.red-wavy {
  text-decoration-line: underline;
  text-decoration-color: red;
  text-decoration-style: wavy;
}
</pre>
<h2>Specify the Thickness</h2>
The <b>text-decoration-thickness</b> property is used to set the thickness of the decoration line.
<pre>
line1down.auto-thick {
  text-decoration-line: underline;
  text-decoration-thickness: auto;
}
line1down.5x-thick {
  text-decoration-line: underline;
  text-decoration-thickness: 5px;
}
line1down.25p-thick {
  text-decoration-line: underline;
  text-decoration-thickness: 25%;
}
line1down.red-double-5p-thick {
  text-decoration-line: underline;
  text-decoration-color: red;
  text-decoration-style: double;
  text-decoration-thickness: 5px;
}
</pre>
<h2>Shorthand</h2>
The text-decoration property is a shorthand property for:
<ul>
  <li><b>text-decoration-line</b> (required)</li>
  <li><b>text-decoration-color</b> (optional)</li>
  <li><b>text-decoration-style</b> (optional)</li>
  <li><b>text-decoration-thickness</b> (optional)</li>
</ul>
<pre>
line1down {
  text-decoration: underline;
}
line1down.red {
  text-decoration: underline red;
}
line1down.red-double {
  text-decoration: underline red double;
}
line1down.red-double-5p-thick {
  text-decoration: underline red double 5px;
}
</pre>
<h2>Tip</h2>
All links in HTML are underlined by default. Sometimes you see that links are styled with no underline. The <b>text-decoration:</b> none; is used to remove the underline from links, like this:
<pre>
a {
  text-decoration: none;
  color: #000;
}
</pre>
