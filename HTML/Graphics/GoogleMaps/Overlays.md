<a href="/HTML/Graphics/GoogleMaps/Basic.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/HTML/Graphics/GoogleMaps/Events.md">Next &gt;</a>
<hr>
Overlays are objects on the map that are bound to latitude/longitude coordinates.
<br>
Google Maps has several types of overlays:
<ul>
  <li>Marker - Single locations on a map. Markers can also display custom icon images.</li>
  <li>Polyline - Series of straight lines on a map.</li>
  <li>Polygon - Series of straight lines on a map, and the shape is "closed".</li>
  <li>Circle and Rectangle.</li>
  <li>Info Windows - Displays content within a popup balloon on top of a map.</li>
  <li>Custom overlays.</li>
</ul>
<h1>Add a Marker</h1>
The Marker constructor creates a marker. Note that the position property must be set for the marker to display.
<br>
Add the marker to the map by using the setMap() method:
<pre>
var marker = new google.maps.Marker({position: myCenter});
marker.setMap(map);
</pre>
<h1>Animate the Marker</h1>
The example below shows how to animate the marker with the animation property:
<pre>
var marker = new google.maps.Marker({
  position:myCenter,
  animation:google.maps.Animation.BOUNCE
});
marker.setMap(map);
</pre>
<h1>Icon Instead of Marker</h1>
The example below specifies an image (icon) to use instead of the default marker:
<pre>
var marker = new google.maps.Marker({
  position:myCenter,
  icon:'pinkball.png'
});
marker.setMap(map);
</pre>
<h1>Polyline</h1>
A Polyline is a line that is drawn through a series of coordinates in an ordered sequence.
<br>
A polyline supports the following properties:
<ul>
  <li>path - specifies several latitude/longitude coordinates for the line</li>
  <li>strokeColor - specifies a hexadecimal color for the line (format: "#FFFFFF")</li>
  <li>strokeOpacity - specifies the opacity of the line (a value between 0.0 and 1.0)</li>
  <li>strokeWeight - specifies the weight of the line's stroke in pixels</li>
  <li>editable - defines whether the line is editable by users (true/false)</li>
</ul>
<pre>
var myTrip = [stavanger,amsterdam,london];
var flightPath = new google.maps.Polyline({
  path:myTrip,
  strokeColor:"#0000FF",
  strokeOpacity:0.8,
  strokeWeight:2
});
</pre>
<h1>Polygon</h1>
A Polygon is similar to a Polyline in that it consists of a series of coordinates in an ordered sequence. However, polygons are designed to define regions within a closed loop.
<br>
Polygons are made of straight lines, and the shape is "closed" (all the lines connect up).
<br>
A polygon supports the following properties:
<ul>
  <li>path - specifies several LatLng coordinates for the line (first and last coordinate are equal)</li>
  <li>strokeColor - specifies a hexadecimal color for the line (format: "#FFFFFF")</li>
  <li>strokeOpacity - specifies the opacity of <br>the line (a value between 0.0 and 1.0)</li>
  <li>strokeWeight - specifies the weight of the line's stroke in pixels</li>
  <li>fillColor - specifies a hexadecimal color for the area within the enclosed region (format: "#FFFFFF")</li>
  <li>fillOpacity - specifies the opacity of the fill color (a value between 0.0 and 1.0)</li>
  <li>editable - defines whether the line is editable by users (true/false)</li>
</ul>
<pre>
var myTrip = [stavanger,amsterdam,london,stavanger];
var flightPath = new google.maps.Polygon({
  path:myTrip,
  strokeColor:"#0000FF",
  strokeOpacity:0.8,
  strokeWeight:2,
  fillColor:"#0000FF",
  fillOpacity:0.4
});
</pre>
<h1>Circles</h1>
A circle supports the following properties:
<ul>
  <li>center - specifies the google.maps.LatLng of the center of the circle</li>
  <li>radius - specifies the radius of the circle, in meters</li>
  <li>strokeColor - specifies a hexadecimal color for the line around the circle (format: "#FFFFFF")</li>
  <li>strokeOpacity - specifies the opacity of the stroke color (a value between 0.0 and 1.0)</li>
  <li>strokeWeight - specifies the weight of the line's stroke in pixels</li>
  <li>fillColor - specifies a hexadecimal color for the area within the circle (format: "#FFFFFF")</li>
  <li>fillOpacity - specifies the opacity of the fill color (a value between 0.0 and 1.0)</li>
  <li>editable - defines whether the circle is editable by users (true/false)</li>
</ul>
<pre>
var myCity = new google.maps.Circle({
  center:amsterdam,
  radius:20000,
  strokeColor:"#0000FF",
  strokeOpacity:0.8,
  strokeWeight:2,
  fillColor:"#0000FF",
  fillOpacity:0.4
});
</pre>
<h1>InfoWindow</h1>
Show an InfoWindow with some text content for a marker:
<pre>
var infowindow = new google.maps.InfoWindow({
  content:"Hello World!"
});
infowindow.open(map,marker);
</pre>
