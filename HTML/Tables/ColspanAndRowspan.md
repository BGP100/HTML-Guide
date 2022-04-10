<a href="/HTML/Tables/SpacingsAndPaddings.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/HTML/Tables/Styling.md">Next &gt;</a>
<hr>
HTML tables can have cells that spans over multiple rows and/or columns.
<br>
<img src="https://i.imgur.com/rRou4yJ.png">
<img src="https://i.imgur.com/YyF57FP.png">
<img src="https://i.imgur.com/jZChc5H.png">
<h1>Colspan</h1>
To make a cell span over multiple columns, use the colspan attribute:
<pre>
&lt;table&gt;
  &lt;tr&gt;
    &lt;th colspan="2"&gt;Name&lt;/th&gt;
    &lt;th&gt;Age&lt;/th&gt;
  &lt;/tr&gt;
  &lt;tr&gt;
    &lt;td&gt;Jill&lt;/td&gt;
    &lt;td&gt;Smith&lt;/td&gt;
    &lt;td&gt;43&lt;/td&gt;
  &lt;/tr&gt;
  &lt;tr&gt;
    &lt;td&gt;Eve&lt;/td&gt;
    &lt;td&gt;Jackson&lt;/td&gt;
    &lt;td&gt;57&lt;/td&gt;
  &lt;/tr&gt;
&lt;/table&gt;
</pre>
<h1>Rowspan</h1>
To make a cell span over multiple rows, use the rowspan attribute:
<pre>
&lt;table&gt;
  &lt;tr&gt;
    &lt;th&gt;Name&lt;/th&gt;
    &lt;td&gt;Jill&lt;/td&gt;
  &lt;/tr&gt;
  &lt;tr&gt;
    &lt;th rowspan="2"&gt;Phone&lt;/th&gt;
    &lt;td&gt;555-1234&lt;/td&gt;
  &lt;/tr&gt;
  &lt;tr&gt;
    &lt;td&gt;555-8745&lt;/td&gt;
  &lt;/tr&gt;
&lt;/table&gt;
</pre>
