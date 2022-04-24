<a href="/JS/jQuery/Get-Started.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/jQuery/Selectors.md">Next &gt;</a>
<hr>
With jQuery you select (query) HTML elements and perform "actions" on them.
<hr>
The jQuery syntax is tailor-made for selecting HTML elements and performing some action on the element(s).
<br>
Basic syntax is: <b>$(selector).action()</b>
<ul>
  <li>A <code>$</code> sign to define/access jQuery</li>
  <li>A (<i>selector</i>) to "query (or find)" HTML elements</li>
  <li>A jQuery <i>action</i>() to be performed on the element(s)</li>
</ul>
Examples:
<br>
<code>$(this).hide()</code> - hides the current element.
<br>
<code>$("p").hide()</code> - hides all <b>&lt;p&gt;</b> elements.
<br>
<code>$(".test").hide()</code> - hides all elements with <b>class="test"</b>.
<br>
<code>$("#test").hide()</code> - hides the element with <b>id="test"</b>.
<h1>The Document Ready Event</h1>
You might have noticed that all jQuery methods in our examples, are inside a document ready event:
<pre>
$(document).ready(function(){
  // jQuery methods go here...
});
</pre>
This is to prevent any jQuery code from running before the document is finished loading (is ready).
<br>
It is good practice to wait for the document to be fully loaded and ready before working with it. This also allows you to have your JavaScript code before the body of your document, in the head section.
<br>
Here are some examples of actions that can fail if methods are run before the document is fully loaded:
<ul>
  <li>Trying to hide an element that is not created yet</li>
  <li>Trying to get the size of an image that is not loaded yet</li>
</ul>
<b>Tip:</b> The jQuery team has also created an even shorter method for the document ready event:
<pre>
$(function(){
  // jQuery methods go here...
});
</pre>
Use the syntax you prefer. We think that the document ready event is easier to understand when reading the code.
