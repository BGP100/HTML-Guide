The <b>&lt;video&gt;</b> tag is used to embed video content in a document, such as a movie clip or other video streams.
<br>
The <b>&lt;video&gt;</b> tag contains one or more <a href="source.md">&lt;source&gt;</a> tags with different video sources. The browser will choose the first source it supports.
<br>
The text between the <b>&lt;video&gt;</b> and <b>&lt;/video&gt;</b> tags will only be displayed in browsers that do not support the <b>&lt;video&gt;</b> element.
<br>
There are three supported video formats in HTML: MP4, WebM, and OGG.
<table class="ws-table-all notranslate" id="table1">
  <tr>
    <th>Browser</th>
    <th>MP4</th>
    <th>WebM</th>
    <th>OGG</th>
  </tr>
  <tr>
    <td>Edge</td>
    <td>YES</td>
    <td>YES</td>
    <td>YES</td>
  </tr>
  <tr>
    <td>Chrome</td>
    <td>YES</td>
    <td>YES</td>
    <td>YES</td>
  </tr>
  <tr>
    <td>Firefox</td>
    <td>YES</td>
    <td>YES</td>
    <td>YES</td>
  </tr>
  <tr>
    <td>Safari</td>
    <td>YES</td>
    <td>YES</td>
    <td>NO</td>
  </tr>
  <tr>
    <td>Opera</td>
    <td>YES</td>
    <td>YES</td>
    <td>YES</td>
  </tr>
</table>
<pre>
&lt;video width="320" height="240" controls&lt;
  &lt;source src="movie.mp4" type="video/mp4"&lt;
  &lt;source src="movie.ogg" type="video/ogg"&lt;
  Your browser does not support the video tag.
&lt;/video&lt;
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
    <td>4.0</td>
    <td>9.0</td>
    <td>3.5</td>
    <td>3.1</td>
    <td>11.5</td>
  </tr>
</table>
<h1>Standard</h1>
The <b>&lt;video&gt;</b> tag supports the standard attributes.
<h1>Event</h1>
The <b>&lt;video&gt;</b> tag supports the event attributes.
<h1>Default CSS</h1>
None.
