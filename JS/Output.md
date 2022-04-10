<a href="/JS/Where-To.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Statements.md">Next &gt;</a>
<hr>
JavaScript can "display" data in different ways:
<ul>
  <li>Writing into an HTML element, using <b>innerHTML</b></li>
  <li>Writing into the HTML output using <b>document.write()</b></li>
  <li>Writing into an alert box, using <b>window.alert()</b></li>
  <li>Writing into the browser console, using <b>console.log()</b></li>
</ul>
<h1>innerHTML</h1>
To access an HTML element, JavaScript can use the document.getElementById(id) method.
<br>
The id attribute defines the HTML element. The innerHTML property defines the HTML content:
<pre>
&lt;h1&gt;My First Web Page&lt;/h1&gt;
&lt;p&gt;My First Paragraph&lt;/p&gt;
&lt;p id="demo"&gt;&lt;/p&gt;
&lt;script&gt;document.getElementById("demo").innerHTML = 5 + 6;&lt;/script&gt;
</pre>
<h1>document.write()</h1>
For testing purposes, it is convenient to use <b>document.write()</b>:
<pre>
&lt;h1&gt;My First Web Page&lt;/h1&gt;
&lt;p&gt;My First Paragraph&lt;/p&gt;
&lt;p id="demo"&gt;&lt;/p&gt;
&lt;script&gt;document.write("5 + 6");&lt;/script&gt;
</pre>
<h1>window.alert()</h1>
You can use an alert box to display data:
<pre>
&lt;h1&gt;My First Web Page&lt;/h1&gt;
&lt;p&gt;My First Paragraph&lt;/p&gt;
&lt;p id="demo"&gt;&lt;/p&gt;
&lt;script&gt;window.alert("5 + 6");&lt;/script&gt;
</pre>
You can skip the <b>window</b> keyword.
<br>
In JavaScript, the window object is the global scope object, that means that variables, properties, and methods by default belong to the window object. This also means that specifying the <b>window</b> keyword is optional:
<pre>
&lt;h1&gt;My First Web Page&lt;/h1&gt;
&lt;p&gt;My First Paragraph&lt;/p&gt;
&lt;p id="demo"&gt;&lt;/p&gt;
&lt;script&gt;alert("5 + 6");&lt;/script&gt;
</pre>
<h1>console.log()</h1>
For debugging purposes, you can call the <b>console.log()</b> method in the browser to display data.
<pre>&lt;script&gt;console.log("5 + 6");&lt;/script&gt;</pre>
<h1>Print</h1>
JavaScript does not have any print object or print methods.
<br>
You cannot access output devices from JavaScript.
<br>
The only exception is that you can call the <b>window.print()</b> method in the browser to print the content of the current window.
<pre>&lt;button onclick="window.print()"&gt;Print this page&lt;/button&gt;</pre>
