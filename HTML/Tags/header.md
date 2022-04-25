The <b>&lt;header&gt;</b> element represents a container for introductory content or a set of navigational links.
<br>
A <b>&lt;header&gt;</b> element typically contains:
<ul>
  <li>One or more heading elements (&lt;h1&gt; ••• &lt;h6&gt;)</li>
  <li>Logo or icon</li>
  <li>Authorship information</li>
</ul>
<b>Note:</b> You can have several <b>&lt;header&gt;</b> elements in one HTML document. However, <b>&lt;header&gt;</b> cannot be placed within a <b>&lt;footer&gt;</b>, <b>&lt;address&gt;</b> or another <b>&lt;header&gt;</b> element.
<pre>
&lt;article&gt;
  &lt;header&gt;
    &lt;h1&gt;A heading here&lt;/h1&gt;
    &lt;p&gt;Posted by John Doe&lt;/p&gt;
    &lt;p&gt;Some additional information here&lt;/p&gt;
  &lt;/header&gt;
  &lt;p&gt;Lorem Ipsum dolor set amet....&lt;/p&gt;
&lt;/article&gt;
</pre>
<h1>Browser Support</h1>
<table class="ws-table-all notranslate">
  <tr>
    <th>&lt;header&gt;</th>
    <th>Chrome</th>
    <th>Edge</th>
    <th>Firefox</th>
    <th>Safari</th>
    <th>Opera</th>
  </tr>
  <tr>
    <td>Version</td>
    <td>6.0</td>
    <td>9.0</td>
    <td>4.0</td>
    <td>5.0</td>
    <td>11.1</td>
  </tr>
</table>
<h1>Default CSS</h1>
<pre>
header { 
  display: block;
}
</pre>
