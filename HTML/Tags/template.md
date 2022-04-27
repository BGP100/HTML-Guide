The <b>&lt;template&gt;</b> tag is used as a container to hold some HTML content hidden from the user when the page loads.
<br>
The content inside <b>&lt;template&gt;</b> can be rendered later with a JavaScript.
<br>
You can use the <b>&lt;template&gt;</b> tag if you have some HTML code you want to use over and over again, but not until you ask for it. To do this without the <b>&lt;template&gt;</b> tag, you have to create the HTML code with JavaScript to prevent the browser from rendering the code.
<pre>
&lt;button onclick="showContent()"&gt;Show hidden content&lt;/button&gt;
&lt;template&gt;
  &lt;h2&gt;Flower&lt;/h2&gt;
  &lt;img src="img_white_flower.jpg" width="214" height="204"&gt;
&lt;/template&gt;
&lt;script&gt;
function showContent() {
  var temp = document.getElementsByTagName("template")[0];
  var clon = temp.content.cloneNode(true);
  document.body.appendChild(clon);
}
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
    <td>26.0</td>
    <td>13.0</td>
    <td>22.0</td>
    <td>8.0</td>
    <td>15.0</td>
  </tr>
</table>
<h1>Event</h1>
The <b>&lt;template&gt;</b> tag supports the event attributes.
