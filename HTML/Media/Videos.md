The HTML <b>&lt;video&gt;</b> element is used to show a video on a web page.
<h1>The Element</h1>
To show a video in HTML, use the <b>&lt;video&gt;</b> element:
<pre>
&lt;video width="320" height="240" controls&gt;
  &lt;source src="movie.mp4" type="video/mp4"&gt;
  &lt;source src="movie.ogg" type="video/ogg"&gt;
  Your browser does not support the video tag.
&lt;/video&gt;
</pre>
<h1>How it works?</h1>
The controls attribute adds video controls, like play, pause, and volume.
<br>
It is a good idea to always include width and height attributes. If height and width are not set, the page might flicker while the video loads.
<br>
The <b>&lt;source&gt;</b> element allows you to specify alternative video files which the browser may choose from. The browser will use the first recognized format.
<br>
The text between the <b>&lt;video&gt;</b> and <b>&lt;/video&gt;</b> tags will only be displayed in browsers that do not support the <b>&lt;video&gt;</b> element.
<h1>autoplay</h1>
To start a video automatically, use the autoplay attribute:
<pre>
&lt;video width="320" height="240" controls <b>autoplay</b>&gt;
  &lt;source src="movie.mp4" type="video/mp4"&gt;
  &lt;source src="movie.ogg" type="video/ogg"&gt;
  Your browser does not support the video tag.
&lt;/video&gt;
</pre>
Add <b>muted</b> after <b>autoplay</b> to let your video start playing automatically but muted:
<pre>
&lt;video width="320" height="240" controls autoplay <b>muted</b>&gt;
  &lt;source src="movie.mp4" type="video/mp4"&gt;
  &lt;source src="movie.ogg" type="video/ogg"&gt;
  Your browser does not support the video tag.
&lt;/video&gt;
</pre>
<h1>Browser Support</h1>
The numbers in the table specify the first browser version that fully supports the <b>&lt;video&gt;</b> element.
<table class="ws-table-all notranslate">
  <tr>
    <th>Browser</th>
    <td>Chrome</td>
    <td>Edge</td>
    <td>Firefox</td>
    <td>Safari</td>
    <td>Opera</td>
  </tr>
  <tr>
    <th>Version</th>
    <td>4.0</td>
    <td>9.0</td>
    <td>3.5</td>
    <td>4.0</td>
    <td>10.5</td>
  </tr>
</table>
<h1>Video Formats</h1>
There are three supported video formats: MP4, WebM, and Ogg. The browser support for the different formats is:
<table class="ws-table-all notranslate">
  <tr>
    <th>Browser</th>
    <th>MP4</th>
    <th>WebM</th>
    <th>Ogg</th>
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
    <td>NO</td>
    <td>YES</td>
    <td>YES</td>
  </tr>
</table>
<h2>Media Types</h2>
<table class="ws-table-all notranslate">
  <tr>
    <th>File Format</th>
    <th>Media Type</th>
  </tr>
  <tr>
    <td>MP4</td>
    <td>video/mp4</td>
  </tr>
  <tr>
    <td>WebM</td>
    <td>video/webm</td>
  </tr>
  <tr>
    <td>Ogg</td>
    <td>video/ogg</td>
  </tr>
</table>
<h1>Tags</h1>
<table class="ws-table-all notranslate">
<tr>
<th>Tag</th>
<th>Description</th>
</tr>
<tr>
<td>&lt;video&gt;</td>
<td>Defines a video or movie.</td>
</tr>
<tr>
<td>&lt;source&gt;</td>
<td>Defines multiple media resources for media elements, such as &lt;video&gt; and &lt;audio&gt;.</td>
</tr>
<tr>
<td>&lt;track&gt;</td>
<td>Defines text tracks in media players.</td>
</tr>
</table>
