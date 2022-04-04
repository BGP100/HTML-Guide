<h1>Default Controls</h1>
When showing a standard Google map, it comes with the default control set:
<ul>
  <li>Zoom - displays a slider or "+/-" buttons to control the zoom level of the map.</li>
  <li>Pan - displays a pan control for panning the map.</li>
  <li>MapType - lets the user toggle between map types (roadmap and satellite).</li>
  <li>Street View - displays a Pegman icon which can be dragged to the map to enable Street View.</li>
</ul>
<h1>More Controls</h1>
In addition to the default controls, Google Maps also has:
<ul>
  <li>Scale - displays a map scale element</li>
  <li>Rotate - displays a small circular icon which allows you to rotate maps</li>
  <li>Overview Map - displays a thumbnail overview map reflecting the current map viewport within a wider area</li>
</ul>
You can specify which controls to show when creating the map (inside MapOptions) or by calling setOptions() to change the map's options.
<h1>Disabling Default Controls</h1>
You may instead wish to turn off the default controls.
<br>
To do so, set the Map's disableDefaultUI property (within the Map options object) to true:
<pre>var mapOptions {disableDefaultUI: true}</pre>
<h1>Turn on ALL Controls</h1>
Some controls appear on the map by default; while others will not appear unless you set them.
<br>
Adding or removing controls from the map is specified in the Map options object.
<br>
Set the control to true to make it visible - Set the control to false to hide it.
<br>
The following example turns "on" all controls:
<pre>
var mapOptions {
  panControl: true,
  zoomControl: true,
  mapTypeControl: true,
  scaleControl: true,
  streetViewControl: true,
  overviewMapControl: true,
  rotateControl: true
}
</pre>
<h1>Modifying Controls</h1>
Several of the map controls are configurable.
<br>
The controls can be modified by specifying control options fields.
<br>
For example, options for modifying a Zoom control are specified in the zoomControlOptions field. The zoomControlOptions field may contain:
<ul>
  <li>google.maps.ZoomControlStyle.SMALL - displays a mini-zoom control (only + and - buttons)</li>
  <li>google.maps.ZoomControlStyle.LARGE - displays the standard zoom slider control</li>
  <li>google.maps.ZoomControlStyle.DEFAULT - picks the best zoom control based on device and map size</li>
</ul>
<pre>
zoomControl: true,
zoomControlOptions: {
    style: google.maps.ZoomControlStyle.SMALL
}
</pre>
Note: If you modify a control, always enable the control first (set it to true).
<br>
Another configurable control is the MapType control.
<br>
Options for modifying a control are specified in the mapTypeControlOptions field. The mapTypeControlOptions field may contain::
<ul>
  <li>google.maps.MapTypeControlStyle.HORIZONTAL_BAR - display one button for each map type</li>
  <li>google.maps.MapTypeControlStyle.DROPDOWN_MENU - select map type via a dropdown menu</li>
  <li>google.maps.MapTypeControlStyle.DEFAULT - displays the "default" behavior (depends on screen size)</li>
</ul>
<pre>
mapTypeControl: true,
mapTypeControlOptions: {
  style: google.maps.MapTypeControlStyle.DROPDOWN_MENU
}
</pre>
You can also position a control, with the ControlPosition property:
<pre>
mapTypeControl: true,
mapTypeControlOptions: {
  style: google.maps.MapTypeControlStyle.DROPDOWN_MENU,
  position: google.maps.ControlPosition.TOP_CENTER
}
</pre>
