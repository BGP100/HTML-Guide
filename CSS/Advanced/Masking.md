With CSS masking you create a mask layer to place over an element to partially or fully hide portions of the element.
<hr>
The CSS <b>mask-image</b> property specifies a mask layer image.
<h1>Browser Support</h1>
<b>Note:</b> Most browsers only have partial support for CSS masking. You will need to use the -webkit- prefix in addition to the standard property in most browsers.
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
    <td>79.0</td>
    <td>53.0</td>
    <td>4.0</td>
    <td>15.0</td>
  </tr>
</table>
<h1>Use an Image as Mask Layer</h1>
To use a PNG or an SVG image as the mask layer, use a url() value to pass in the mask layer image.
<br>
The mask image needs to have a transparent or semi-transparent area. Black indicates fully transparent.
<br>
<pre>
.mask1 {
  -webkit-mask-image: url(w3logo.png);
  mask-image: url(w3logo.png);
  -webkit-mask-repeat: no-repeat;
  mask-repeat: no-repeat; 
}
</pre>
<b>Explained:</b>
<br>
The <b>mask-image</b> property specifies the image to be used as a mask layer for an element.
<br>
The <b>mask-repeat</b> property specifies if or how a mask image will be repeated. The <b>no-repeat</b> value indicates that the mask image will not be repeated (the mask image will only be shown once).
<h1>With Gradients</h1>
Here, we use a linear-gradient as the mask layer for our image. This linear gradient goes from top (black) to bottom (transparent):
<br>
<img src="https://i.imgur.com/6wb9sjM.jpg" width="100">
<pre>
mask1 {
  -webkit-mask-image: linear-gradient(black, transparent);
  mask-image: linear-gradient(black, transparent);
}
</pre>
<hr>
Here, we use a radial-gradient (shaped as a circle) as the mask layer for our image:
<br>
<img src="https://i.imgur.com/gtL5TyO.jpg" width="100">
<pre>
mask2 {
  -webkit-mask-image: radial-gradient(circle, black 50%, rgba(0, 0, 0, 0.5) 50%);
  mask-image: radial-gradient(circle, black 50%, rgba(0, 0, 0, 0.5) 50%);
}
</pre>
<h1>SVG Masks</h1>
<img src="https://i.imgur.com/RRw6yDK.jpg" width="40%">
<pre>
&lt;svg width="600" height="400"&gt;
  &lt;mask id="svgmask1"&gt;
    &lt;polygon fill="#ffffff" points="200 0, 400 400, 0 400"&gt;&lt;/polygon&gt;
  &lt;/mask&gt;
  &lt;image xmlns:xlink="http://www.w3.org/1999/xlink" xlink:href="img_5terre.jpg" mask="url(#svgmask1)"&gt;&lt;/image&gt;
&lt;/svg&gt;
</pre>
<hr>
<img src="https://i.imgur.com/Nj21pOL.jpg" width="40%">
<pre>
&lt;svg width="600" height="400"&gt;
  &lt;mask id="svgmask1"&gt;
    &lt;polygon fill="#ffffff" points="200 0, 400 400, 0 400"&gt;&lt;/polygon&gt;
  &lt;/mask&gt;
  &lt;image xmlns:xlink="http://www.w3.org/1999/xlink" xlink:href="img_5terre.jpg" mask="url(#svgmask2)"&gt;&lt;/image&gt;
&lt;/svg&gt;
</pre>
<img src="https://i.imgur.com/OCl4HMz.jpg" width="40%">
<pre>
&lt;svg width="600" height="400"&gt;
  &lt;mask id="svgmask1"&gt;
    &lt;circle fill="#ffffff" cx="75" cy="75" r="75"&gt;&lt;/circle&gt;
    &lt;circle fill="#ffffff" cx="80" cy="260" r="75"&gt;&lt;/circle&gt;
    &lt;circle fill="#ffffff" cx="270" cy="160" r="75"&gt;&lt;/circle&gt;
  &lt;/mask&gt;
  &lt;image xmlns:xlink="http://www.w3.org/1999/xlink" xlink:href="img_5terre.jpg" mask="url(#svgmask2)"&gt;&lt;/image&gt;
&lt;/svg&gt;
</pre>
