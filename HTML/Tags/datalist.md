The <b>&lt;datalist&gt;</b> tag specifies a list of pre-defined options for an <b>&lt;input&gt;</b> element.
<br>
The <b>&lt;datalist&gt;</b> tag is used to provide an "autocomplete" feature for <b>&lt;input&gt;</b> elements. Users will see a drop-down list of pre-defined options as they input data.
<br>
The <b>&lt;datalist&gt;</b> element's id attribute must be equal to the <b>&lt;input&gt;</b> element's list attribute (this binds them together).
<pre>
&lt;label for="browser"&gt;Choose your browser from the list:&lt;/label&gt;
&lt;input list="browsers" name="browser" id="browser"&gt;
&lt;datalist id="browsers"&gt;
  &lt;option value="Edge"&gt;
  &lt;option value="Firefox"&gt;
  &lt;option value="Chrome"&gt;
  &lt;option value="Opera"&gt;
  &lt;option value="Safari"&gt;
&lt;/datalist&gt;
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
    <td>Version</td>
    <td>20.0</td>
    <td>10.0</td>
    <td>4.0</td>
    <td>12.1</td>
    <td>9.5</td>
  </tr>
</table>
<h1>Standard</h1>
The <b>&lt;data&gt;</b> tag supports the standard attributes.
<h1>Event</h1>
The <b>&lt;data&gt;</b> tag supports the event attributes.
