<a href="/CSS/Lists/Styling.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/Tables/Size.md">Next &gt;</a>
<hr>
The look of an HTML table can be greatly improved with CSS:
<br>
<img src="https://i.imgur.com/l968yyt.jpg" width="69%">
<br>
To specify table borders in CSS, use the border property.
<br>
The example below specifies a solid border for <b>&lt;table&gt;</b>, <b>&lt;th&gt;</b>, and <b>&lt;td&gt;</b> elements: To specify table borders in CSS, use the border property.
<br>
The example below specifies a solid border for <b>&lt;table&gt;</b>, <b>&lt;th&gt;</b>, and <b>&lt;td&gt;</b> elements:
<br>
<img src="https://i.imgur.com/INwgzHz.jpg" width="20%">
<pre>
table, th, td {
  border: 1px solid;
}
</pre>
<h1>Full-Width</h1>
The table above might seem small in some cases. If you need a table that should span the entire screen (full-width), add <b>width: 100%</b> to the <b>&lt;table&gt;</b> element:
<br>
<img src="https://i.imgur.com/oPXqVQJ.jpg" width="90%">
<pre>
table {
  width: 100%;
}
</pre>
<h1>Collapse</h1>
The <b>border-collapse</b> property sets whether the table borders should be collapsed into a single border:
<br>
<img src="https://i.imgur.com/uAkltMf.jpg" width="90%">
<pre>
table {
  border-collapse: collapse;
}
</pre>
If you only want a border around the table, only specify the border property for <b>&lt;table&gt;</b>:
<img src="https://i.imgur.com/OIKadki.jpg" width="90%">
<pre>
table {
  border: 1px solid;
}
</pre>
