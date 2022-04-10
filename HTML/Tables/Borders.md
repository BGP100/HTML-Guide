<a href="/HTML/Tables/Main.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/HTML/Tables/Sizes.md">Next &gt;</a>
<hr>
HTML tables can have borders of different styles and shapes.
<h1>Double Borders</h1>
When you add a border to a table, you also add borders around each table cell:
<br>
<img src="https://i.imgur.com/xA6S3Ws.png">
<br>
To add a border, use the CSS border property on table, th, and td elements:
<pre>
table, th, td {
  border: 1px solid black;
}
</pre>
<h1>Collapsed Borders</h1>
To avoid having double borders like in the example above, set the CSS border-collapse property to collapse.
<br>
This will make the borders collapse into a single border:
<br>
<img src="https://i.imgur.com/ELq9S34.png">
<pre>
table, th, td {
  border: 1px solid black;
  border-collapse: collapse;
}
</pre>
<h1>Styled Borders</h1>
If you set a background color of each cell, and give the border a white color (the same as the document background), you get the impression of an invisible border:
<br>
<img src="https://i.imgur.com/AakFq8C.png">
<pre>
table, th, td {
  border: 1px solid white;
  border-collapse: collapse;
}
th, td {
  background-color: #96D4D4;
}
</pre>
<h1>Round Borders</h1>
With the border-radius property, the borders get rounded corners:
<br>
<img src="https://i.imgur.com/vcNLKVn.png">
<pre>
table, th, td {
  border: 1px solid black;
  border-radius: 10px;
}
</pre>
Skip the border around the table by leaving out table from the css selector:
<br>
<img src="https://i.imgur.com/hvj6tC3.png">
<h1>Dotted Borders</h1>
With the border-style property, you can set the appereance of the border.
<br>
<img src="https://i.imgur.com/l6q4KPe.png">
<pre>
th, td {
  border-style: dotted;
}
</pre>
<h1>Border Color</h1>
With the border-color property, you can set the color of the border.
<br>
<img src="https://i.imgur.com/kAP9IZZ.png">
<pre>
th, td {
  border-color: #96D4D4;
}
</pre>
<h1>Allowed Borders</h1>
The following values are allowed:
<ul>
  <li>Dotted <img src="https://i.imgur.com/SUSnZug.png"></li>
  <li>Dashed <img src="https://i.imgur.com/rP4yfRj.png"></li>
  <li>Solid <img src="https://i.imgur.com/6ZplU08.png"></li>
  <li>Double <img src="https://i.imgur.com/mRp9Lzc.png"></li>
  <li>Groove <img src="https://i.imgur.com/CmM2Blp.png"></li>
  <li>Ridge <img src="https://i.imgur.com/nNdRgmF.png"></li>
  <li>Inset <img src="https://i.imgur.com/u3LvjLP.png"></li>
  <li>Outset <img src="https://i.imgur.com/0Vvv07W.png"></li>
  <li>Hidden</li>
  <li>None</li>
</ul>
