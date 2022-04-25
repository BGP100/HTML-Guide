<a href="/JS/jQuery/Effects/Chaining.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/jQuery/Traversing/Ancestors.md">Next &gt;</a>
<hr>
<h1>What is it?</h1>
jQuery traversing, which means "move through", are used to "find" (or select) HTML elements based on their relation to other elements. Start with one selection and move through that selection until you reach the elements you desire.
<br>
The image below illustrates an HTML page as a tree (DOM tree). With jQuery traversing, you can easily move up (ancestors), down (descendants) and sideways (siblings) in the tree, starting from the selected (current) element. This movement is called traversing - or moving through - the DOM tree.
<br>
<img src="https://i.imgur.com/8zEvw8v.png" width="50%">
<br>
Illustration explained:
<ul>
  <li>The <b>&lt;div&gt;</b> element is the parent of <b>&lt;ul&gt;</b>, and an ancestor of everything inside of it.</li>
  <li>The <b>&lt;ul&gt;</b> element is the parent of both <b>&lt;li&gt;</b> elements, and a child of <b>&lt;div&gt;</b>.</li>
  <li>The left <b>&lt;li&gt;</b> element is the parent of <b>&lt;span&gt;</b>, child of <b>&lt;ul&gt;</b> and a descendant of <b>&lt;div&gt;</b>.</li>
  <li>The <b>&lt;span&gt;</b> element is a child of the left <b>&lt;li&gt;</b> and a descendant of <b>&lt;ul&gt;</b> and <b>&lt;div&gt;</b>.</li>
  <li>The two <b>&lt;li&gt;</b> elements are siblings (they share the same parent).</li>
  <li>The right <b>&lt;li&gt;</b> element is the parent of <b>&lt;b&gt;</b>, child of <b>&lt;ul&gt;</b> and a descendant of <b>&lt;div&gt;</b>.</li>
  <li>The <b>&lt;b&gt;</b> element is a child of the right <b>&lt;li&gt;</b> and a descendant of <b>&lt;ul&gt;</b> and <b>&lt;div&gt;</b>.</li>
</ul>
<h1>Traversing DOM</h1>
jQuery provides a variety of methods that allow us to traverse the DOM.
<br>
The largest category of traversal methods are tree-traversal.
<br>
The next chapters will show us how to travel up, down and sideways in the DOM tree.
