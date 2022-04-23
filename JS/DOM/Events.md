<a href="/JS/DOM/Animations.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/DOM/Navigation.md">Next &gt;</a>
<hr>
HTML DOM allows JavaScript to react to HTML events.
<h1>Events</h1>
<h2>Reacting to Events</h2>
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
<h2>onload &amp; onunload</h2>
The <b>onload</b> and <b>onunload</b> events are triggered when the user enters or leaves the page.
<br>
The <b>onload</b> event can be used to check the visitor's browser type and browser version, and load the proper version of the web page based on the information.
<br>
The <b>onload</b> and <b>onunload</b> events can be used to deal with cookies.
<pre>&lt;body onload="checkCookies()"&gt;</pre>
<h2>onchange</h2>
The <b>onchange</b> event is often used in combination with validation of input fields.
<br>
Below is an example of how to use the onchange. The <b>upperCase()</b> function will be called when a user changes the content of an input field.
<pre>&lt;input type="text" id="fname" onchange="upperCase()"&gt;</pre>
<h1>Events Listener</h1>
<h2>addEventListener()</h2>
The <b>addEventListener()</b> method attaches an event handler to the specified element.
<br>
The <b>addEventListener()</b> method attaches an event handler to an element without overwriting existing event handlers.
<br>
You can add many event handlers to one element.
<br>
You can add many event handlers of the same type to one element, i.e two "click" events.
<br>
You can add event listeners to any DOM object not only HTML elements. i.e the window object.
<br>
The <b>addEventListener()</b> method makes it easier to control how the event reacts to bubbling.
<br>
When using the <b>addEventListener()</b> method, the JavaScript is separated from the HTML markup, for better readability and allows you to add event listeners even when you do not control the HTML markup.
<br>
You can easily remove an event listener by using the <b>removeEventListener()</b> method.
<pre>document.getElementById("myBtn").addEventListener("click", displayDate);</pre>
<h2>removeEventListener()</h2>
The <b>removeEventListener()</b> method removes event handlers that have been attached with the addEventListener() method:
<pre>element.removeEventListener("mousemove", myFunction);</pre>
<h2>Syntax</h2>
<pre>element.addEventListener(event, function, useCapture);</pre>
The first parameter is the type of the event (like <code>"click"</code> or <code>"mousedown"</code> or any other HTML DOM Event.)
<br>
The second parameter is the function we want to call when the event occurs.
<br>
The third parameter is a boolean value specifying whether to use event bubbling or event capturing. This parameter is optional.
<h2>Add an Event Handler to an Element</h2>
<pre>element.addEventListener("click", function() { alert("Hello World!");});</pre>
You can also refer to an external "named" function:
<pre>
element.addEventListener("click", myFunction);
function myFunction() {
  alert ("Hello World!");
}
</pre>
<h2>Add Many Event Handlers to the Same Element</h2>
The <b>addEventListener()</b> method allows you to add many events to the same element, without overwriting existing events:
<pre>
element.addEventListener("click", myFunction);
element.addEventListener("click", mySecondFunction);
</pre>
You can add events of different types to the same element:
<pre>
element.addEventListener("mouseover", myFunction);
element.addEventListener("click", mySecondFunction);
element.addEventListener("mouseout", myThirdFunction);
</pre>
<h2>Event Bubbling or Event Capturing?</h2>
There are two ways of event propagation in the HTML DOM, bubbling and capturing.
<br>
Event propagation is a way of defining the element order when an event occurs. If you have a <b>&lt;p&gt;</b> element inside a <b>&lt;div&gt;</b> element, and the user clicks on the <b>&lt;p&gt;</b> element, which element's "click" event should be handled first?
<br>
In bubbling the inner most element's event is handled first and then the outer: the <b>&lt;p&gt;</b> element's click event is handled first, then the <b>&lt;div&gt;</b> element's click event.
<br>
In capturing the outer most element's event is handled first and then the inner: the <b>&lt;div&gt;</b> element's click event will be handled first, then the <b>&lt;p&gt;</b> element's click event.
<br>
With the <b>addEventListener()</b> method you can specify the propagation type by using the "useCapture" parameter:
<pre>addEventListener(event, function, useCapture);</pre>
The default value is false, which will use the bubbling propagation, when the value is set to true, the event uses the capturing propagation.
<pre>
document.getElementById("myP").addEventListener("click", myFunction, true);
document.getElementById("myDiv").addEventListener("click", myFunction, true);
</pre>
