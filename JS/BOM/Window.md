<a href="/JS/BOM/Main.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/BOM/Screen.md">Next &gt;</a>
<hr>
The Browser Object Model (BOM) allows JavaScript to "talk to" the browser.
<hr>
There are no official standards for the Browser Object Model (BOM).
<br>
Since modern browsers have implemented (almost) the same methods and properties for JavaScript interactivity, it is often referred to, as methods and properties of the BOM.
<h1>The Window Object</h1>
The <b>window</b> object is supported by all browsers. It represents the browser's window.
<br>
All global JavaScript objects, functions, and variables automatically become members of the window object.
<br>
Global variables are properties of the window object.
<br>
Global functions are methods of the window object.
<br>
Even the document object (of the HTML DOM) is a property of the window object:
<pre>window.document.getElementById("header");</pre>
is the same as:
<pre>document.getElementById("header");</pre>
<h1>Window Size</h1>
Two properties can be used to determine the size of the browser window.
<br>
Both properties return the sizes in pixels:
<ul>
  <li><b>window.innerHeight</b> - the inner height of the browser window (in pixels)</li>
  <li><b>window.innerWidth</b> - the inner width of the browser window (in pixels)</li>
</ul>
<b>Note:</b> The browser window (the browser viewport) is NOT including toolbars and scrollbars.
<pre>
let w = window.innerWidth;
let h = window.innerHeight;
</pre>
<h1>Other Window Methods</h1>
Some other methods:
<ul>
  <li><b>window.open()</b> - open a new window</li>
  <li><b>window.close()</b> - close the current window</li>
  <li><b>window.moveTo()</b> - move the current window</li>
  <li><b>window.resizeTo()</b> - resize the current window</li>
</ul>
