<a href="/HTML/Graphics/GoogleMaps/Overlays.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/HTML/Graphics/GoogleMaps/Controls.md">Next &gt;</a>
<hr>
<h1>Click to Zoom</h1>
We still use the map from the previous page: a map centered on London, England.
<br>
Now we want to zoom when a user is clicking on the marker (We attach an event handler to a marker that zooms the map when clicked).
<br>
Here is the added code:
<pre>
// Zoom to 9 when clicking on marker
google.maps.event.addListener(marker,'click',function() {
  map.setZoom(9);
  map.setCenter(marker.getPosition());
});
</pre>
I register for event notifications using the addListener() event handler. That method takes an object, an event to listen for, and a function to call when the specified event occurs.
<h1>Pan Back to Marker</h1>
Here, we save the zoom changes and pan the map back after 3 seconds
<pre>
google.maps.event.addListener(marker,'click',function() {
  var pos = map.getZoom();
  map.setZoom(9);
  map.setCenter(marker.getPosition());
  window.setTimeout(function() {map.setZoom(pos);},3000);
});
</pre>
<h1>Open an InfoWindow When Clicking on The Marker</h1>
Click on the marker to show an infowindow with some text:
<pre>
var infowindow = new google.maps.InfoWindow({
  content:"Hello World!"
});
google.maps.event.addListener(marker, 'click', function() {
  infowindow.open(map,marker);
});
</pre>
<a href="Overlays.md#InfoWindow">Click Here</a> for more 'InfoWindow' information
<h1>Set Markers and Open InfoWindow for Each Marker</h1>
Run a function when the user clicks on the map.
<br>
The placeMarker() function places a marker where the user has clicked, and shows an infowindow with the latitudes and longitudes of the marker:
<pre>
google.maps.event.addListener(map, 'click', function(event) {
  placeMarker(map, event.latLng);
});
function placeMarker(map, location) {
  var marker = new google.maps.Marker({
    position: location,
    map: map
  });
  var infowindow = new google.maps.InfoWindow({
    content: 'Latitude: ' + location.lat() +
    '<br>Longitude: ' + location.lng()
  });
  infowindow.open(map,marker);
}
</pre>
