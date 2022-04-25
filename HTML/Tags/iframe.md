The <b>&lt;iframe&gt;</b> tag specifies an inline frame.
<br>
An inline frame is used to embed another document within the current HTML document.
<br>
<b><i>Tip:</i></b> Use CSS to style the <b>&lt;iframe&gt;</b> (see example below). 
<br>
<b><i>Tip:</i></b> It is a good practice to always include a title attribute for the <b>&lt;iframe&gt;</b>. This is used by screen readers to read out what the content of the <b>&lt;iframe&gt;</b> is.
<br>
<b><i>Tip:</i></b> <a href="embed.md">&lt;embed&gt;</a> is like <b>&lt;iframe&gt;</b> but without a frame border (you can also remove the border with css).
<pre>&lt;iframe src="https://bledy-guides.repl.co" title="BledyGuides"&gt;&lt;/iframe&gt;</pre>
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
<h1>Global</h1>
The <b>&lt;iframe&gt;</b> tag supports the global attributes.
<h1>Event</h1>
The <b>&lt;iframe&gt;</b> tag supports the event attributes.
<h1>Default CSS</h1>
Most browsers will display the <b>&lt;iframe&gt;</b> element with the following default values:
<pre>
iframe:focus {
  outline: none;
}
iframe[seamless] {
  display: block;
}
</pre>
