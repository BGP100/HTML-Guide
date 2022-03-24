The <b>&lt;canvas&gt;</b> tag is used to draw graphics, on the fly, via scripting (usually JavaScript).
<br>
The <b>&lt;canvas&gt;</b> tag is transparent, and is only a container for graphics, you must use a script to actually draw the graphics.
<br>
Any text inside the <b>&lt;canvas&gt;</b> element will be displayed in browsers with JavaScript disabled and in browsers that do not support <b>&lt;canvas&gt;</b>.
<pre>
&lt;canvas id="myCanvas"&gt;
Your browser does not support the canvas tag.
&lt;/canvas&gt;
&lt;script&gt;
var canvas = document.getElementById("myCanvas");
var ctx = canvas.getContext("2d");
ctx.fillStyle = "#FF0000";
ctx.fillRect(0, 0, 80, 80);
&lt;/script&gt;
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
    <td>2.0</td>
    <td>3.1</td>
    <td>9.0</td>
  </tr>
</table>
<h1>Standard</h1>
The <b>&lt;canvas&gt;</b> tag supports the standard attributes.
<h1>Event</h1>
The <b>&lt;canvas&gt;</b> tag supports the event attributes.
<h1>Default CSS</h1>
Most browsers will display the <b>&lt;abbr&gt;</b> element with the following default values:
<pre>
canvas {
  height: 150px;
  width: 300px;
}
</pre>
