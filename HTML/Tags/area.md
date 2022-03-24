The <b>&lt;area&gt;</b> tag defines an area inside an image map (an image map is an image with clickable areas).
<br>
<b>&lt;area&gt;</b> elements are always nested inside a <b>&lt;map&gt;</b> tag.
<br>
<b><i>Note:</i></b> The usemap attribute in <b>&lt;img&gt;</b> is associated with the <b>&lt;map&gt;</b> element's name attribute, and creates a relationship between the image and the map.
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
The <b>&lt;address&gt;</b> tag supports the standard attributes.
<h1>Event</h1>
The <b>&lt;address&gt;</b> tag supports the event attributes.
<h1>Default CSS</h1>
Most browsers will display the <b>&lt;area&gt;</b> element with the following default values:
<pre>
area {
  display: none;
}
</pre>
