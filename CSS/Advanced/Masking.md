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
Here is the mask image (a PNG image) we will use:
<br>
<img src="https://i.imgur.com/4Wy6lNA.webp" width="40%">
<br>
<img src="https://i.imgur.com/ohAZbfM.jpg" width="100%">
