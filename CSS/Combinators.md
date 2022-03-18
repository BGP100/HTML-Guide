A CSS selector can contain more than one simple selector. Between the simple selectors, we can include a combinator.
<br>
There are four different combinators in CSS:
<ul>
  <li>descendant selector (space)</li>
  <li>child selector (&gt;)<li>
  <li>adjacent sibling selector (+)</li>
  <li>general sibling selector (~)</li>
</ul>
<h1>Descendant Selector</h1>
The descendant selector matches all elements that are descendants of a specified element.
<br>
The following example selects all <b>&lt;p&gt;</b> elements inside <b>&lt;div&gt;</b> elements:
<pre>
div p {
  background-color: yellow;
}
</pre>
<h1>Child Selector</h1>
The child selector selects all elements that are the children of a specified element.
<br>
The following example selects all <b>&lt;p&gt;</b> elements that are children of a <b>&lt;div&gt;</b> element:
<pre>
div &gt; p {
  background-color: yellow;
}
</pre>
<h1>Adjacent Sibling Selector</h1>
The adjacent sibling selector is used to select an element that is directly after another specific element.
<br>
Sibling elements must have the same parent element, and "adjacent" means "immediately following".
<br>
The following example selects the first <b>&lt;p&gt;</b> element that are placed immediately after <b>&lt;div&gt;</b> elements:
<pre>
div + p {
  background-color: yellow;
}
</pre>
<h1>General Sibling Selector</h1>
The general sibling selector selects all elements that are next siblings of a specified element.
<br>
The following example selects all <b>&lt;p&gt;</b> elements that are next siblings of <b>&lt;div&gt;</b> elements:
<pre>
div ~ p {
  background-color: yellow;
}
</pre>
