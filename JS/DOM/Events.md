<a href="/JS/DOM/Animations.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/DOM/Navigation.md">Next &gt;</a>
<hr>
HTML DOM allows JavaScript to react to HTML events.
<h1>Reacting to Events</h1>
A JavaScript can be executed when an event occurs, like when a user clicks on an HTML element.
<br>
To execute code when a user clicks on an element, add JavaScript code to an HTML event attribute:
<pre><i>onclick=JavaScript</i></pre>
Examples of HTML events:
<ul>
  <li>When a user clicks the mouse</li>
  <li>When a web page has loaded</li>
  <li>When an image has been loaded</li>
  <li>When the mouse moves over an element</li>
  <li>When an input field is changed</li>
  <li>When an HTML form is submitted</li>
  <li>When a user strokes a key</li>
</ul>
In this example, the content of the <b>&lt;h1&gt;</b> element is changed when a user clicks on it:
<pre>&lt;h1 onclick="this.innerHTML='Ooops!'"&gt;Click on this text!&lt;/h1&gt;</pre>
In this example, a function is called from the event handler:
<pre>
&lt;h1 onclick="changeText(this)"&gt;Click on this text!
&lt;script&gt;
function changeText(id) {
  id.innerHTML = "Ooops!";
}
&lt;/script&gt;
</pre>
<h1>onload &amp; onunload</h1>
The <b>onload</b> and <b>onunload</b> events are triggered when the user enters or leaves the page.
<br>
The <b>onload</b> event can be used to check the visitor's browser type and browser version, and load the proper version of the web page based on the information.
<br>
The <b>onload</b> and <b>onunload</b> events can be used to deal with cookies.
<pre>&lt;body onload="checkCookies()"&gt;</pre>
<h1>onchange</h1>
The <b>onchange</b> event is often used in combination with validation of input fields.
<br>
Below is an example of how to use the onchange. The <b>upperCase()</b> function will be called when a user changes the content of an input field.
<pre>&lt;input type="text" id="fname" onchange="upperCase()"&gt;</pre>
