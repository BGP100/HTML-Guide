The <b>&lt;track&gt;</b> tag specifies text tracks for <a href="audio.md">&lt;audio&gt;</a> or <a href="video.md">&lt;video&gt;</a> elements.
<br>
This element is used to specify subtitles, caption files or other files containing text, that should be visible when the media is playing.
<br>
Tracks are formatted in WebVTT format (.vtt files).
<pre>
&lt;video width="320" height="240" controls&gt;
  &lt;source src="forrest_gump.mp4" type="video/mp4"&gt;
  &lt;source src="forrest_gump.ogg" type="video/ogg"&gt;
  &lt;track src="fgsubtitles_en.vtt" kind="subtitles" srclang="en" label="English"&gt;
  &lt;track src="fgsubtitles_no.vtt" kind="subtitles" srclang="no" label="Norwegian"&gt;
&lt;/video&gt;
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
    <td>23.0</td>
    <td>10.0</td>
    <td>31.0</td>
    <td>6.0</td>
    <td>12.1</td>
  </tr>
</table>
<h1>Standard</h1>
The <b>&lt;track&gt;</b> tag supports the standard attributes.
<h1>Event</h1>
The <b>&lt;track&gt;</b> tag supports the event attributes.
<h1>Default CSS</h1>
None.
