<a href="/CSS/Tables/Responsive.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/Max-width.md">Next &gt;</a>
<hr>
The <b>display</b> property is the most important CSS property for controlling layout.
<hr>
The <b>display</b> property specifies if/how an element is displayed.
<br>
Every HTML element has a default display value depending on what type of element it is. The default display value for most elements is block or <b>inline</b>.
<br>
<b>Sorry, but GitHub can't handle these things. So just go to the coding part!</b>
<h1>block-level</h1>
A block-level element always starts on a new line and takes up the full width available (stretches out to the left and right as far as it can).
<br>
Examples of block-level elements:
<ul>
  <li>&lt;div&gt;</li>
  <li>&lt;h1&gt; <b>•••</b> &lt;h6&gt;</li>
  <li>&lt;p&gt;</li>
  <li>&lt;form&gt;</li>
  <li>&lt;header&gt;</li>
  <li>&lt;footer&gt;</li>
  <li>&lt;section&gt;</li>
</ul>
<h1>inline</h1>
An inline element does not start on a new line and only takes up as much width as necessary.
<br>
Examples of inline elements:
<ul>
  <li>&lt;span&gt;</li>
  <li>&lt;a&gt;</li>
  <li>&lt;img&gt;</li>
</ul>
<h1>display: none;</h1>
<b>display: none;</b> is commonly used with JavaScript to hide and show elements without deleting and recreating them. Take a look at our last example on this page if you want to know how this can be achieved.
<br>
The <b>&lt;script&gt;</b> element uses <b>display: none;</b> as default.
<h1>Override Default Display</h1>
As mentioned, every element has a default display value. However, you can override this.
<br>
Changing an inline element to a block element, or vice versa, can be useful for making the page look a specific way, and still follow the web standards.
<br>
A common example is making inline <b>&lt;li&gt;</b> elements for horizontal menus:
<pre>
li {
  display: inline;
}
</pre>
The following example displays <b>&lt;span&gt;</b> elements as block elements:
<pre>
span {
  display: block;
}
</pre>
The following example displays <b>&lt;a&gt;</b> elements as block elements:
<pre>
a {
  display: block;
}
</pre>
