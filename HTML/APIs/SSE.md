<a href="/HTML/APIs/WebWorkers.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/HTML/Timer.md">Next &gt;</a>
<hr>
Server-Sent Events (SSE) allow a web page to get updates from a server.
<hr>
A server-sent event is when a web page automatically gets updates from a server.
<br>
This was also possible before, but the web page would have to ask if any updates were available. With server-sent events, the updates come automatically.
<br>
Examples: Facebook/Twitter updates, stock price updates, news feeds, sport results, etc.
<h1>Browser Support</h1>
The numbers in the table specify the first browser version that fully support server-sent events.
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
    <td>6.0</td>
    <td>79.0</td>
    <td>6.0</td>
    <td>5.0</td>
    <td>11.5</td>
  </tr>
</table>
<h1>Recieve SSE Notifications</h1>
The EventSource object is used to receive server-sent event notifications:
<pre>
var source = new EventSource("demo_sse.php");
source.onmessage = function(event) {
  document.getElementById("result").innerHTML += event.data + "<br>";
};
</pre>
Example above explained:
<ul>
  <li>Create a new EventSource object, and specify the URL of the page sending the updates (in this example "demo_sse.php")</li>
  <li>Each time an update is received, the onmessage event occurs</li>
  <li>When an onmessage event occurs, put the received data into the element with id="result"</li>
</ul>
<h1>Check the SSE Support</h1>
In the tryit example above there were some extra lines of code to check browser support for server-sent events:
<pre>
if(typeof(EventSource) !== "undefined") {
  // Yes! Server-sent events support!
  // Some code.....
} else {
  // Sorry! No server-sent events support..
}
</pre>
<h1>Server-Side Code Example</h1>
For the example above to work, you need a server capable of sending data updates (like PHP or ASP).
<br>
The server-side event stream syntax is simple. Set the "Content-Type" header to "text/event-stream". Now you can start sending event streams.
<br>
Code in PHP (demo_sse.php):
<pre>&lt;?php header('Content-Type: text/event-stream');header('Cache-Control: no-cache');$time = date('r');echo "data: The server time is: {$time}\n\n";flush();?&gt;</pre>
Code in ASP (VB) (demo_sse.asp):
<pre>&lt;% Response.ContentType = "text/event-stream" Response.Expires = -1 Response.Write("data: The server time is: " & now()) Response.Flush() %&gt;</pre>
Code explained:
<ul>
  <li>Set the "Content-Type" header to "text/event-stream".</li>
  <li>Specify that the page should not cache.</li>
  <li>Output the data to send (Always start with "data: ").</li>
  <li>Flush the output data back to the web page.</li>
</ul>
<h1>EventSource Object</h1>
In the examples above we used the onmessage event to get messages. But other events are also available:
<table class="ws-table-all notranslate">
  <tr>
    <th>Events</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>onopen</td>
    <td>When a connection to the server is opened.</td>
  </tr>
  <tr>
    <td>onmessage</td>
    <td>When a message is received.</td>
  </tr>
  <tr>
    <td>onerror</td>
    <td>When an error occurs.</td>
  </tr>
</table>
