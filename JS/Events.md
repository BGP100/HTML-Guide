<a href="/JS/Data-Types.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Strings/Main.md">Next &gt;</a>
<hr>
HTML events are "things" that happen to HTML elements.
<br>
When JavaScript is used in HTML pages, JavaScript can "react" on these events.
<br>
An HTML event can be something the browser does, or something a user does.
<br>
Here are some examples of HTML events:
<ul>
  <li>An HTML web page has finished loading</li>
  <li>An HTML input field was changed</li>
  <li>An HTML button was clicked</li>
</ul>
Often, when events happen, you may want to do something.
<br>
JavaScript lets you execute code when events are detected.
<br>
HTML allows event handler attributes, with JavaScript code, to be added to HTML elements.
<br>
With single quotes:
<pre>&lt;element event='some JavaScript'&gt;</pre>
With double quotes:
<pre>&lt;element event="some JavaScript"&gt;</pre>
In the following example, an onclick attribute (with code), is added to a button element:
<pre>&lt;button onclick="document.getElementById('demo').innerHTML = Date()"&gt;The time is?&lt;/button&gt;</pre>
In the example above, the JavaScript code changes the content of the element with id="demo".
<br>
In the next example, the code changes the content of its own element (using this.innerHTML):
<pre>&lt;button onclick="this.innerHTML = Date()"&gt;The time is?&lt;/button&gt;</pre>
JavaScript code is often several lines long. It is more common to see event attributes calling functions:
<pre>&lt;button onclick="displayDate()"&gt;The time is?&lt;/button&gt;</pre>
<h1>Common Events</h1>
Here is a list of some common HTML events:
<table class="ws-table-all">
  <tr>
    <th>Event</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>onchange</td>
    <td>An HTML element has been changed</td>
  </tr>
  <tr>
    <td>onclick</td>
    <td>The user clicks an HTML element</td>
  </tr>
  <tr>
    <td>onmouseover</td>
    <td>The user moves the mouse over an HTML element</td>
  </tr>
  <tr>
    <td>onmouseout</td>
    <td>The user moves the mouse away from an HTML element</td>
  </tr>
  <tr>
    <td>onkeydown</td>
    <td>The user pushes a keyboard key</td>
  </tr>
  <tr>
    <td>onload</td>
    <td>The browser has finished loading the page</td>
  </tr>
</table>
<h1>Handlers</h1>
Event handlers can be used to handle and verify user input, user actions, and browser actions:
<ul>
  <li>Things that should be done every time a page loads</li>
  <li>Things that should be done when the page is closed</li>
  <li>Action that should be performed when a user clicks a button</li>
  <li>Content that should be verified when a user inputs data</li>
  <li>And more ...</li>
</ul>
Many different methods can be used to let JavaScript work with events:
<ul>
  <li>HTML event attributes can execute JavaScript code directly</li>
  <li>HTML event attributes can call JavaScript functions</li>
  <li>You can assign your own event handler functions to HTML elements</li>
  <li>You can prevent events from being sent or being handled</li>
  <li>And more ...</li>
</ul>
