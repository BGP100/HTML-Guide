<a href="/HTML/Graphics/Canvas/Clock/5-Start.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/HTML/Graphics/SVG/IntoHTML.md">Next &gt;</a>
<hr>
SVG defines vector-based graphics in XML format.
<h1>What is it?</h1>
<ul>
  <li>SVG stands for Scalable Vector Graphics.</li>
  <li>SVG is used to define graphics for the Web.</li>
  <li>SVG is a W3C recommendation.</li>
</ul>
<h1>The Element</h1>
The HTML <b>&lt;svg&gt;</b> element is a container for SVG graphics.
<br>
SVG has several methods for drawing paths, boxes, circles, text, and graphic images.
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
    <td>3.0</td>
    <td>3.2</td>
    <td>10.1</td>
  </tr>
</table>
<h1>Example</h1>
<img src="https://i.imgur.com/oVlYcHQ.jpg" width="100" height="100">
<pre>&lt;svg width="100" height="100"&gt;&lt;circle cx="50" cy="50" r="40" stroke="green" stroke-width="4" fill="yellow" /&gt;&lt;/svg&gt;</pre>
<h1>Differences Between SVG and Canvas</h1>
SVG is a language for describing 2D graphics in XML.
<br>
Canvas draws 2D graphics, on the fly (with a JavaScript).
<br>
SVG is XML based, which means that every element is available within the SVG DOM. You can attach JavaScript event handlers for an element.
<br>
In SVG, each drawn shape is remembered as an object. If attributes of an SVG object are changed, the browser can automatically re-render the shape.
<br>
Canvas is rendered pixel by pixel. In canvas, once the graphic is drawn, it is forgotten by the browser. If its position should be changed, the entire scene needs to be redrawn, including any objects that might have been covered by the graphic.
<hr>
The table below shows some important differences between Canvas and SVG:
<table class="ws-table-all notranslate">
  <tr>
    <th></th>
    <th>Canvas</th>
    <th>SVG</th>              
  </tr>
  <tr>
    <td>Resolution</td>
    <td>Resolution dependent</td>
    <td>Resolution independent</td>
  </tr>
  <tr>
    <td>Event Handlers Support</td>
    <td>No support for event handlers</td>
    <td>Support for event handlers</td>
  </tr>
  <tr>
    <td>Text Rendering</td>
    <td>Poor text rendering capabilities</td>
    <td>Best suited for applications with large rendering areas (like Google Maps)</td>
  </tr>
  <tr>
    <td>Saving Proccess</td>
    <td>You can save the resulting image as .png or .jpg</td>
    <td>Slow rendering if complex (anything that uses the DOM a lot will be slow)</td>
  </tr>
  <tr>
    <td>App-Suited</td>
    <td>Well suited for graphic-intensive games</td>
    <td>Not suited for game applications</td>
  </tr>
</table>
