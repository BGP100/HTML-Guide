The <b>text-align</b> property sets the horizontal alignment (like left, right, or center) of the content in <b>&lt;th&gt;</b> or <b>&lt;td&gt;</b>.
<br>
By default, the content of <b>&lt;th&gt;</b> elements are center-aligned and the content of <b>&lt;td&gt;</b> elements are left-aligned.
<br>
To center-align the content of <b>&lt;th&gt;</b> elements as well, use <b>text-align: center</b>:
<br>
<img src="https://i.imgur.com/FIIN5f2.jpg" width="69%">
<pre>
td {
  text-align: center;
}
</pre>
To left-align the content, force the alignment of <b>&lt;th&gt;</b> elements to be left-aligned, with the <b>text-align: left</b> property:
<img src="https://i.imgur.com/eX5Mfop.jpg" width="69%">
<pre>
th {
  text-align: left;
}
</pre>
<h1>Vertical</h1>
The <b>vertical-align</b> property sets the vertical alignment (like top, bottom, or middle) of the content in <b>&lt;th&gt;</b> or <b>&lt;td&gt;</b>.
<br>
By default, the vertical alignment of the content in a table is middle (for both <b>&lt;th&gt;</b> and <b>&lt;td&gt;</b> elements).
<br>
The following example sets the vertical text alignment to bottom for <b>&lt;td&gt;</b> elements:
<br>
<img src="https://i.imgur.com/com0wxZ.jpg" width="69%">
<pre>
td {
  height: 50px;
  vertical-align: bottom;
}
</pre>
