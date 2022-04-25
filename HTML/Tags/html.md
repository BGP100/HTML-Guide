The <b>&lt;html&gt;</b> tag represents the root of an HTML document.
<br>
The <b>&lt;html&gt;</b> tag is the container for all other HTML elements (except for the <a href="!DOCTYPE.md">&lt;!DOCTYPE&gt;</a> tag).
<br>
<b>Note:</b> You should always include the <b>lang</b> attribute inside the <b>&lt;html&gt;</b> tag, to declare the language of the Web page. This is meant to assist search engines and browsers.
<pre>
&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;head&gt;
  &lt;meta charset="utf-8"&gt;
  &lt;meta name="viewport" content="width=device-width, initial-scale=1.0"&gt;
  &lt;title&gt;Title of the document&lt;/title&gt;
  &lt;link rel="stylesheet" href="style.css" /&gt;
&lt;/head&gt;
&lt;body&gt;
  &lt;h1 class="hdr"&gt;This is a heading&lt;/h1&gt;
  &lt;p class="txt"&gt;This is a paragraph.&lt;/p&gt;
  &lt;script src="script.js"&gt;&lt;/script&gt;
&lt;/body&gt;
&lt;/html&gt;
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
<h1>Event</h1>
The <b>&lt;html&gt;</b> tag supports the event attributes.
<h1>Default CSS</h1>
Most browsers will display the <b>&lt;html&gt;</b> element with the following default values:
<pre>
html {
  display: block;
}
html:focus {
  outline: none;
}
</pre>
