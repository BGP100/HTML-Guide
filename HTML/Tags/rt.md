The <b>&lt;rt&gt;</b> tag defines an explanation or pronunciation of characters (for East Asian typography) in a ruby annotation.
<br>
Use <b>&lt;rt&gt;</b> together with <a href="ruby.md">&lt;ruby&gt;</a> and <a href="rp.md">&lt;rp&gt;</a>: The <a href="ruby.md">&lt;ruby&gt;</a> element consists of one or more characters that needs an explanation/pronunciation, and an <b>&lt;rt&gt;</b> element that gives that information, and an optional <a href="rp.md">&lt;rp&gt;</a> element that defines what to show for browsers that not support ruby annotations.
<pre>
&lt;ruby&gt;
漢 rt&gt;ㄏㄢˋ&lt;/rt&gt;
&lt;/ruby&gt;
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
    <td>5.0</td>
    <td>5.5</td>
    <td>38.0</td>
    <td>5.0</td>
    <td>15.0</td>
  </tr>
</table>
<h1>Standard</h1>
The <b>&lt;rt&gt;</b> tag supports the standard attributes.
<h1>Event</h1>
The <b>&lt;rt&gt;</b> tag supports the event attributes.
<h1>Default CSS</h1>
Most browsers will display the <b>&lt;rt&gt;</b> element with the following default values:
<pre>
rt {
  line-height: normal;
}
</pre>
