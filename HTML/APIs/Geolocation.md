The HTML Geolocation API is used to locate a user's position.
<hr>
The HTML Geolocation API is used to get the geographical position of a user.
<br>
Since this can compromise privacy, the position is not available unless the user approves it.
<h1>Browser Support</h1>
The numbers in the table specify the first browser version that fully supports Geolocation.
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
    <td>5.0 - 49.0 (http)<br>50.0 (https)</td>
    <td>9.0</td>
    <td>3.5</td>
    <td>5.0</td>
    <td>16.0</td>
  </tr>
</table>
<h1>Using Geolocation</h1>
The <b>getCurrentPosition()</b> method is used to return the user's position.
<br>
The example below returns the latitude and longitude of the user's position:
<pre>
&lt;script&gt;
var x = document.getElementById("demo");
function getLocation() {
  if (navigator.geolocation) {
    navigator.geolocation.getCurrentPosition(showPosition);
  } else {
    x.innerHTML = "Geolocation is not supported by this browser.";
  }
}
function showPosition(position) {
  x.innerHTML = "Latitude: " + position.coords.latitude + 
  "&lt;br&gt;Longitude: " + position.coords.longitude; 
}
&lt;/script&gt;
</pre>
Example above explained:
<ul>
  <li>Check if Geolocation is supported
  <li>If supported, run the getCurrentPosition() method. If not, display a message to the user.</li>
  <li>If the getCurrentPosition() method is successful, it returns a coordinates object to the function specified in the parameter (showPosition).</li>
  <li>The showPosition() function outputs the Latitude and Longitude.</li>
</ul>
The example above is a very basic Geolocation script, with no error handling.
<h1>Handling Errors and Rejections</h1>
The second parameter of the <b>getCurrentPosition()</b> method is used to handle errors. It specifies a function to run if it fails to get the user's location:
<pre>
function showError(error) {
  switch(error.code) {
    case error.PERMISSION_DENIED:
      x.innerHTML = "User denied the request for Geolocation."
      break;
    case error.POSITION_UNAVAILABLE:
      x.innerHTML = "Location information is unavailable."
      break;
    case error.TIMEOUT:
      x.innerHTML = "The request to get user location timed out."
      break;
    case error.UNKNOWN_ERROR:
      x.innerHTML = "An unknown error occurred."
      break;
  }
}
</pre>
<h1>Location-Specific Information</h1>
This page has demonstrated how to show a user's position on a map.
<br>
Geolocation is also very useful for location-specific information, like:
<ul>
  <li>Up-to-date local information.</li>
  <li>Showing Points-of-interest near the user.</li>
  <li>Turn-by-turn navigation (GPS).</li>
</ul>
<h1>The getCurrentPosition() Method (Return Data)</h1>
The <b>getCurrentPosition()</b> method returns an object on success. The latitude, longitude and accuracy properties are always returned. The other properties are returned if available:
<table class="ws-table-all notranslate">
  <tr>
    <th>Property</th>
    <th>Returns</th>
  </tr>
  <tr>
    <td>coords.latitude</td>
    <td>The latitude as a decimal number (always returned)</td>
  </tr>
  <tr>
    <td>coords.longitude</td>
    <td>The longitude as a decimal number (always returned)</td>
  </tr>
  <tr>
    <td>coords.accuracy</td>
    <td>The accuracy of position (always returned)</td>
  </tr>
  <tr>
    <td>coords.altitude</td>
    <td>The altitude in meters above the mean sea level (returned if available)</td>
  </tr>
  <tr>
    <td>coords.altitudeAccuracy</td>
    <td>The altitude accuracy of position (returned if available)</td>
  </tr>
  <tr>
    <td>coords.heading</td>
    <td>The heading as degrees clockwise from North (returned if available)</td>
  </tr>
  <tr>
    <td>coords.speed</td>
    <td>The speed in meters per second (returned if available)</td>
  </tr>
  <tr>
    <td>timestamp</td>
    <td>The date/time of the response (returned if available)</td>
  </tr>
</table>
<h1>Geolocation Object</h1>
The Geolocation object also has other interesting methods:
<ul>
  <li><b>watchPosition()</b> - Returns the current position of the user and continues to return updated position as the user moves (like the GPS in a car).</li>
  <li><b>clearWatch()</b> - Stops the <b>watchPosition()</b> method.</li>
</ul>
The example below shows the watchPosition() method. You need an accurate GPS device to test this (like smartphone):
<pre>
var x = document.getElementById("demo");
function getLocation() {
  if (navigator.geolocation) {
    navigator.geolocation.watchPosition(showPosition);
  } else {
    x.innerHTML = "Geolocation is not supported by this browser.";
  }
}
function showPosition(position) {
  x.innerHTML = "Latitude: " + position.coords.latitude + 
  "&lt;br&gt;Longitude: " + position.coords.longitude; 
}
</pre>
