The <b>&lt;embed&gt;</b> tag defines a container for an external resource, such as a web page, a picture, a media player, or a plug-in application.
<br><br>
<b>Warnings</b>
<br>
Most browsers no longer support Java Applets and Plug-ins.
<br>
ActiveX controls are no longer supported in any browsers.
<br>
The support for Shockwave Flash has also been turned off in modern browsers.
<br><br>
<b>Suggestions</b>
<br>
To display a picture, it is better to use the <b>&lt;img&gt;</b> tag.
<br>
To display HTML, it is better to use the <b>&lt;iframe&gt;</b> tag.
<br>
To display video or audio, it is better to use the <b>&lt;video&gt;</b> and <b>&lt;audio&gt;</b> tags.
<pre>&lt;embed type="image/jpg" src="pic_trulli.jpg" width="300" height="200"&gt;</pre>
<pre>&lt;embed type="text/html" src="snippet.html" width="500" height="200"&gt;</pre>
<pre>&lt;embed type="video/webm" src="video.mp4" width="400" height="300"&gt;</pre>
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
<h1>Standard</h1>
The <b>&lt;embed&gt;</b> tag supports the standard attributes.
<h1>Event</h1>
The <b>&lt;embed&gt;</b> tag supports the event attributes.
<h1>Default CSS</h1>
Most browsers will display the <b>&lt;embed&gt;</b> element with the following default values:
<pre>
embed:focus {
  outline: none;
}
</pre>
