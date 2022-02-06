HTML tables can have different sizes for each column, row or the entire table.
<br>
<img src="https://i.imgur.com/tueJN6M.png">
<img src="https://i.imgur.com/0w8tsoA.png">
<img src="https://i.imgur.com/APg9ROf.png">
<br>
Use the style attribute with the width or height properties to specify the size of a table, row or column.
<h1>Width</h1>
To set the width of a table, add the style attribute to the <b>&lt;table&gt;</b> element:
<pre>
&lt;table class="ws-table-all notranslate" style="width:100%"&gt;
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
<b>Demo:</b>
<br>
<table class="ws-table-all notranslate" style="width:100%">
  <tr>
    <th>Firstname</th>
    <th>Lastname</th>
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
<br>
<b>Note:</b> Using a percentage as the size unit for a width means how wide will this element be compared to its parent element, which in this case is the <body> element.
<h1>Column Width</h1>
<img src="https://i.imgur.com/5NfpKNh.png">
<br>
To set the size of a specific column, add the style attribute on a &lt;th&gt; or &lt;td&gt; element:
<pre>
&lt;table style="width:100%"&gt;
  &lt;tr&gt;
    &lt;th style="width:70%">Firstname&lt;/th&gt;
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
<h1>Row Height</h1>
<img src="https://i.imgur.com/hvrvC3C.png">
<br>
To set the height of a specific row, add the style attribute on a table row element:
<pre>
&lt;table style="width:100%"&gt;
  &lt;tr&gt;
    &lt;th&gt;Firstname&lt;/th&gt;
    &lt;th&gt;Lastname&lt;/th&gt;
    &lt;th&gt;Age&lt;/th&gt;
  &lt;/tr&gt;
  &lt;tr style="height:200px"&gt;
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
