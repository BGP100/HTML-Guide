<a href="/JS/AJAX/Introduction.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/AJAX/Request.md">Next &gt;</a>
<hr>
The keystone of AJAX is the XMLHttpRequest object.
<ul>
  <li>Create an XMLHttpRequest object</li>
  <li>Define a callback function</li>
  <li>Open the XMLHttpRequest object</li>
  <li>Send a Request to a server</li>
</ul>
<h1>The XMLHttpRequest Object</h1>
All modern browsers support the XMLHttpRequest object.
<br>
The XMLHttpRequest object can be used to exchange data with a web server behind the scenes. This means that it is possible to update parts of a web page, without reloading the whole page.
<h1>Create an XMLHttpRequest Object</h1>
All modern browsers (Chrome, Firefox, IE, Edge, Safari, Opera) have a built-in XMLHttpRequest object.
<br>
Syntax for creating an XMLHttpRequest object:
<pre>variable = new XMLHttpRequest();</pre>
<h1>Define a Callback Function</h1>
A callback function is a function passed as a parameter to another function.
<br>
In this case, the callback function should contain the code to execute when the response is ready.
<pre>
xhttp.onload = function() {
  // What to do when the response is ready
}
</pre>
<h1>Send a Request</h1>
To send a request to a server, you can use the open() and send() methods of the XMLHttpRequest object:
<pre>
xhttp.open("GET", "ajax_info.txt");
xhttp.send();
</pre>
<pre>
// Create an XMLHttpRequest object
const xhttp = new XMLHttpRequest();
// Define a callback function
xhttp.onload = function() {
  // Here you can use the Data
}
// Send a request
xhttp.open("GET", "ajax_info.txt");
xhttp.send();
</pre>
<h1>Access Across Domains</h1>
For security reasons, modern browsers do not allow access across domains.
<br>
This means that both the web page and the XML file it tries to load, must be located on the same server.
<br>
The examples on W3Schools all open XML files located on the W3Schools domain.
<br>
If you want to use the example above on one of your own web pages, the XML files you load must be located on your own server.
<h1>XMLHttpRequest Object Methods</h1>
<table class="ws-table-all notranslate">
  <tr>
    <th>Method</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>new XMLHttpRequest()</td>
    <td>Creates a new XMLHttpRequest object</td>
  </tr>
  <tr>
    <td>abort()</td>
    <td>Cancels the current request</td>
  </tr>
  <tr>
    <td>getAllResponseHeaders()</td>
    <td>Returns header information</td>
  </tr>
  <tr>
    <td>getResponseHeader()</td>
    <td>Returns specific header information</td>
  </tr>
  <tr>
    <td>open(<i>method, url, async, user, psw</i>)</td>
    <td>Specifies the request<br><br><i>method</i>: the request type GET or POST<br><i>url</i>: the file location<br><i>async</i>: true (asynchronous) or false (synchronous)<br><i>user</i>: optional user name<br><i>psw</i>: optional password</td>
  </tr>
  <tr>
    <td>send()</td>
    <td>Sends the request to the server<br>Used for GET requests</td>
  </tr>
  <tr>
    <td>send(<em>string</em>)</td>
    <td>Sends the request to the server.<br>Used for POST requests</td>
  </tr>
  <tr>
    <td>setRequestHeader()</td>
    <td>Adds a label/value pair to the header to be sent</td>
  </tr>
</table>
<h1>XMLHttpRequest Object Properties</h1>
<table class="ws-table-all notranslate">
  <tr>
    <th>Property</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>onload</td>
    <td>Defines a function to be called when the request is recieved (loaded)</td>
  </tr>
  <tr>
    <td>onreadystatechange</td>
    <td>Defines a function to be called when the readyState property changes</td>
  </tr>
  <tr>
    <td>readyState</td>
    <td>Holds the status of the XMLHttpRequest.<br>0: request not initialized <br>1: server connection established<br>2: request received <br>3: processing request <br>4: request finished and response is ready</td>
  </tr>
  <tr>
    <td>responseText</td>
    <td>Returns the response data as a string</td>
  </tr>
  <tr>
    <td>responseXML</td>
    <td>Returns the response data as XML data</td>
  </tr>
  <tr>
    <td>status</td>
    <td>Returns the status-number of a request<br>200: "OK"<br>403: "Forbidden"<br>404: "Not Found"<br></td>
  </tr>
  <tr>
    <td>statusText</td>
    <td>Returns the status-text (e.g. "OK" or "Not Found")</td>
  </tr>
</table>
<h1>Multiple Callback Functions</h1>
If you have more than one AJAX task in a website, you should create one function for executing the XMLHttpRequest object, and one callback function for each AJAX task.
<br>
The function call should contain the URL and what function to call when the response is ready.
<pre>
loadDoc("url-1", myFunction1);
loadDoc("url-2", myFunction2);
function loadDoc(url, cFunction) {
  const xhttp = new XMLHttpRequest();
  xhttp.onload = function() {cFunction(this);}
  xhttp.open("GET", url);
  xhttp.send();
}
function myFunction1(xhttp) {
  // action goes here
}
function myFunction2(xhttp) {
  // action goes here
}
</pre>
