The <b>&lt;head&gt;</b> element is a container for metadata (data about data) and is placed between the <b>&lt;html&gt;</b> tag and the <b>&lt;body&gt;</b> tag.
<br>
Metadata is data about the HTML document. Metadata is not displayed.
<br>
Metadata typically define the document title, character set, styles, scripts, and other meta information.
<br>
The following elements can go inside the <b>&lt;head&gt;</b> element:
<ul>
  <li><a href="title.md">&lt;title&gt;</a> (required in every HTML document)</li>
  <li><a href="style.md">&lt;style&gt;</a></li>
  <li><a href="link.md">&lt;link&gt;</a></li>
  <li><a href="meta.md">&lt;meta&gt;</a></li>
  <li><a href="base.md">&lt;base&gt;</a></li>
  <li><a href="script.md">&lt;script&gt;</a></li>
  <li><a href="noscript.md">&lt;noscript&gt;</a></li>
</ul>
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
The <b>&lt;head&gt;</b> tag supports the event attributes.
<h1>Default CSS</h1>
Most browsers will display the <b>&lt;head&gt;</b> element with the following default values:
<pre>
head {
  display: none;
}
</pre>
