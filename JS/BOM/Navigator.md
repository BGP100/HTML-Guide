<a href="/JS/BOM/History.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/BOM/Popups.md">Next &gt;</a>
<hr>
The <b>window.navigator</b> object contains information about the visitor's browser.
<hr>
The window.navigator object can be written without the window prefix.
<br>
Some examples:
<ul>
  <li><a href="#appName">navigator.appName</a></li>
  <li><a href="#appCodeName">navigator.appCodeName</a></li>
  <li><a href="#platform">navigator.platform</a></li>
  <li><a href="#Is-The-Browser-Online">navigator.onLine</a></li>
  <li><a href="#Is-Java-Enabled">navigator.javaEnabled()</a></li>
  <li><a href="#product">navigator.product</a></li>
  <li><a href="#appVersion">navigator.appVersion</a></li>
  <li><a href="#userAgent">navigator.userAgent</a></li>
  <li><a href="#language">navigator.language</a></li>
</ul>
<h1>appName</h1>
The appName property returns the application name of the browser:
<pre>
&lt;p id="demo"&gt;&lt;/p&gt;
&lt;script&gt;document.getElementById("demo").innerHTML = "navigator.appName is " + navigator.appName;&lt;/script&gt;
</pre>
<h1>appCodeName</h1>
The <b>appCodeName</b> property returns the application code name of the browser:
<pre>
&lt;p id="demo"&gt;&lt;/p&gt;
&lt;script&gt;document.getElementById("demo").innerHTML = "navigator.appCodeName is " + navigator.appCodeName;&lt;/script&gt;
</pre>
<h1>platform</h1>
The <b>platform</b> property returns the browser platform (operating system):
<pre>
&lt;p id="demo"&gt;&lt;/p&gt;
&lt;script&gt;document.getElementById("demo").innerHTML = navigator.platform;&lt;/script&gt;
</pre>
<h1>Warning !!!</h1>
The information from the navigator object can often be misleading, and should not be used to detect browser versions because:
<ul>
  <li>Different browsers can use the same name</li>
  <li>The navigator data can be changed by the browser owner</li>
  <li>Some browsers misidentify themselves to bypass site tests</li>
  <li>Browsers cannot report new operating systems, released later than the browser</li>
</ul>
<h1>Is The Browser Online?</h1>
The <b>onLine</b> property returns true if the browser is online:
<pre>
&lt;p id="demo"&gt;&lt;/p&gt;
&lt;script&gt;document.getElementById("demo").innerHTML = navigator.onLine;&lt;/script&gt;
</pre>
<h1>Is Java Enabled?</h1>
The <b>javaEnabled()</b> method returns true if Java is enabled:
<pre>
&lt;p id="demo"&gt;&lt;/p&gt;
&lt;script&gt;document.getElementById("demo").innerHTML = navigator.javaEnabled();&lt;/script&gt;
</pre>
<h1>product</h1>
The <b>product</b> property returns the product name of the browser engine:
<pre>
&lt;p id="demo"&gt;&lt;/p&gt;
&lt;script&gt;document.getElementById("demo").innerHTML = "navigator.product is " + navigator.product;&lt;/script&gt;
</pre>
<h1>appVersion</h1>
The <b>appVersion</b> property returns version information about the browser:
<pre>
&lt;p id="demo"&gt;&lt;/p&gt;
&lt;script&gt;document.getElementById("demo").innerHTML = navigator.appVersion;&lt;/script&gt;
</pre>
<h1>userAgent</h1>
The <b>userAgent</b> property returns the user-agent header sent by the browser to the server:
<pre>
&lt;p id="demo"&gt;&lt;/p&gt;
&lt;script&gt;document.getElementById("demo").innerHTML = navigator.userAgent;&lt;/script&gt;
</pre>
<h1>language</h1>
The <b>language</b> property returns the browser's language:
<pre>
&lt;p id="demo"&gt;&lt;/p&gt;
&lt;script&gt;document.getElementById("demo").innerHTML = navigator.language;&lt;/script&gt;
</pre>
