<a href="/HTML/Head.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/HTML/Responsive.md">Next &gt;</a>
<hr>
Websites often display content in multiple columns (like a magazine or a newspaper).
<br>
<img src="https://i.imgur.com/YIJb7Qa.png">
<h1>Elements</h1>
HTML has several semantic elements that define the different parts of a web page:
<ul>
  <li>&lt;header&gt; - Defines a header for a document or a section.</li>
  <li>&lt;nav&gt; - Defines a set of navigation links.</li>
  <li>&lt;section&gt; - Defines a section in a document.</li>
  <li>&lt;article&gt; - Defines an independent, self-contained content.</li>
  <li>&lt;aside&gt; - Defines content aside from the content (like a sidebar).</li>
  <li>&lt;footer&gt; - Defines a footer for a document or a section.</li>
  <li>&lt;details&gt; - Defines additional details that the user can open and close on demand.</li>
  <li>&lt;summary&gt; - Defines a heading for the &lt;details&gt; element.</li>
  <li>&lt;details&gt; - Defines the content for the &lt;summary&gt; element.</li>
</ul>
<img src="https://i.imgur.com/bxGv0go.png">
<h1>Techniques</h1>
There are four different techniques to create multicolumn layouts. Each technique has its pros and cons:
<ul>
  <li>CSS Framework.</li>
  <li>CSS Float property.</li>
  <li>CSS Flexbox.</li>
  <li>CSS Grid.</li>
</ul>
<h2>Framework</h2>
If you want to create your layout fast, you can use a <a href="/CSS/Responsive/Frameworks.md">CSS framework.
<h2>Float</h2>
It is common to do entire web layouts using the CSS float property. Float is easy to learn - you just need to remember how the float and clear properties work.<br><b>Disadvantages:</b> Floating elements are tied to the document flow, which may harm the flexibility.
<img src="https://i.imgur.com/68JBU5N.png">
<h2>Flexbox</h2>
Use of flexbox ensures that elements behave predictably when the page layout must accommodate different screen sizes and different display devices.
<img src="https://i.imgur.com/7QFPluJ.png">
<h2>Grid</h2>
The CSS Grid Layout Module offers a grid-based layout system, with rows and columns, making it easier to design web pages without having to use floats and positioning.
