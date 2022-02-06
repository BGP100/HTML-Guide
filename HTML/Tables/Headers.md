HTML tables can have headers for each column or row, or for many columns/rows.
<br>
<img src="https://i.imgur.com/IkLo3ac.png">
<img src="https://i.imgur.com/XSiZyDK.png">
<img src="https://i.imgur.com/3KSAaae.png">
<img src="https://i.imgur.com/fOIc525.png">
<br>
Table headers are defined with th elements, each th element represents a table cell.
<pre>
&lt;table class="ws-table-all notranslate"&gt;
  &lt;tr&gt;
    &lt;th&gt;Firstname&lt;/th&gt;
    &lt;th&gt;Lastname&lt;/th&gt;
    &lt;th&gt;Age&lt;/th&gt;
  &lt;/tr&gt;
  &lt;tr&gt;
    &lt;td&gt;Jill&lt;/td&gt;
    &lt;td&gt;Smith&lt;/td&gt;
    &lt;td&gt;50&lt;/td&gt;
  &lt;/tr&gt;
  &lt;tr&gt;
    &lt;td&gt;Eve&lt;/td&gt;
    &lt;td&gt;Jackson&lt;/td&gt;
    &lt;td&gt;94&lt;/td&gt;
  &lt;/tr&gt;
&lt;/table&gt;
</pre>
<h1>Vertical Headers</h1>
To use the first column as table headers, define the first cell in each row as a th element:
<pre>
&lt;table class="ws-table-all notranslate"&gt;
  &lt;tr&gt;
    &lt;th&gt;Firstname&lt;/th&gt;
    &lt;td&gt;Jill&lt;/td&gt;
    &lt;td&gt;Eve&lt;/td&gt;
  &lt;/tr&gt;
  &lt;tr&gt;
    &lt;th&gt;Lastname&lt;/th&gt;
    &lt;td&gt;Smith&lt;/td&gt;
    &lt;td&gt;Jackson&lt;/td&gt;
  &lt;/tr&gt;
  &lt;tr&gt;
    &lt;th&gt;Age&lt;/th&gt;
    &lt;td&gt;94&lt;/td&gt;
    &lt;td&gt;50&lt;/td&gt;
  &lt;/tr&gt;
&lt;/table&gt;
</pre>
<h1>Align Headers</h1>
By default, table headers are bold and centered:
<img src="https://i.imgur.com/5RyQRvJ.png">
To left-align the table headers, use the CSS text-align property:
<pre>
th {
  text-align: left;
}
</pre>
<h1>Header for Multiple Columns</h1>
You can have a header that spans over two or more columns.
<table class="ws-table-all notranslate">
  <tr>
    <th colspan="2">Name</th>
    <th>Age</th>
  </tr>
  <tr>
    <td>Jill</td>
    <td>Smith</td>
    <td>50</td>
  </tr>
  <tr>
    <td>Eve</td>
    <td>Jackson</td>
    <td>94</td>
  </tr>
</table>
To do this, use the colspan attribute on the <b>&lt;th&gt;</b> element:
<pre>
&lt;table class="ws-table-all notranslate"&gt;
  &lt;tr&gt;
    &lt;th colspan="2"&gt;Name&lt;/th&gt;
    &lt;th&gt;Age&lt;/th&gt;
  &lt;/tr&gt;
  &lt;tr&gt;
    &lt;td&gt;Jill&lt;/td&gt;
    &lt;td&gt;Smith&lt;/td&gt;
    &lt;td&gt;50&lt;/td&gt;
  &lt;/tr&gt;
  &lt;tr&gt;
    &lt;td&gt;Eve&lt;/td&gt;
    &lt;td&gt;Jackson&lt;/td&gt;
    &lt;td&gt;94&lt;/td&gt;
  &lt;/tr&gt;
&lt;/table&gt;
</pre>
<h1>Captions</h1>
You can add a caption that serves as a heading for the entire table.
<br>
<table width="100%">
  <caption>Monthly savings</caption>
  <tr>
    <th>Month</th>
    <th>Savings</th>
  </tr>
  <tr>
    <td>January</td>
    <td>$100</td>
  </tr>
  <tr>
    <td>February</td>
    <td>$50</td>
  </tr>
</table>
To add a caption to a table, use the <b>&lt;caption&gt;</b> tag:
<pre>
&lt;table style="width:100%"&gt;
  &lt;caption&gt;Monthly savings&lt;/caption&gt;
  &lt;tr&gt;
    &lt;th&gt;Month&lt;/th&gt;
    &lt;th&gt;Savings&lt;/th&gt;
  &lt;/tr&gt;
  &lt;tr&gt;
    &lt;td&gt;January&lt;/td&gt;
    &lt;td&gt;$100&lt;/td&gt;
  &lt;/tr&gt;
  &lt;tr&gt;
    &lt;td&gt;February&lt;/td&gt;
    &lt;td&gt;$50&lt;/td&gt;
  &lt;/tr&gt;
&lt;/table&gt;
</pre>
<b>Note:</b> The &lt;caption&gt; tag should be inserted immediately after the &lt;table&gt; tag.
