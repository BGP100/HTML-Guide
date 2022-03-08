This basic example creates a Google Map centered in London, England:
<pre>
&lt;h1&gt;My First Google Map&lt;/h1&gt;
&lt;div id="googleMap" style="width:100%;height:400px;">&lt;/div&gt;
&lt;script&gt;
function myMap() {
var mapProp= {
  center:new google.maps.LatLng(51.508742,-0.120850),
  zoom:5,
};
var map = new google.maps.Map(document.getElementById("googleMap"),mapProp);}
&lt;/script&gt;
&lt;script src="https://maps.googleapis.com/maps/api/js?key=YOUR_KEY&callback=myMap"&gt;&lt;/script&gt;
</pre>
<h1>The Map Container and Size</h1>
The map needs an HTML element to hold the map:
<pre>&lt;div id="googleMap" style="width:100%;height:400px"&gt;&lt;/div&gt;</pre>
<b>Tip:</b> Also set the size of the map.
<h1>Create a Function to Set The Map Properties</h1>
<pre>
function myMap() {
var mapProp = {
    center:new google.maps.LatLng(51.508742,-0.120850),
    zoom:5,
};
var map = new google.maps.Map(document.getElementById("googleMap"),mapProp);
}
</pre>
The mapProp variable defines the properties for the map.
<br>
The center property specifies where to center the map (using latitude and longitude coordinates).
<br>
The zoom property specifies the zoom level for the map (try to experiment with the zoom level).
<br>
The line: var map=new google.maps.Map(document.getElementById("googleMap"), mapProp); creates a new map inside the <b>&lt;div&gt;</b> element with id="googleMap", using the parameters that are passed (mapProp).
<h1>Multiple Maps</h1>
The example below defines four maps with different map types:
<pre>
var map1 = new google.maps.Map(document.getElementById("googleMap1"), mapOptions1);
var map2 = new google.maps.Map(document.getElementById("googleMap2"), mapOptions2);
var map3 = new google.maps.Map(document.getElementById("googleMap3"), mapOptions3);
var map4 = new google.maps.Map(document.getElementById("googleMap4"), mapOptions4);
</pre>
<h1>Free Google API Key</h1>
Google allows a website to call any Google API for free, thousands of times a day.
<a href="https://developers.google.com/maps/documentation/javascript/get-api-key">Click Here</a> to learn how to get an API key.
<pre>&lt;script src="https://maps.googleapis.com/maps/api/js?key=YOUR_KEY&callback=myMap"&gt;&lt;/script&gt;</pre>
