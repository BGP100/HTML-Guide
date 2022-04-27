The <b>&lt;tfoot&gt;</b> tag is used to group footer content in an HTML table.
<br>
The <b>&lt;tfoot&gt;</b> element is used in conjunction with the <a href="thead.md">&lt;thead&gt;</a> and <a href="tbody.md">&lt;tbody&gt;</a> elements to specify each part of a table (footer, header, body).
<br>
Browsers can use these elements to enable scrolling of the table body independently of the header and footer. Also, when printing a large table that spans multiple pages, these elements can enable the table header and footer to be printed at the top and bottom of each page.
<br>
<b>Note:</b> The <b>&lt;tfoot&gt;</b> element must have one or more <a href="tr.md">&lt;tr&gt;</a> tags inside.
<br>
The <b>&lt;tfoot&gt;</b> tag must be used in the following context: As a child of a <a href="table.md">&lt;table&gt;</a> element, after any <a href="caption.md">&lt;caption&gt;</a>, <a href="colgroup.md">&lt;colgroup&gt;</a>, <a href="thead.md">&lt;thead&gt;</a>, and <a href="tbody.md">&lt;tbody&gt;</a> elements.
<br>
<b>Tip:</b> The <a href="thead.md">&lt;thead&gt;</a>, <a href="tbody.md">&lt;tbody&gt;</a>, and <b>&lt;tfoot&gt;</b> elements will not affect the layout of the table by default. However, you can use CSS to style these elements (see example below)!
<pre>
&lt;table&gt;
  &lt;thead&gt;
    &lt;tr&gt;
      &lt;th&gt;Month&lt;/th&gt;
      &lt;th&gt;Savings&lt;/th&gt;
    &lt;/tr&gt;
    &lt;tr&gt;
      &lt;td&gt;January&lt;/td&gt;
      &lt;td&gt;$100&lt;/td&gt;
    &lt;/tr&gt;
  &lt;/thead&gt;
  &lt;tbody&gt;
    &lt;tr&gt;
      &lt;th&gt;Month&lt;/th&gt;
      &lt;th&gt;Savings&lt;/th&gt;
    &lt;/tr&gt;
    &lt;tr&gt;
      &lt;td&gt;January&lt;/td&gt;
      &lt;td&gt;$100&lt;/td&gt;
    &lt;/tr&gt;
  &lt;/tbody&gt;
  &lt;tfoot&gt;
    &lt;tr&gt;
      &lt;th&gt;Month&lt;/th&gt;
      &lt;th&gt;Savings&lt;/th&gt;
    &lt;/tr&gt;
    &lt;tr&gt;
      &lt;td&gt;January&lt;/td&gt;
      &lt;td&gt;$100&lt;/td&gt;
    &lt;/tr&gt;
  &lt;/tfoot&gt;
&lt;/table&gt;
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
The <b>&lt;tfoot&gt;</b> tag supports the standard attributes.
<h1>Event</h1>
The <b>&lt;tfoot&gt;</b> tag supports the event attributes.
<h1>Default CSS</h1>
Most browsers will display the <b>&lt;tfoot&gt;</b> element with the following default values:
<pre>
tfoot {
  display: table-footer-group;
  vertical-align: middle;
  border-color: inherit;
}
</pre>
