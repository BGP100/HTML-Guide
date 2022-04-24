<a href="/JS/BOM/Popups.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/BOM/Cookies.md">Next &gt;</a>
<hr>
JavaScript can be executed in time-intervals.
<br>
This is called timing events.
<h1>Timing Events</h1>
The window object allows execution of code at specified time intervals.
<br>
These time intervals are called timing events.
<br>
The two key methods to use with JavaScript are:
<ul>
  <li><code>setTimeout(function, milliseconds)</code><br>Executes a function, after waiting a specified number of milliseconds.</li>
  <li><code>setInterval(function, milliseconds)</code><br>Same as <b>setTimeout()</b>, but repeats the execution of the function continuously.</li>
</ul>
<h1>setTimeout()</h1>
<b>Syntax:</b>
<pre>window.setTimeout(function, milliseconds);</pre>
The <b>window.setTimeout()</b> method can be written without the window prefix.
<br>
The first parameter is a function to be executed.
<br>
The second parameter indicates the number of milliseconds before execution.
<pre>
&lt;button onclick="setTimeout(myFunction,3000)"&gt;Try it&lt;/button&gt;
&lt;script&gt;
function myFunction() {
  alert('Hello');
}
&lt;/script&gt;
</pre>
<h1>How to Stop the Execution?</h1>
The <b>clearTimeout()</b> method stops the execution of the function specified in setTimeout().
<pre>window.clearTimeout(timeoutVariable)</pre>
The <b>window.clearTimeout()</b> method can be written without the window prefix.
<br>
The <b>clearTimeout()</b> method uses the variable returned from <b>setTimeout()</b>:
<pre>
myVar = setTimeout(function, milliseconds);
clearTimeout(myVar);
</pre>
If the function has not already been executed, you can stop the execution by calling the <b>clearTimeout()</b> method:
<pre>
&lt;button onclick="myVar=setTimeout(myFunction,3000)"&gt;Try it&lt;/button&gt;
&lt;button onclick="clearTimeout(myVar)"&gt;Stop it&lt;/button&gt;
&lt;p id="demo"&gt;&lt;/p&gt;
&lt;script&gt;
let myVar = setInterval(myTimer, 1000);
function myTimer() {
  const d = new Date();
  document.getElementById("demo").innerHTML = d.toLocaleTimeString();
}
&lt;/script&gt;
</pre>
<h1>setInterval()</h1>
The <b>setInterval()</b> method repeats a given function at every given time-interval.
<pre>window.setInterval(function, milliseconds);</pre>
The <b>window.setInterval()</b> method can be written without the window prefix.
<br>
The first parameter is the function to be executed.
<br>
The second parameter indicates the length of the time-interval between each execution.
<br>
This example executes a function called "myTimer" once every second (like a digital watch).
<pre>
setInterval(myTimer, 1000);
function myTimer() {
  const d = new Date();
  document.getElementById("demo").innerHTML = d.toLocaleTimeString();
}
</pre>
<b>Did you know?</b>
<br>
There are 1000 milliseconds in one second.
