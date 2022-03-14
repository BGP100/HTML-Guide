The <b>font-style</b> property is mostly used to specify italic text.
<br>
This property has three values:
<ul>
  <li><b>normal</b> - The text is shown normally.</li>
  <li><b>italic</b> - The text is shown in italics.</li>
  <li><b>oblique</b> - The text is "leaning" (oblique is very similar to italic, but less supported).</li>
</ul>
<pre>
p.normal {
  font-style: normal;
}
p.italic {
  font-style: italic;
}
p.oblique {
  font-style: oblique;
}
</pre>
<h1>Weight</h1>
The <b>font-weight</b> property specifies the weight of a font:
<pre>
p.normal {
  font-weight: normal;
}
p.thick {
  font-weight: bold;
}
</pre>
<h1>Variant</h1>
The <b>font-variant</b> property specifies whether or not a text should be displayed in a small-caps font.
<br>
In a small-caps font, all lowercase letters are converted to uppercase letters. However, the converted uppercase letters appears in a smaller font size than the original uppercase letters in the text.
<pre>
p.normal {
  font-variant: normal;
}
p.small {
  font-variant: small-caps;
}
</pre>
