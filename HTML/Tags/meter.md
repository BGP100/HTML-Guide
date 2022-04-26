The <b>&lt;meter&gt;</b> tag defines a scalar measurement within a known range, or a fractional value. This is also known as a gauge.
<br>
<b>Examples:</b> Disk usage, the relevance of a query result, etc.
<br>
<b>Note:</b> The <b>&lt;meter&gt;</b> tag should not be used to indicate progress (as in a progress bar). For progress bars, use the <a href="progress.md">&lt;progress&gt;</a> tag.
<br>
<b>Tip:</b> Always add the <a href="label.md">&lt;label&gt;</a> tag for best accessibility practices!
<pre>
&lt;label for="disk_c"&gt;Disk usage C:&lt;/label&gt;
&lt;meter id="disk_c" value="2" min="0" max="10"&gt;2 out of 10&lt;/meter&gt;&lt;br&gt;
&lt;label for="disk_d"&gt;Disk usage D:&lt;/label&gt;
&lt;meter id="disk_d" value="0.6"&gt;60%&lt;/meter&gt;
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
    <td>8.0</td>
    <td>13.0</td>
    <td>16.0</td>
    <td>6.0</td>
    <td>11.5</td>
  </tr>
</table>
<h1>Standard</h1>
The <b>&lt;meter&gt;</b> tag supports the standard attributes.
<h1>Event</h1>
The <b>&lt;meter&gt;</b> tag supports the event attributes.
<h1>Default CSS</h1>
None.
