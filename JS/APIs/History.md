<a href="/JS/APIs/Forms.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/APIs/WebStorage.md">Next &gt;</a>
<hr>
The Web History API provides easy methods to access the windows.history object.
<br>
The window.history object contains the URLs (Web Sites) visited by the user.
<h1>Browser Support</h1>
The Web History API is supported in all browsers:
<table class="ws-table-all notranslate">
  <tr>
    <th>Browser</th>
    <th>Chrome</th>
    <th>Edge</th>
    <th>Firefox</th>
    <th>Safari</th>
    <th>Opera</th>
  </tr>
  <tr>
    <td>Compatibility</td>
    <td>Yes</td>
    <td>Yes</td>
    <td>Yes</td>
    <td>Yes</td>
    <td>Yes</td>
  </tr>
</table>
<h1>back()</h1>
The <b>back()</b> method loads the previous URL in the windows.history list.
<br>
It is the same as clicking the "back arrow" in your browser.
<pre>
&lt;button onclick="myFunction()"&gt;Go Back&lt;/button&gt;
&lt;script&gt;
function myFunction() {
  window.history.back();
}
&lt;/script&gt;
</pre>
<h1>go()</h1>
The <b>go()</b> method loads a specific URL from the history list:
<pre>
&lt;button onclick="myFunction()"&gt;Go Back 2 Pages&lt;/button&gt;
&lt;script&gt;
function myFunction() {
  window.history.go(-2);
}
&lt;/script&gt;
</pre>
<h1>Properties</h1>
<table class="ws-table-all notranslate">
  <tr>
    <th>Property</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>length</td>
    <td>Returns the number of URLs in the history list</td>
  </tr>
</table>
<h1>History Object Methods</h1>
<table class="ws-table-all notranslate">
  <tr>
    <th>Method</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>back()</td>
    <td>Loads the previous URL in the history list</td>
    </tr>
  <tr>
    <td>forward()</td>
    <td>Loads the next URL in the history list</td>
    </tr>
  <tr>
    <td>go()</td>
    <td>Loads a specific URL from the history list</td>
  </tr>
</table>
