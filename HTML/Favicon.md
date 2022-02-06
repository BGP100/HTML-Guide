You can use any image you like as your favicon. You can also create your own favicon on sites like https://favicon.cc/
<br>
A favicon image is displayed to the left of the page title in the browser tab, like this:
<br>
<img src="https://i.imgur.com/ywllKZ1.png" width="20%" height="auto">
<br>
To add a favicon to your website, either save your favicon image to the root directory of your webserver, or create a folder in the root directory called images, and save your favicon image in this folder. A common name for a favicon image is "favicon.ico".
<br>
Next, add a <b>link</b> element to your "index.html" file, after the <b>title</b> element, like this:
<pre>&lt;link rel="icon" type="image/x-icon" href="/images/favicon.ico"&gt;</pre>
Now, save the "index.html" file and reload it in your browser. Your browser tab should now display your favicon image to the left of the page title.
<h1>File Format Support</h1>
The following table shows the file format support for a favicon image:
<table class="ws-table-all notranslate">
  <tr>
    <th>Browser</th>
    <th>ICO</th>
    <th>PNG</th>
    <th>GIF</th>
    <th>JPEG</th>
    <th>SVG</th>
  </tr>
  <tr>
<td>Edge</td>
    <td>Yes</td>
    <td>Yes</td>
    <td>Yes</td>
    <td>Yes</td>
    <td>Yes</td>
  </tr>
  <tr>
    <td>Chrome</td>
    <td>Yes</td>
    <td>Yes</td>
    <td>Yes</td>
    <td>Yes</td>
    <td>Yes</td>
  </tr>
  <tr>
    <td>Firefox</td>
    <td>Yes</td>
    <td>Yes</td>
    <td>Yes</td>
    <td>Yes</td>
    <td>Yes</td>
  </tr>
  <tr>
    <td>Opera</td>
    <td>Yes</td>
    <td>Yes</td>
    <td>Yes</td>
    <td>Yes</td>
    <td>Yes</td>
  </tr>
  <tr>
    <td>Safari</td>
    <td>Yes</td>
    <td>Yes</td>
    <td>Yes</td>
    <td>Yes</td>
    <td>Yes</td>
  </tr>
</table>
