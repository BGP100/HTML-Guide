<a href="/CSS/Pseudo-Class.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/Opacity.md">Next &gt;</a>
<hr>
A CSS pseudo-element is used to style specified parts of an element.
<br>
For example, it can be used to:
<ul>
  <li>Style the first letter, or line, of an element.</li>
  <li>Insert content before, or after, the content of an element.</li>
</ul>
<h1>Syntax</h1>
The syntax of pseudo-elements:
<pre>
selector::pseudo-element {
  property: value;
}
</pre>
<h1>::first-line Pseudo-element</h1>
The <b>::first-line</b> pseudo-element is used to add a special style to the first line of a text.
<br>
The following example formats the first line of the text in all <b>&lt;p&gt;</b> elements:
<pre>
p::first-line {
  color: #ff0000;
  font-variant: small-caps;
}
</pre>
<b><i>Note:</i></b> The <b>::first-line</b> pseudo-element can only be applied to block-level elements.
<br>
The following properties apply to the ::first-line pseudo-element:
<ul>
  <li><b>font properties</b></li>
  <li><b>color properties</b></li>
  <li><b>background properties</b></li>
  <li><b>word-spacing</b></li>
  <li><b>letter-spacing</b></li>
  <li><b>text-decoration</b></li>
  <li><b>vertical-align</b></li>
  <li><b>text-transform</b></li>
  <li><b>line-height</b></li>
  <li><b>clear</b></li>
</ul>
<h1>::first-letter Pseudo-element</h1>
The <b>::first-letter</b> pseudo-element is used to add a special style to the first letter of a text.
<br>
The following example formats the first letter of the text in all <b>&lt;p&gt;</b> elements:
<pre>
p::first-letter {
  color: #ff0000;
  font-size: xx-large;
}
</pre>
<b><i>Note:</i></b> The <b>::first-letter</b> pseudo-element can only be applied to block-level elements.
<br>
The following properties apply to the ::first-letter pseudo- element: 
<ul>
  <li><b>font properties</b></li>
  <li><b>color properties</b></li>
  <li><b>background properties</b></li>
  <li><b>margin properties</b></li>
  <li><b>padding properties</b></li>
  <li><b>border properties</b></li>
  <li><b>text-decoration</b></li>
  <li><b>vertical-align (only if "float" is "none")</b></li>
  <li><b>text-transform</b></li>
  <li><b>line-height</b></li>
  <li><b>float</b></li>
  <li><b>clear</b></li>
</ul>
<h1>Combine with HTML Classes</h1>
Pseudo-elements can be combined with HTML classes:
<pre>
p.intro::first-letter {
  color: #ff0000;
  font-size: 200%;
}
</pre>
The example above will display the first letter of paragraphs with class="intro", in red and in a larger size.
<h1>Multiple Pseudo-Elements</h1>
Several pseudo-elements can also be combined.
<br>
In the following example, the first letter of a paragraph will be red, in an xx-large font size. The rest of the first line will be blue, and in small-caps. The rest of the paragraph will be the default font size and color:
<pre>
p::first-letter {
  color: #ff0000;
  font-size: xx-large;
}
p::first-line {
  color: #0000ff;
  font-variant: small-caps;
}
</pre>
<h1>::before Pseudo-Element</h1>
The <b>::before</b> pseudo-element can be used to insert some content before the content of an element.
<br>
The following example inserts an image before the content of each <b>&lt;h1&gt;</b> element:
<pre>
h1::before {
  content: url(//i.imgur.com/ixnaQfO.gif);
}
</pre>
<h1>::after Pseudo-Element</h1>
The <b>::after</b> pseudo-element can be used to insert some content after the content of an element.
<br>
The following example inserts an image after the content of each <b>&lt;h1&gt;</b> element:
<pre>
h1::after {
  content: url(//i.imgur.com/ixnaQfO.gif);
}
</pre>
<h1>::marker Pseudo-Element</h1>
The <b>::marker</b> pseudo-element selects the markers of list items.
<br>
The following example styles the markers of list items:
<pre>
::marker {
  color: red;
  font-size: 23px;
}
</pre>
<h1>::selection Pseudo-Element</h1>
The <b>::selection</b> pseudo-element matches the portion of an element that is selected by a user.
<br>
The following CSS properties can be applied to <b>::selection</b>: <b>color</b>, <b>background</b>, <b>cursor</b>, and <b>outline</b>.
<br>
The following example makes the selected text red on a yellow background:
<pre>
::selection {
  color: red;
  background: yellow;
}
</pre>
