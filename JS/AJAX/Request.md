<a href="/JS/AJAX/Status.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/AJAX/Response.md">Next &gt;</a>
<hr>
The XMLHttpRequest object is used to request data from a server.
<h1>Send a Request To a Server</h1>
To send a request to a server, we use the open() and send() methods of the XMLHttpRequest object:
<pre>
xhttp.open("GET", "ajax_info.txt", true);
xhttp.send();
</pre>
<table class="ws-table-all notranslate"> 
  <tr>
    <th>Method</th>
    <th>Description</th>
  </tr>  
  <tr>
    <td>open(<i>method, url, async</i>)</td>
    <td>Specifies the type of request.<br>---------------<br><i>method</i>: the type of request: GET or POST<br><i>url</i>: the server (file) location<br><i>async</i>: true (asynchronous) or false (synchronous)</td>
  </tr>
  <tr>
    <td>send()</td>
    <td>Sends the request to the server (used for GET)</td>
  </tr>
  <tr>
    <td>send(<i>string</i>)</td>
    <td>Sends the request to the server (used for POST)</td>
  </tr>
</table>
<h1>A File On a Server</h1>
The url parameter of the open() method, is an address to a file on a server:
<pre>xhttp.open("GET", "ajax_test.asp", true);</pre>
The file can be any kind of file, like .txt , .htm , and .xml, or server scripting files like .asp and .php (which can perform actions on the server before sending the response back).
<h1>True or False?</h1>
Server requests should be sent asynchronously.

The async parameter of the open() method should be set to true:
<pre>xhttp.open("GET", "ajax_test.asp", true);</pre>
By sending asynchronously, the JavaScript does not have to wait for the server response, but can instead:
<ul>
  <li>execute other scripts while waiting for server response</li>
  <li>deal with the response after the response is ready</li>
</ul>
<b>WARNING!!!</b>
<br>
The default value for the async parameter is async = true.
<br>
You can safely remove the third parameter from your code.
<br>
Synchronous XMLHttpRequest (async = false) is not recommended because the JavaScript will stop executing until the server response is ready. If the server is busy or slow, the application will hang or stop.
<h1>GET or POST?</h1>
GET is simpler and faster than POST, and can be used in most cases.
<br>
However, always use POST requests when:
<ul>
  <li>A cached file is not an option (update a file or database on the server).</li>
  <li>Sending a large amount of data to the server (POST has no size limitations).</li>
  <li>Sending user input (which can contain unknown characters), POST is more robust and secure than GET.</li>
</ul>
<h2>GET</h2>
A simple <b>GET</b> request:
<pre>
xhttp.open("GET", "demo_get.asp");
xhttp.send();
</pre>
In the example above, you may get a cached result. To avoid this, add a unique ID to the URL:
<pre>
xhttp.open("GET", "demo_get.asp?t=" + Math.random());
xhttp.send();
</pre>
If you want to send information with the GET method, add the information to the URL:
<pre>
xhttp.open("GET", "demo_get2.asp?fname=Henry&lname=Ford");
xhttp.send();
</pre>
How the server uses the input and how the server responds to a request, is explained in a later chapter.
<h2>POST</h2>
A simple POST request:
<pre>
xhttp.open("POST", "demo_post.asp");
xhttp.send();
</pre>
To POST data like an HTML form, add an HTTP header with setRequestHeader(). Specify the data you want to send in the send() method:
<pre>
xhttp.open("POST", "ajax_test.asp");
xhttp.setRequestHeader("Content-type", "application/x-www-form-urlencoded");
xhttp.send("fname=Henry&lname=Ford");
</pre>
<table class="ws-table-all notranslate"> 
  <tr>
    <th>Method</th>
    <th>Description</th>
  </tr>  
  <tr>
    <td>setRequestHeader(<i>header, value</i>)</td>
    <td>Adds HTTP headers to the request<br>---------------<br><i>header</i>: specifies the header name<br><i>value</i>: specifies the header value</td>
  </tr>
</table>
<h1>Synchronous</h1>
To execute a synchronous request, change the third parameter in the open() method to false:
<pre>xhttp.open("GET", "ajax_info.txt", false);</pre>
Sometimes async = false are used for quick testing. You will also find synchronous requests in older JavaScript code.
<br>
Since the code will wait for server completion, there is no need for an onreadystatechange function:
<pre>
xhttp.open("GET", "ajax_info.txt", false);
xhttp.send();
document.getElementById("demo").innerHTML = xhttp.responseText;
</pre>
<b>WARNING!!!</b>
<br>
Synchronous XMLHttpRequest (async = false) is not recommended because the JavaScript will stop executing until the server response is ready. If the server is busy or slow, the application will hang or stop.
<br>
Modern developer tools are encouraged to warn about using synchronous requests and may throw an InvalidAccessError exception when it occurs.
