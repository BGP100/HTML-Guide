<a href="/JS/BOM/Screen.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/BOM/History.md">Next &gt;</a>
<hr>
The <b>window.location</b> object can be used to get the current page address (URL) and to redirect the browser to a new page.
<hr>
The window.location object can be written without the window prefix.
<br>
Some examples:
<ul>
  <li><a href="#href">window.location.href</a> - returns the href (URL) of the current page</li>
  <li><a href="#hostname">window.location.hostname</a> - returns the domain name of the web host</li>
  <li><a href="#pathname">window.location.pathname</a> - returns the path and filename of the current page</li>
  <li><a href="#protocol">window.location.protocol</a> - returns the web protocol used (http: or https:)</li>
  <li><a href="#port">window.location.port</a> - returns the number of the internet host port (of the current page)</li>
  <li><a href="#assign">window.location.assign()</a> - loads a new document</li>
</ul>
<h1>href</h1>
The <b>window.location.href</b> property returns the URL of the current page.
<pre>document.getElementById("demo").innerHTML = "Page location is " + window.location.href;</pre>
Result:
<pre>Page location is https://github.com/BGP100/HTML-Guide/blob/main/JS/BOM/Location.md</pre>
<h1>hostname</h1>
The <b>window.location.hostname</b> property returns the name of the internet host (of the current page).
<pre>document.getElementById("demo").innerHTML = "Page hostname is " + window.location.hostname</pre>
Result:
<pre>Page hostname is www.github.com</pre>
<h1>pathname</h1>
The <b>window.location.pathname</b> property returns the pathname of the current page.
<pre>document.getElementById("demo").innerHTML = "Page pathname is " + window.location.pathname</pre>
Result:
<pre>Page pathname is /BGP100/HTML-Guide/blob/main/JS/BOM/Location.md</pre>
<h1>protocol</h1>
The <b>window.location.protocol</b> property returns the web protocol of the page.
<pre>document.getElementById("demo").innerHTML = "Page protocol is " + window.location.protocol</pre>
Result:
<br>
<pre>Page protocol is https:</pre>
<h1>port</h1>
The <b>window.location.port</b> property returns the number of the internet host port (of the current page).
<pre>document.getElementById("demo").innerHTML = "Page port is " + window.location.assign()</pre>
Result:
<pre>Page port is&nbsp;</pre>
<h1>assign()</h1>
The <b>window.location.assign()</b> method loads a new document.
<pre>
&lt;input type="button" value="Load new document" onclick="newDoc()"&gt;
&lt;script&gt;
function newDoc() {
  window.location.assign("//bledy-guides.repl.co")
}
&lt;/script&gt;
</pre>
