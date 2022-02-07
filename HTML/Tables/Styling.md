Use CSS to make your tables look better.
<h1>Zebra Stripes</h1>
If you add a background color on every other table row, you will get a nice zebra stripes effect.
<br>
<img src="https://i.imgur.com/oK2qvtm.png">
<br>
To style every other table row element, use the :nth-child(even) selector like this:
<pre>
tr:nth-child(even) {
  background-color: #D6EEEE;
}
</pre>
<h1>Vertical Zebra Stripes</h1>
To make vertical zebra stripes, style every other <em>column</em>, instead of every other row.
<br>
<img src="https://i.imgur.com/ICDSrcK.png">
<br>
Set the :nth-child(even) for table data elements like this:
<pre>
td:nth-child(even), th:nth-child(even) {
  background-color: #D6EEEE;
}
</pre>
<h1>Combine Vertical and Horizontal Zebra Stripes</h1>
You can combine the styling from the two examples above and you will have stripes on every other row and every other column.
<br>
If you use a transparent color you will get an overlapping effect.
<br>
<img src="https://i.imgur.com/LCbeW7X.png">
<br>
Use an rgba() color to specify the transparency of the color:
<pre>
tr:nth-child(even) {
  background-color: rgba(150, 212, 212, 0.4);
}
<p></p>
th:nth-child(even),td:nth-child(even) {
  background-color: rgba(150, 212, 212, 0.4);
}
</pre>
<h1>Horizontal Dividers</h1>
<img src="https://i.imgur.com/UzoOYOP.png">
<br>
If you specify borders only at the bottom of each table row, you will have a table with horizontal dividers.
<br>
Add the border-bottom property to all tr elements to get horizontal dividers:
<pre>
tr {
  border-bottom: 1px solid #ddd;
}
</pre>
<h1>Hoverable Table</h1>
Sorry but GitHub cant make styles so just go to the coding part.
<br>
Use the :hover selector on tr to highlight table rows on mouse over:
<img src="https://i.imgur.com/UzoOYOP.png">
<pre>
tr {
  border-bottom: 1px solid #ddd;
}
<p></p>
tr:hover {
  background-color: #D6EEEE;
}
</pre>
