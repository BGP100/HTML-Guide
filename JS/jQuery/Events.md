<a href="/JS/jQuery/Selectors.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/jQuery/HTML.md">Next &gt;</a>
<hr>
jQuery is tailor-made to respond to events in an HTML page.
<h1>What are Them?</h1>
All the different visitors' actions that a web page can respond to are called events.
<br>
An event represents the precise moment when something happens.
<br>
Examples:
<ul>
  <li>moving a mouse over an element</li>
  <li>selecting a radio button</li>
  <li>clicking on an element</li>
</ul>
The term "fires/fired" is often used with events. Example: "The keypress event is fired, the moment you press a key".
<br>
Here are some common DOM events:
<table class="ws-table-all notranslate">
  <tr>
    <th>Mouse Events</th>
    <th>Keyboard Events</th>
    <th>Form Events</th>
    <th>Document/Window Events</th>
  </tr>
  <tr>
    <td>click</td>
    <td>keypress</td>
    <td>submit</td>
    <td>load</td>
  </tr>
  <tr>
    <td>dblclick</td>
    <td>keydown</td>
    <td>change</td>
    <td>resize</td>
  </tr>
  <tr>
    <td>mouseenter</td>
    <td>keyup</td>
    <td>focus</td>
    <td>scroll</td>
  </tr>
  <tr>
    <td>mouseleave</td>
    <td>&nbsp;</td>
    <td>blur</td>
    <td>unload</td>
  </tr>
</table>
<h1>Syntax For Event Methods</h1>
In jQuery, most DOM events have an equivalent jQuery method.
<br>
To assign a click event to all paragraphs on a page, you can do this:
<pre>$("p").click();</pre>
The next step is to define what should happen when the event fires. You must pass a function to the event:
<pre>
$("p").click(function(){
  // action goes here!!
});
</pre>
<h1>Commonly Used jQuery Event Methods</h1>
<h2>$(document).ready()</h2>
The <b>$(document).ready()</b> method allows us to execute a function when the document is fully loaded.
<h2>click()</h2>
The <b>click()</b> method attaches an event handler function to an HTML element.
<br>
The function is executed when the user clicks on the HTML element.
<br>
The following example says: When a click event fires on a <p> element; hide the current <p> element:
<pre>
$("p").click(function(){
  $(this).hide();
});
</pre>
<h2>dblclick()</h2>
The <b>dblclick()</b> method attaches an event handler function to an HTML element.
<br>
The function is executed when the user double-clicks on the HTML element:
<pre>
$("p").dblclick(function(){
  $(this).hide();
});
</pre>
<h2>mouseenter()</h2>
The <b>mouseenter()</b> method attaches an event handler function to an HTML element.
<br>
The function is executed when the mouse pointer enters the HTML element:
<pre>
$("#p1").mouseenter(function(){
  alert("You entered p1!");
});
</pre>
<h2>mouseleave()</h2>
The <b>mouseleave()</b> method attaches an event handler function to an HTML element.
<br>
The function is executed when the mouse pointer leaves the HTML element:
<pre>
$("#p1").mouseleave(function(){
  alert("Bye! You now leave p1!");
});
</pre>
<h2>mousedown()</h2>
The <b>mousedown()</b> method attaches an event handler function to an HTML element.
<br>
The function is executed, when the left, middle or right mouse button is pressed down, while the mouse is over the HTML element:
<pre>
$("#p1").mousedown(function(){
  alert("Mouse down over p1!");
});
</pre>
<h2>mouseup()</h2>
The <b>mouseup()</b> method attaches an event handler function to an HTML element.
<br>
The function is executed, when the left, middle or right mouse button is released, while the mouse is over the HTML element:
<pre>
$("#p1").mouseup(function(){
  alert("Mouse up over p1!");
});
</pre>
<h2>hover()</h2>
The <b>hover()</b> method takes two functions and is a combination of the <b>mouseenter()</b> and <b>mouseleave()</b> methods.
<br>
The first function is executed when the mouse enters the HTML element, and the second function is executed when the mouse leaves the HTML element:
<pre>
$("#p1").hover(function(){
  alert("You entered p1!");
},
function(){
  alert("Bye! You now leave p1!");
});
</pre>
<h2>focus()</h2>
The <b>focus()</b> method attaches an event handler function to an HTML form field.
<br>
The function is executed when the form field gets focus:
<pre>
$("input").focus(function(){
  $(this).css("background-color", "#cccccc");
});
</pre>
<h2>blur()</h2>
The <b>blur()</b> method attaches an event handler function to an HTML form field.
<br>
The function is executed when the form field loses focus:
<pre>
$("input").blur(function(){
  $(this).css("background-color", "#ffffff");
});
</pre>
<h2>on()</h2>
The <b>on()</b> method attaches one or more event handlers for the selected elements.
<br>
Attach a click event to a <b>&lt;p&gt;</b> element:
<pre>
$("p").on("click", function(){
  $(this).hide();
});
</pre>
Attach multiple event handlers to a <b>&lt;p&gt;</b> element:
<pre>
$("p").on({
  mouseenter: function(){
    $(this).css("background-color", "lightgray");
  },
  mouseleave: function(){
    $(this).css("background-color", "lightblue");
  },
  click: function(){
    $(this).css("background-color", "yellow");
  }
});
</pre>
