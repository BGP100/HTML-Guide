<a href="/CSS/Tables/Alignment.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/Tables/Responsive.md">Next &gt;</a>
<hr>
<h1>Padding</h1>
To control the space between the border and the content in a table, use the padding property on <b>&lt;td&gt;</b> and <b>&lt;th&gt;</b> elements:
<br>
<img src="https://i.imgur.com/orX44Og.jpg" width="69%">
<pre>
th, td {
  padding: 15px;
  text-align: left;
}
</pre>
<h1>Horizontal Dividers</h1>
<img src="https://i.imgur.com/bxuwQ7b.jpg" width="69%">
Add the <b>border-bottom</b> property to <b>&lt;td&gt;</b> and <b>&lt;th&gt;</b> for horizontal dividers:
<pre>
th, td {
  border-bottom: 1px solid #ddd;
}
</pre>
<h1>Hover</h1>
Use the <b>:hover</b> selector on <b>&lt;tr&gt;</b> to highlight table rows on mouse over:
<br>
<img src="https://i.imgur.com/bxuwQ7b.jpg" width="69%">
<pre>tr:hover {background-color: coral;}</pre>
<h1>Stipes</h1>
<img src="https://i.imgur.com/7Z1MeoJ.jpg" width="69%">
For zebra-striped tables, use the <b>nth-child()</b> selector and add a <b>background-color</b> to all even (or odd) table rows:
<pre>tr:nth-child(even) {background-color: #f2f2f2;}</pre>
<h1>Color</h1>
The example below specifies the background color and text color of <b>&lt;th&gt;</b> elements:
<img src="https://i.imgur.com/00wwDlk.jpg" width="69%">
<pre>
th {
  background-color: #04AA6D;
  color: white;
}
</pre>
