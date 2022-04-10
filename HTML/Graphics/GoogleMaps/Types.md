<a href="/HTML/Graphics/GoogleMaps/Controls.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/HTML/Graphics/Game/Main.md">Next &gt;</a>
<hr>
The following map types are supported in Google Maps API:
<ul>
  <li>ROADMAP (normal, default 2D map)</li>
  <li>SATELLITE (photographic map)</li>
  <li>HYBRID (photographic map + roads and city names)</li>
  <li>TERRAIN (map with mountains, rivers, etc.)</li>
</ul>
The map type is specified either within the Map properties object, with the mapTypeId property:
<pre>
var mapOptions = {
  center:new google.maps.LatLng(51.508742,-0.120850),
  zoom:7,
  mapTypeId: google.maps.MapTypeId.HYBRID
};
</pre>
Or by calling the map's setMapTypeId() method:
<pre>map.setMapTypeId(google.maps.MapTypeId.HYBRID);</pre>
<h1>45-Degree View</h1>
The map types SATELLITE and HYBRID support a 45-degree perspective imagery view for certain locations (only at high zoom levels).
<br>
If you zoom into a location with 45-degree imagery view, the map will automatically alter the perspective view. In addition, the map will add:
<ul>
  <li>A compass wheel around the Pan control, allowing you to rotate the image.</li>
  <li>A Rotate control between the Pan and Zoom controls, allowing you to rotate the image at a 90-degree view.</li>
  <li>A toggle control for displaying the 45-degree view, under the Satellite control/label.</li>
</ul>
<b>Note:</b> Zooming out from a map with 45-degree imagery will revert each of these changes, and the original map is displayed.
<br>
The following example shows a 45-degree perspective view of Palazzo Ducale in Venice, Italy:
<pre>
var mapOptions = {
  center:myCenter,
  zoom:18,
  mapTypeId:google.maps.MapTypeId.HYBRID
};
</pre>
<h1>Disable 45-Degree View</h1>
You can disable 45-degree perspective view by calling setTilt(0) on the Map object:
<pre>map.setTilt(0);</pre>
