<a href="/JS/AJAX/Request.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/AJAX/XML-Files.md">Next &gt;</a>
<hr>
<h1>Properties</h1>
<table class="ws-table-all notranslate"> 
  <tr>
    <th>Property</th>
    <th>Description</th>
  </tr>  
  <tr>
    <td><a href="#responseText">responseText</a></td>
    <td>get the response data as a string</td>
  </tr>
  <tr>
    <td><a href="#responseXML">responseXML</a></td>
    <td>get the response data as XML data</td>
  </tr>
</table>
<h2>responseText</h2>
The <b>responseText</b> property returns the server response as a JavaScript string, and you can use it accordingly:
<pre>document.getElementById("demo").innerHTML = xhttp.responseText;</pre>
<h2>responseXML</h2>
The XMLHttpRequest object has an in-built XML parser.
<br>
The responseXML property returns the server response as an XML DOM object.
<br>
Using this property you can parse the response as an XML DOM object:
<pre>
const xmlDoc = xhttp.responseXML;
const x = xmlDoc.getElementsByTagName("ARTIST");
let txt = "";
for (let i = 0; i &lt; x.length; i++) {
  txt += x[i].childNodes[0].nodeValue + "&lt;br&gt;";
}
document.getElementById("demo").innerHTML = txt;
xhttp.open("GET", "cd_catalog.xml");
xhttp.send();
</pre>
<h1>Methods</h1>
<table class="ws-table-all notranslate"> 
  <tr>
    <th>Method</th>
    <th>Description</th>
  </tr>  
  <tr>
    <td><a href="#getResponseHeader">getResponseHeader()</a></td>
    <td>Returns specific header information from the server resource</td>
  </tr>
  <tr>
    <td><a href="#getAllResponseHeaders">getAllResponseHeaders()</a></td>
    <td>Returns all the header information from the server resource</td>
  </tr>
</table>
<h2>getResponseHeader()</h2>
The <b>getResponseHeader()</b> method returns specific header information from the server response.
<pre>
const xhttp = new XMLHttpRequest();
xhttp.onload = function() {
    document.getElementById("demo").innerHTML = this.getResponseHeader("Last-Modified");
}
xhttp.open("GET", "ajax_info.txt");
xhttp.send();
</pre>
<h2>getAllResponseHeaders()</h2>
The <b>getAllResponseHeaders()</b> method returns all header information from the server response.
<pre>
const xhttp = new XMLHttpRequest();
xhttp.onload = function() {
    document.getElementById("demo").innerHTML = this.getAllResponseHeaders();
}
xhttp.open("GET", "ajax_info.txt");
xhttp.send();
</pre>
