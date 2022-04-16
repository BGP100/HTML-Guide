<a href="/JS/Modules.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/BeginnerGuide.md">Next &gt;</a>
<hr>
<h1>Code Debugging</h1>
Programming code might contain syntax errors, or logical errors.
<br>
Many of these errors are difficult to diagnose.
<br>
Often, when programming code contains errors, nothing will happen. There are no error messages, and you will get no indications where to search for errors.
<br>
Searching for (and fixing) errors in programming code is called code debugging.
<h1>Debuggers</h1>
Debugging is not easy. But fortunately, all modern browsers have a built-in JavaScript debugger.
<br>
Built-in debuggers can be turned on and off, forcing errors to be reported to the user.
<br>
With a debugger, you can also set breakpoints (places where code execution can be stopped), and examine variables while the code is executing.
<br>
Normally, otherwise follow the steps at the bottom of this page, you activate debugging in your browser with the F12 key, and select "Console" in the debugger menu.
<h1>console.log()</h1>
If your browser supports debugging, you can use console.log() to display JavaScript values in the debugger window:
<pre>
&lt;h1&gt;My First Web Page&lt;/h1&gt;
&lt;script&gt;
a = 5;
b = 6;
c = a + b;
console.log(c);
&lt;/script&gt;
</pre>
<h1>Breakpoints</h1>
In the debugger window, you can set breakpoints in the JavaScript code.
<br>
At each breakpoint, JavaScript will stop executing, and let you examine JavaScript values.
<br>
After examining values, you can resume the execution of code (typically with a play button).
<h1>debugger</h1>
The <b>debugger</b> keyword stops the execution of JavaScript, and calls (if available) the debugging function.
<br>
This has the same function as setting a breakpoint in the debugger.
<br>
If no debugging is available, the debugger statement has no effect.
<br>
With the debugger turned on, this code will stop executing before it executes the third line.
<pre>
let x = 15 * 5;
debugger;
document.getElementById("demo").innerHTML = x;
</pre>
<h1>Major Browsers' Debugging Tools</h1>
Normally, you activate debugging in your browser with F12, and select "Console" in the debugger menu.
<br>
Otherwise follow these steps:
<h2>Chrome</h2>
<ul>
  <li>Open the browser.
  <li>From the menu, select "More tools".
  <li>From tools, choose "Developer tools".
  <li>Finally, select Console.
</ul>
<h2>Firefox</h2>
<ul>
  <li>Open the browser.
  <li>From the menu, select "Web Developer".
  <li>Finally, select "Web Console".
</ul>
<h2>Edge</h2>
<ul>
  <li>Open the browser.
  <li>From the menu, select "Developer Tools".
  <li>Finally, select "Console".
</ul>
<h2>Opera</h2>
<ul>
  <li>Open the browser.
  <li>From the menu, select "Developer".
  <li>From "Developer", select "Developer tools".
  <li>Finally, select "Console".
</ul>
<h2>Safari</h2>
<ul>
  <li>Go to Safari, Preferences, Advanced in the main menu.
  <li>Check "Enable Show Develop menu in menu bar".
  <li>When the new option "Develop" appears in the menu:
  <li>Choose "Show Error Console".
</ul>
<h1>Did You Know?</h1>
Debugging is the process of testing, finding, and reducing bugs (errors) in computer programs.
<br>
The first known computer bug was a real bug (an insect) stuck in the electronics.
