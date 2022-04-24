<a href="/JS/BOM/Window.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/BOM/Location.md">Next &gt;</a>
<hr>
The <b>window.history</b> object contains the browsers history.
<hr>
The window.history object can be written without the window prefix.
<br>
To protect the privacy of the users, there are limitations to how JavaScript can access this object.
<br>
Some methods:
<ul>
  <li><a href="#Back">history.back()</a> - same as clicking back in the browser</li>
  <li><a href="#Forward">history.forward()</a> - same as clicking forward in the browser</li>
</ul>
<h1>Back</h1>
The <b>history.back()</b> method loads the previous URL in the history list.
<br>
This is the same as clicking the Back button in the browser.
<pre>
&lt;input type="button" value="Back" onclick="goBack()"&gt;
&lt;script&gt;
function goBack() {
  window.history.back()
}
&lt;/script&gt;
</pre>
<h1>Forward</h1>
The history.forward() method loads the next URL in the history list.
<br>
This is the same as clicking the Forward button in the browser.
<pre>
&lt;input type="button" value="Back" onclick="goForward()"&gt;
&lt;script&gt;
function goForward() {
  window.history.forward()
}
&lt;/script&gt;
</pre>
