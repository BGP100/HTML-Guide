<a href="/JS/AJAX/Response.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/AJAX/PHP.md">Next &gt;</a>
<hr>
AJAX can be used for interactive communication with an XML file.
<h1>Example</h1>
The following example will demonstrate how a web page can fetch information from an XML file with AJAX:
<pre>Sorry, but GitHub can't display these type of stuff.</pre>
<h1>Explained:</h1>
When a user clicks on the "Get CD info" button above, the <b>loadDoc()</b> function is executed.
<br>
The <b>loadDoc()</b> function creates an <b>XMLHttpRequest</b> object, adds the function to be executed when the server response is ready, and sends the request off to the server.
<br>
When the server response is ready, an HTML table is built, nodes (elements) are extracted from the XML file, and it finally updates the element "demo" with the HTML table filled with XML data:
<pre>
function loadDoc() {
  const xhttp = new XMLHttpRequest();
  xhttp.onload = function() {myFunction(this);}
  xhttp.open("GET", "cd_catalog.xml");
  xhttp.send();
}
function myFunction(xml) {
  const xmlDoc = xml.responseXML;
  const x = xmlDoc.getElementsByTagName("CD");
  let table="&lt;tr&gt;&lt;th&gt;Artist&lt;/th&gt;&lt;th&gt;Title&lt;/th&gt;&lt;/tr&gt;";
  for (let i = 0; i &lt; x.length; i++) {
    table += "&lt;tr&gt;&lt;td&gt;" +
    x[i].getElementsByTagName("ARTIST")[0].childNodes[0].nodeValue + "&lt;/td&gt;&lt;td&gt;" + x[i].getElementsByTagName("TITLE")[0].childNodes[0].nodeValue + "&lt;/td&gt;&lt;/tr&gt;";
  }
  document.getElementById("demo").innerHTML = table;
}
&lt;/script&gt;
</pre>
<h1>The XML File</h1>
The XML file used in the example above looks like this: <a href="https://codepen.io/BGP100/pen/GRyePxw">"cd_catalog.xml"</a>.
