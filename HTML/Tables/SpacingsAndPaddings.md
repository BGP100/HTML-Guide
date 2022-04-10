<a href="/HTML/Tables/Headers.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/HTML/Tables/ColspanAndRowspan.md">Next &gt;</a>
<hr>
HTML tables can adjust the padding inside the cells, and also the space between the cells.
<br>
<img src="https://i.imgur.com/EF2WUd3.png">
<img src="https://i.imgur.com/PavmrlQ.png">
<h1>Cell padding</h1>
Cell padding is the space between the cell edges and the cell content.
<br>
By default the padding is set to 0.
<br>
To add padding on table cells, use the CSS padding property:
<pre>
th, td {
  padding: 15px;
}
</pre>
To add padding only above the content, use the padding-top property.
<br>
And the others sides with the padding-bottom, padding-left, and padding-right properties:
<pre>
th, td {
  padding-top: 10px;
  padding-bottom: 20px;
  padding-left: 30px;
  padding-right: 40px;
}
</pre>
<h1>Cell Spacing</h1>
Cell spacing is the space between each cell.
<br>
By default the space is set to 2 pixels.
<br>
To change the space between table cells, use the CSS border-spacing property on the table element:
<pre>
table {
  border-spacing: 30px;
}
</pre>
