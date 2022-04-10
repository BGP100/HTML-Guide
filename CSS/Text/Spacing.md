<a href="/CSS/Text/Transformation.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/Text/Shadow.md">Next &gt;</a>
<hr>
<h1>Text Indentation, Letter Spacing, Line Height, Word Spacing, and White Space</h1>
<h2>Text Indentation</h2>
The <b>text-indent</b> property is used to specify the indentation of the first line of a text:
<pre>
p {
  text-indent: 50px;
}
</pre>
<h2>Letter Spacing</h2>
The <b>letter-spacing</b> property is used to specify the space between the characters in a text.
<br>
The following example demonstrates how to increase or decrease the space between characters:
<pre>
h1 {
  letter-spacing: 5px;
}
h2 {
  letter-spacing: -2px;
}
</pre>
<h2>Line Height</h2>
The <b>line-height</b> property is used to specify the space between lines:
<pre>
p.small {
  line-height: 0.8;
}
p.big {
  line-height: 1.8;
}
</pre>
<h2>Word Spacing</h2>
The <b>word-spacing</b> property is used to specify the space between the words in a text.
<br>
The following example demonstrates how to increase or decrease the space between words:
<pre>
p.spacing {
  word-spacing: 10px;
}
p.non-spacing {
  word-spacing: -3px;
}
</pre>
<h2>White Space</h2>
The <b>white-space</b> property specifies how white-space inside an element is handled.
<br>
This example demonstrates how to disable text wrapping inside an element:
<pre>
p {
  white-space: nowrap;
}
</pre>
