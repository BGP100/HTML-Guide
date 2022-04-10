<a href="/CSS/NavigationBar/Vertical.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/Dropdown.md">Next &gt;</a>
<hr>
<a href="https://github.com/BGP100/topnav.html">Click Here</a> to see the code for the <b>Navigation Var</b>.
<hr>
<img src="https://i.imgur.com/V63iU8V.png">
There are two ways to create a horizontal navigation bar. Using inline or floating list items.
<h1>Inline</h1>
One way to build a horizontal navigation bar is to specify the <b>&lt;li&gt;</b> elements as inline, in addition to the "standard" code from the previous page:
<pre>
li {
  display: inline;
}
</pre>
<b>Explained:</b>
<ul>
  <li><b>display: inline;</b> - By default, <b>&lt;li&gt;</b> elements are block elements. Here, we remove the line breaks before and after each list item, to display them on one line.</li>
</ul>
<h1>Floating</h1>
Another way of creating a horizontal navigation bar is to float the <b>&lt;li&gt;</b> elements, and specify a layout for the navigation links:
<pre>
li {
  float: left;
}
a {
  display: block;
  padding: 8px;
  background-color: #dddddd;
}
</pre>
<b>Explained:</b>
<ul>
  <li><b>float: left;</b> - Use float to get block elements to float next to each other</li>
  <li><b>display: block;</b> - Allows us to specify padding (and height, width, margins, etc. if you want)</li>
  <li><b>padding: 8px;</b> - Specify some padding between each <b>&lt;a&gt;</b> element, to make them look good</li>
  <li><b>background-color:</b> #dddddd; - Add a gray background-color to each <b>&lt;a&gt;</b> element</li>
</ul>
</b>Tip:</b> Add the background-color to <b>&lt;ul&gt;</b> instead of each <b>&lt;a&gt;</b> element if you want a full-width background color:
<pre>
ul {
  background-color: #dddddd;
}
</pre>
<h1>Examples</h1>
Create a basic horizontal navigation bar with a dark background color and change the background color of the links when the user moves the mouse over them:
<br>
<img src="https://i.imgur.com/Dg6RyPp.png">
<pre>
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  overflow: hidden;
  background-color: #333;
}
li {
  float: left;
}
li a {
  display: block;
  color: white;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
}
/* Change the link color to #111 (black) on hover */
li a:hover {
  background-color: #111;
}
</pre>
<hr>
Add an "active" class to the current link to let the user know which page he/she is on:
<br>
<img src="https://i.imgur.com/V63iU8V.png">
<pre>
.active {
  background-color: #04AA6D;
}
</pre>
<hr>
Right-align links by floating the list items to the right (float:right;):
<br>
<img src="https://i.imgur.com/84OCTKc.png">
<pre>
&lt;ul&gt;
  &lt;li&gt;&lt;a href="#home"&gt;Home&lt;/a&gt;&lt;/li&gt;
  &lt;li&gt;&lt;a href="#news"&gt;News&lt;/a&gt;&lt;/li&gt;
  &lt;li&gt;&lt;a href="#contact"&gt;Contact&lt;/a&gt;&lt;/li&gt;
  &lt;li style="float:right"&gt;&lt;a class="active" href="#about">About&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
</pre>
<hr>
Add the border-right property to <b>&lt;li&gt;</b> to create link dividers:
<br>
<img src="https://i.imgur.com/GoXhiUi.png">
<pre>
/* Add a gray right border to all list items, except the last item (last-child) */
li {
  border-right: 1px solid #bbb;
}
li:last-child {
  border-right: none;
}
</pre>
<hr>
Make the navigation bar stay at the top or the bottom of the page, even when the user scrolls the page:
<br>
<img src="https://i.imgur.com/wUF6hAO.png">
<pre>
ul {
  position: fixed;
  top: 0;
  width: 100%;
}
</pre>
<img src="https://i.imgur.com/3cdlexg.png">
<pre>
ul {
  position: fixed;
  bottom: 0;
  width: 100%;
}
</pre>
<hr>
An example of a gray horizontal navigation bar with a thin gray border:
<br>
<img src="https://i.imgur.com/VbLi70q.png">
<pre>
ul {
  border: 1px solid #e7e7e7;
  background-color: #f3f3f3;
}
li a {
  color: #666;
}
</pre>
<hr>
Add <b>position: sticky;</b> to <b>&lt;li&gt;</b> to create a sticky navbar.
<br>
A sticky element toggles between relative and fixed, depending on the scroll position. It is positioned relative until a given offset position is met in the viewport - then it "sticks" in place (like position:fixed).
<br>
<img src="https://i.imgur.com/XVEK7WT.png">
<pre>
ul {
  position: -webkit-sticky; /* Safari */
  position: sticky;
  top: 0;
}
</pre>
<h2>MORE</h2>
<img src="https://i.imgur.com/JwteRvA.jpg">
<p></p>
<img src="https://i.imgur.com/CrzFMdW.jpg">
<p></p>
<img src="https://i.imgur.com/JVutkwr.png">
