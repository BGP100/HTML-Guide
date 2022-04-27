The <b>&lt;source&gt;</b> tag is used to specify multiple media resources for media elements, such as <a href="video.md">&lt;video&gt;</a>, <a href="audio.md">&lt;audio&gt;</a>, and <a href="picture.md">&lt;picture&gt;</a>.
<br>
The <b>&lt;source&gt;</b> tag allows you to specify alternative video/audio/image files which the browser may choose from, based on browser support or viewport width. The browser will choose the first <b>&lt;source&gt;</b> it supports.
<pre>
&lt;audio controls&gt;
  &lt;source src="movie.ogg" type="audio/ogg"&gt;
  &lt;source src="movie.mp3" type="audio/mp4"&gt;
  Your browser does not support the audio element.
&lt;/audio&gt;
</pre>
<pre>
&lt;video controls&gt;
  &lt;source src="horse.ogg" type="video/ogg"&gt;
  &lt;source src="horse.mp4" type="video/mpeg"&gt;
  Your browser does not support the video element.
&lt;/video&gt;
</pre>
<pre>
&lt;picture&gt;
  &lt;source media="(min-width:650px)" srcset="img_pink_flowers.jpg"&gt;
  &lt;source media="(min-width:465px)" srcset="img_white_flower.jpg"&gt;
  &lt;img src="img_orange_flowers.jpg" alt="Flowers" style="width:auto;"&gt;
&lt;/picture&gt;
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
    <td>4.0</td>
    <td>10.5</td>
  </tr>
</table>
<h1>Standard</h1>
The <b>&lt;source&gt;</b> tag supports the standard attributes.
<h1>Event</h1>
The <b>&lt;source&gt;</b> tag supports the event attributes.
<h1>Default CSS</h1>
None.
