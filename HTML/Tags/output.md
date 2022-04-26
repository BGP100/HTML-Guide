The <b>&lt;output&gt;</b> tag is used to represent the result of a calculation (like one performed by a script).
<pre>
&lt;form oninput="x.value=parseInt(a.value)+parseInt(b.value)"&gt;
  &lt;input type="range" id="a" value="50"&gt;
  +&lt;input type="number" id="b" value="25"&gt;
  =&lt;output name="x" for="a b"&gt;&lt;/output&gt;
&lt;/form&gt;
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
The <b>&lt;output&gt;</b> tag supports the standard attributes.
<h1>Event</h1>
The <b>&lt;output&gt;</b> tag supports the event attributes.
<h1>Default CSS</h1>
Most browsers will display the <b>&lt;output&gt;</b> element with the following default values:
<pre>
output {
  display: inline;
}
</pre>
