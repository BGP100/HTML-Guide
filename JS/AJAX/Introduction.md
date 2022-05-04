<a href="https://bledy-guides.repl.co/#ajax">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/AJAX/XMLHttp.md">Next &gt;</a>
<hr>
AJAX is not a programming language.
<br>
AJAX is a technique for accessing web servers from a web page.
<br>
AJAX stands for Asynchronous JavaScript And XML.
<br>
AJAX is a developer's dream, because you can:
<ul>
  <li>Read data from a web server - after the page has loaded</li>
  <li>Update a web page without reloading the page</li>
  <li>Send data to a web server - in the background</li>
</ul>
<h1>Example</h1>
The HTML page contains a &lt;div&gt; section and a &lt;button&gt;.
<br>
The &lt;div&gt; section is used to display information from a server.
<br>
The &lt;button&gt; calls a function (if it is clicked).
<br>
The function requests data from a web server and displays it:
<pre>
&lt;div id="demo"&gt;
  &lt;h2&gt;Let AJAX change this text&lt;/h2&gt;
  &lt;button type="button" onclick="loadDoc()"&gt;Change Content&lt;/button&gt;
&lt;/div&gt;
&lt;script&gt;
function loadDoc() {
  const xhttp = new XMLHttpRequest();
  xhttp.onload = function() {
    document.getElementById("demo").innerHTML = this.responseText;
    }
  xhttp.open("GET", "ajax_info.txt", true);
  xhttp.send();
}
&lt;/script&gt;
</pre>
<h1>What is it?</h1>
AJAX = Asynchronous JavaScript And XML.
<br>
AJAX is not a programming language.
<br>
AJAX just uses a combination of:
<ul>
  <li>A browser built-in XMLHttpRequest object (to request data from a web server)</li>
  <li>JavaScript and HTML DOM (to display or use the data)</li>
</ul>
<b>Note:</b> AJAX is a misleading name. AJAX applications might use XML to transport data, but it is equally common to transport data as plain text or JSON text.
<br>
AJAX allows web pages to be updated asynchronously by exchanging data with a web server behind the scenes. This means that it is possible to update parts of a web page, without reloading the whole page.
<h1>How it Works</h1>
<img src="https://i.imgur.com/T9SonZ9.gif">
<br>
1. An event occurs in a web page (the page is loaded, a button is clicked)
<br>
2. An XMLHttpRequest object is created by JavaScript
<br>
3. The XMLHttpRequest object sends a request to a web server
<br>
4. The server processes the request
<br>
5. The server sends a response back to the web page
<br>
6. The response is read by JavaScript
<br>
7. Proper action (like page update) is performed by JavaScript
<h1>Modern Browsers (Fetch API)</h1>
Modern Browsers can use Fetch API instead of the XMLHttpRequest Object.
<br>
The Fetch API interface allows web browser to make HTTP requests to web servers.
<br>
If you use the XMLHttpRequest Object, Fetch can do the same in a simpler way.
