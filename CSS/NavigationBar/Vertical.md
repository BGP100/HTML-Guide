<a href="/CSS/NavigationBar/Main.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/NavigationBar/Horizontal.md">Next &gt;</a>
<hr>
<a href="https://github.com/BGP100/topnav.html">Click Here</a> to see the code for the <b>Navigation Var</b>.
<hr>
<img src="https://i.imgur.com/74ce74a.png" width="100%">
<br>
To build a vertical navigation bar, you can style the <b>&lt;a&gt;</b> elements inside the list, in addition to the code from the previous page:
<pre>
li a {
  display: block;
  width: 60px;
}
</pre>
<b>Explained:</b>
<ul>
  <li><b>display: block;</b> - Displaying the links as block elements makes the whole link area clickable (not just the text), and it allows us to specify the width (and padding, margin, height, etc. if you want).</li>
  <li><b>width: 60px;</b> - Block elements take up the full width available by default. We want to specify a 60 pixels width.</li>
</ul>
You can also set the width of <b>&lt;ul&gt;</b>, and remove the width of <b>&lt;a&gt;</b>, as they will take up the full width available when displayed as block elements. This will produce the same result as our previous example:
<pre>
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  width: 60px;
}
li a {
  display: block;
}
</pre>
<h1>Examples</h1>
Create a basic vertical navigation bar with a gray background color and change the background color of the links when the user moves the mouse over them:
<br>
<img src="https://i.imgur.com/025Q9Jw.png">
<pre>
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  width: 200px;
  background-color: #f1f1f1;
}
li a {
  display: block;
  color: #000;
  padding: 8px 16px;
  text-decoration: none;
}
/* Change the link color on hover */
li a:hover {
  background-color: #555;
  color: white;
}
</pre>
<hr>
Add an "active" class to the current link to let the user know which page he/she is on:
<br>
<img src="https://i.imgur.com/Lyc5mvr.png">
<pre>
.active {
  background-color: #04AA6D;
  color: white;
}
</pre>
<hr>
Add <b>text-align:center</b> to <b>&lt;li&gt;</b> or <b>&lt;a&gt;</b> to center the links.
<br>
Add the <b>border</b> property to <b>&lt;ul&gt;</b> add a border around the navbar. If you also want borders inside the navbar, add a <b>border-bottom</b> to all <b>&lt;ul&gt;</b> elements, except for the last one:
<br>
<img src="https://i.imgur.com/9cceARX.png">
<pre>
ul {
  border: 1px solid #555;
}
li {
  text-align: center;
  border-bottom: 1px solid #555;
}
li:last-child {
  border-bottom: none;
}
</pre>
<hr>
Create a full-height, "sticky" side navigation:
<br>
<img src="https://i.imgur.com/XlhFvsj.png">
<pre>
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  width: 25%;
  background-color: #f1f1f1;
  height: 100%; /* Full height */
  position: fixed; /* Make it stick, even on scroll */
  overflow: auto; /* Enable scrolling if the sidenav has too much content */
}
</pre>
<b>Note:</b> This example might not work properly on mobile devices.
