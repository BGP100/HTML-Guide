The <b>&lt;audio&gt;</b> tag is used to embed sound content in a document, such as music or other audio streams.
<br>
The <b>&lt;audio&gt;</b> tag contains one or more <b>&lt;source&gt;</b> tags with different audio sources. The browser will choose the first source it supports.
<br>
The text between the <b>&lt;audio&gt;</b> and <b>&lt;/audio&gt;</b> tags will only be displayed in browsers that do not support the <b>&lt;audio&gt;</b> element.
<br>
There are three supported audio formats in HTML: MP3, WAV, and OGG.
<table class="ws-table-all notranslate" id="table1">
  <tr>
    <th>Browser</th>
    <th>MP3</th>
    <th>WAV</th>
    <th>OGG</th>
  </tr>
  <tr>
    <td>Edge</td>
    <td>YES</td>
    <td>YES <code>*</code></td>
    <td>YES <code>*</code></td>
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
<code>*</code> From Edge 79
<audio controls>
  <source src="horse.mp3" type="audio/mpeg">
  <source src="horse.ogg" type="audio/ogg">
  Your browser does not support the audio tag.
</audio>
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
    <td>4.0</td>
    <td>11.5</td>
  </tr>
</table>
<h1>Standard</h1>
The <b>&lt;audio&gt;</b> tag supports the standard attributes.
<h1>Event</h1>
The <b>&lt;audio&gt;</b> tag supports the event attributes.
<h1>Default CSS</h1>
None.
