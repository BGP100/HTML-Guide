The <b>&lt;colgroup&gt;</b> tag specifies a group of one or more columns in a table for formatting.
<br>
The <b>&lt;colgroup&gt;</b> tag is useful for applying styles to entire columns, instead of repeating the styles for each cell, for each row.
<br>
<b>Note:</b> The <b>&lt;colgroup&gt;</b> tag must be a child of a <a href="table.md">&lt;table&gt;</a> element, after any <a href="caption.md">&lt;caption&gt;</a> elements and before any <a href="thead.md">&lt;thead&gt;</a>, <a href="tbody.md">&lt;tbody&gt;</a>, <a href="tfoot.md">&lt;tfoot&gt;</a>, and <b>&lt;colgroup&gt;</b> elements.
<br>
<b>Tip:</b> To define different properties to a column within a <b>&lt;colgroup&gt;</b>, use the <a href="col.md">&lt;col&gt;</a> tag within the <b>&lt;colgroup&gt;</b> tag.
<pre>
&lt;colgroup&gt;
  &lt;col span="2" style="background-color:red"&gt;
  &lt;col style="background-color:yellow"&gt;
&lt;/colgroup&gt;
</pre>
<h1>Browser Support</h1>
<table class="ws-table-all notranslate">
  <tr>
    <th>Browser</th>
    <th>Chrome</th>
    <th>Edge</th>
    <th>Firefox</th>
    <th>Safari</th>
    <th>Opera</th>
  </tr>
  <tr>
    <td>Compatibility</td>
    <td>Yes</td>
    <td>Yes</td>
    <td>Yes</td>
    <td>Yes</td>
    <td>Yes</td>
  </tr>
</table>
<h1>Standard</h1>
The <b>&lt;colgroup&gt;</b> tag supports the standard attributes.
<h1>Event</h1>
The <b>&lt;colgroup&gt;</b> tag supports the event attributes.
<h1>Default CSS</h1>
Most browsers will display the <b>&lt;colgroup&gt;</b> element with the following default values:
<pre>
colgroup {
  display: table-column-group;
}
</pre>
