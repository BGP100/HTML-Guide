<img src="https://i.imgur.com/Gn9yLP6.jpg" width="25%">
<br>
The HTML <b>&lt;canvas&gt;</b> element is used to draw graphics on a web page.
<br>
The graphic to the left is created with <b>&lt;canvas&gt;</b>. It shows four elements: a red rectangle, a gradient rectangle, a multicolor rectangle, and a multicolor text.
<h1>What is it?</h1>
The HTML <b>&lt;canvas&gt;</b> element is used to draw graphics, on the fly, via JavaScript.
<br>
The <b>&lt;canvas&gt;</b> element is only a container for graphics. You must use JavaScript to actually draw the graphics.
<br>
Canvas has several methods for drawing paths, boxes, circles, text, and adding images.
<h1>Browser Support</h1>
The numbers in the table specify the first browser version that fully supports the <b>&lt;canvas&gt;</b> element.
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
    <td>2.0</td>
    <td>3.1</td>
    <td>9.0</td>
  </tr>
</table>
<h1>Example</h1>
A canvas is a rectangular area on an HTML page. By default, a canvas has no border and no content.
<br>
The markup looks like this:
<pre>&lt;canvas id="myCanvas" width="200" height="100"&gt;&lt;/canvas&gt;</pre>
<b><i>Note:</i></b> Always specify an <b>id</b> attribute (to be referred to in a script), and a <b>width</b> and <b>height</b> attribute to define the size of the canvas. To add a border, use the <b>style</b> attribute.
<br>
Here is an example of a basic, empty canvas:
<br>
<img src="https://i.imgur.com/BwoXDFW.jpg" width="200" height="100">
<pre>&lt;canvas id="myCanvas" width="200" height="100" style="border:1px solid #000000;"&gt;&lt;/canvas&gt;
