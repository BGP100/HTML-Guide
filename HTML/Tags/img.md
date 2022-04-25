The <b>&lt;img&gt;</b> tag is used to embed an image in an HTML page.
<br>
Images are not technically inserted into a web page; images are linked to web pages. The <img> tag creates a holding space for the referenced image.
<br>
The <b>&lt;img&gt;</b> tag has two required attributes:
<ul>
  <li>src - Specifies the path to the image</li>
  <li>alt - Specifies an alternate text for the image, if the image for some reason cannot be displayed</li>
</ul>
Note: Also, always specify the width and height of an image. If width and height are not specified, the page might flicker while the image loads.
<br>
<b><i>Tip:</i></b> To link an image to another document, simply nest the <b>&lt;img&gt;</b> tag inside an <a href="a.md">&lt;a&gt;</a> tag (see example below).
<pre>&lt;img src="img_girl.jpg" alt="Girl in a jacket" width="500" height="600"&gt;</pre>
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
The <b>&lt;img&gt;</b> tag supports the standard attributes.
<h1>Event</h1>
The <b>&lt;img&gt;</b> tag supports the event attributes.
<h1>Default CSS</h1>
Most browsers will display the <b>&lt;img&gt;</b> element with the following default values:
<pre>
img {
  display: inline-block;
}
</pre>
