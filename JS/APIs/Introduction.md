<a href="/JS/Async/AsyncAndAwait.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/APIs/Forms.md">Next &gt;</a>
<hr>
A Web API is a developer's dream.
<ul>
  <li>It can extend the functionality of the browser</li>
  <li>It can greatly simplify complex functions</li>
  <li>It can provide easy syntax to complex code</li>
</ul>
<h1>What is it?</h1>
API stands for <b>A</b>pplication <b>P</b>rogramming <b>I</b>nterface.
<br>
A Web API is an application programming interface for the Web.
<br>
A Browser API can extend the functionality of a web browser.
<br>
A Server API can extend the functionality of a web server.
<h1>Browser APIs</h1>
All browsers have a set of built-in Web APIs to support complex operations, and to help accessing data.
<br>
For example, the Geolocation API can return the coordinates of where the browser is located.
<pre>
const myElement = document.getElementById("demo");
function getLocation() {
  if (navigator.geolocation) {
    navigator.geolocation.getCurrentPosition(showPosition);
  } else {
    myElement.innerHTML = "Geolocation is not supported by this browser.";
  }
}
function showPosition(position) {
  myElement.innerHTML = "Latitude: " + position.coords.latitude + "&lt;br&gt;Longitude: " + position.coords.longitude;
}
</pre>
<h1>Third Party APIs</h1>
Third party APIs are not built into your browser.
<br>
To use these APIs, you will have to download the code from the Web.
<br>
Examples:
<ul>
  <li><b>YouTube API</b> - Allows you to display videos on a web site.</li>
  <li><b>Twitter API</b> - Allows you to display Tweets on a web site.</li>
  <li><b>Facebook API</b> - Allows you to display Facebook info on a web site.</li>
</ul>
<h1>Other APIs</h1>
I made other APIs before, check them out by <a href="/HTML/APIs">clicking here</a>!
