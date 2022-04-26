The <b>&lt;map&gt;</b> tag is used to define an image map. An image map is an image with clickable areas.
<br>
The required name attribute of the <b>&lt;map&gt;</b> element is associated with the <a href="img.md">&lt;img&gt;</a>'s usemap attribute and creates a relationship between the image and the map.
<br>
The <b>&lt;map&gt;</b> element contains a number of <a href="area.md">&gt;area&gt;</a> elements, that defines the clickable areas in the image map.
<pre>
&lt;img src="workplace.jpg" alt="Workplace" usemap="#workmap" width="400" height="379"&gt;
&lt;map name="workmap"&gt;
  &lt;area shape="rect" coords="34,44,270,350" alt="Computer" href="computer.htm"&gt;
  &lt;area shape="rect" coords="290,172,333,250" alt="Phone" href="phone.htm"&gt;
  &lt;area shape="circle" coords="337,300,44" alt="Cup of coffee" href="coffee.htm"&gt;
&lt;/map&gt;
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
    <td>Compatibility</td>
    <td>Yes</td>
    <td>Yes</td>
    <td>Yes</td>
    <td>Yes</td>
    <td>Yes</td>
  </tr>
</table>
<h1>Standard</h1>
The <b>&lt;map&gt;</b> tag supports the standard attributes.
<h1>Event</h1>
The <b>&lt;map&gt;</b> tag supports the event attributes.
<h1>Default CSS</h1>
Most browsers will display the <b>&lt;map&gt;</b> element with the following default values:
<pre>
map {
  display: inline;
}
</pre>
