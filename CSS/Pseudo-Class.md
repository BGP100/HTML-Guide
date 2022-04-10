<a href="/CSS/Combinators.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/Pseudo-Element.md">Next &gt;</a>
<hr>
A pseudo-class is used to define a special state of an element.
<br>
For example, it can be used to:
<ul>
  <li>Style an element when a user mouses over it.</li>
  <li>Style visited and unvisited links differently.</li>
  <li>Style an element when it gets focus.</li>
</ul>
<h1>Syntax</h1>
The syntax of pseudo-classes:
<pre>
selector:pseudo-class {
  property: value;
}
</pre>
<h1>Anchor</h1>
Links can be displayed in different ways:
<pre>
/* unvisited link */
a:link {
  color: #FF0000;
}
/* visited link */
a:visited {
  color: #00FF00;
}
/* mouse over link */
a:hover {
  color: #FF00FF;
}
/* selected link */
a:active {
  color: #0000FF;
}
</pre>
<h1>Combine With HTML Classes</h1>
Pseudo-classes can be combined with HTML classes:
<br>
When you hover over the link in the example, it will change color:
<pre>
a.highlight:hover {
  color: #ff0000;
}
</pre>
<h1>Hover Example</h1>
An example of using the :hover pseudo-class on a <b>&lt;div&gt;</b> element:
<pre>
div:hover {
  background-color: blue;
}
</pre>
<h1>Tooltip Hover</h1>
Hover over a <b>&lt;div&gt;</b> element to show a <b>&lt;p&gt;</b> element (like a tooltip):
<pre>
p {
  display: none;
  background-color: yellow;
  padding: 20px;
}
div:hover p {
  display: block;
}
</pre>
<h1>:first-child Pseudo-class</h1>
The <b>:first-child</b> pseudo-class matches a specified element that is the first child of another element.
<h1>Match the First &lt;p&gt;</h1>
In the following example, the selector matches any <b>&lt;p&gt;</b> element that is the first child of any element:
<pre>
p:first-child {
  color: blue;
}
</pre>
<h1>Match the First &lt;i&gt; in &lt;p&gt; Elements</h1>
In the following example, the selector matches the first <b>&lt;i&gt;</b> element in all <b>&lt;p&gt;</b> elements:
<pre>
p i:first-child {
  color: blue;
}
</pre>
<h1>Match &lt;i&gt; Elements in First &lt;p&gt;</h1>
In the following example, the selector matches all <b>&lt;i&gt;</b> elements in <b>&lt;p&gt;</b> elements that are the first child of another element:
<pre>
p:first-child i {
  color: blue;
}
</pre>
<h1>:lang Pseudo-class</h1>
The <b>:lang</b> pseudo-class allows you to define special rules for different languages.
<br>
In the example below, <b>:lang</b> defines the quotation marks for <b>&lt;q&gt;</b> elements with lang="no":
<pre>
q:lang(no) {
  quotes: "~" "~";
}
</pre>
