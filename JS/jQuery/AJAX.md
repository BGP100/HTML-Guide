<a href="/JS/jQuery/Traversing/Filtering.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/jQuery/NoConflict.md">Next &gt;</a>
<hr>
AJAX is the art of exchanging data with a server, and updating parts of a web page - without reloading the whole page.
<h1>What is it?</h1>
AJAX = Asynchronous JavaScript and XML.
<br>
In short; AJAX is about loading data in the background and display it on the webpage, without reloading the whole page.
<br>
Examples of applications using AJAX: Gmail, Google Maps, Youtube, and Facebook tabs.
<br>
You can learn more about it in my <a href="/JS/AJAX/Introduction.md">AJAX tutorial</a>.
<h1>What About jQuery and AJAX?</h1>
jQuery provides several methods for AJAX functionality.
<br>
With the jQuery AJAX methods, you can request text, HTML, XML, or JSON from a remote server using both HTTP Get and HTTP Post - And you can load the external data directly into the selected HTML elements of your web page!
<br><br>
<b>Without jQuery, AJAX coding can be a bit tricky!</b>
<br>
Writing regular AJAX code can be a bit tricky, because different browsers have different syntax for AJAX implementation. This means that you will have to write extra code to test for different browsers. However, the jQuery team has taken care of this for us, so that we can write AJAX functionality with only one single line of code.
<h1>Methods</h1>
<h2>load()</h2>
The jQuery <b>load()</b> method is a simple, but powerful AJAX method.
<br>
The <b>load()</b> method loads data from a server and puts the returned data into the selected element.
<pre>$("#div1").load("demo_test.txt");</pre>
It is also possible to add a jQuery selector to the URL parameter:
<pre>$("#div1").load("demo_test.txt #p1");</pre>
The optional callback parameter specifies a callback function to run when the <b>load()</b> method is completed. The callback function can have different parameters:
<ul>
  <li><b>responseTxt</b> - contains the resulting content if the call succeeds</li>
  <li><b>statusTxt</b> - contains the status of the call</li>
  <li><b>xhr</b> - contains the XMLHttpRequest object</li>
</ul>
The following example displays an alert box after the <b>load()</b> method completes. If the load() method has succeeded, it displays "External content loaded successfully!", and if it fails it displays an error message:
<pre>
$("button").click(function(){
  $("#div1").load("demo_test.txt", function(responseTxt, statusTxt, xhr){
    if(statusTxt == "success")
      alert("External content loaded successfully!");
    if(statusTxt == "error")
      alert("Error: " + xhr.status + ": " + xhr.statusText);
  });
});
</pre>
<b>Syntax:</b>
<pre>$(<i>selector</i>).load(<i>URL</i>,<i>data</i>,<i>callback</i>);</pre>
<h2>$.get()</h2>
The <code>$.get()</code> method requests data from the server with an HTTP GET request:
<pre>
$("button").click(function(){
  $.get("demo_test.asp", function(data, status){
    alert("Data: " + data + "\nStatus: " + status);
  });
});
</pre>
The first parameter of <code>$.get()</code> is the URL we wish to request ("demo_test.asp").
<br>
<b>Tip:</b> Here is how the ASP file looks like ("demo_test.asp"):
<pre>
&lt;%
response.write("This is some text from an external ASP file.")
%&gt;
</pre>
<b>Syntax:</b>
<pre>$.get(<i>URL</i>,<i>callback</i>);</pre>
<h2>$.post()</h2>
The <code>$.post()</code> method requests data from the server using an HTTP POST request.
<pre>
$("button").click(function(){
  $.post("demo_test_post.asp",
  {
    name: "Donald Duck",
    city: "Duckburg"
  },
  function(data, status){
    alert("Data: " + data + "\nStatus: " + status);
  });
});
</pre>
The first parameter of <code>$.post()</code> is the URL we wish to request ("demo_test_post.asp").
<br>
<b>Tip:</b> Here is how the ASP file looks like ("demo_test_post.asp"):
<pre>
&lt;%
dim fname,city
fname=Request.Form("name")
city=Request.Form("city")
Response.Write("Dear " & fname & ". ")
Response.Write("Hope you live well in " & city & ".")
%&gt;
</pre>
<b>Syntax:</b>
<pre>$.load(<i>URL</i>,<i>data</i>,<i>callback</i>);</pre>
