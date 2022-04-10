<a href="/JS/Introduction.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Output.md">Next &gt;</a>
<hr>
In HTML, JavaScript code is inserted between <b>&lt;script&gt;</b> and <b>&lt;/script&gt;</b> tags.
<pre>
&lt;script&gt;
document.getElementById("demo").innerHTML = "My First JavaScript";
&lt;/script&gt;
</pre>
<h1>Functions &amp; Events</h1>
A JavaScript function is a block of JavaScript code, that can be executed when "called" for.
<br>
For example, a function can be called when an event occurs, like when the user clicks a button.
<h1>JS in &lt;head&gt; or &lt;body&gt;?</h1>
You can place any number of scripts in an HTML document.
<br>
Scripts can be placed in the <b>&lt;body&gt;</b>, or in the <b>&lt;head&gt;</b> section of an HTML page, or in both.
<h2>&lt;head&gt;</h2>
In this example, a JavaScript function is placed in the <b>&lt;head&gt;</b> section of an HTML page.
<br>
The function is invoked (called) when a button is clicked:
<pre>
&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;head&gt;
&lt;script&gt;
function myFunction() {
  document.getElementById("demo").innerHTML = "Paragraph changed.";
}
&lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;h1&gt;Demo JavaScript in Head&lt;/h1&gt;
&lt;p id="demo"&gt;A Paragraph&lt;/p&gt;
&lt;button type="button" onclick="myFunction()"&gt;A Button&lt;/button&gt;
&lt;/body&gt;
&lt;/html&gt;
</pre>
<h2>&lt;body&gt;</h2>
In this example, a JavaScript function is placed in the <b>&lt;body&gt;</b> section of an HTML page.
<br>
The function is invoked (called) when a button is clicked:
<pre>
&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;body&gt;
&lt;h1&gt;Demo JavaScript in Head&lt;/h1&gt;
&lt;p id="demo"&gt;A Paragraph&lt;/p&gt;
&lt;button type="button" onclick="myFunction()"&gt;A Button&lt;/button&gt;
&lt;script&gt;
function myFunction() {
  document.getElementById("demo").innerHTML = "Paragraph changed.";
}
&lt;/script&gt;
&lt;/body&gt;
&lt;/html&gt;
</pre>
<h1>External</h1>
Scripts can also be placed in external files:
<pre>
function myFunction() {
  document.getElementById("demo").innerHTML = "Paragraph changed.";
}
</pre>
External scripts are practical when the same code is used in many different web pages.
<br>
JavaScript files have the file extension .js.
<br>
To use an external script, put the name of the script file in the src (source) attribute of a <b>&lt;script&gt;</b> tag:
<pre>&lt;script src="myScript.js"&gt;&lt;/script&gt;</pre>
You can place an external script reference in <b>&lt;body&gt;</b> or <b>&lt;head&gt;</b> as you like.
<br>
The script will behave as if it was located exactly where the <b>&lt;script&gt;</b> tag is located.
<h2>Advantages</h2>
Placing scripts in external files has some advantages:
<ul>
  <li>It separates HTML and code</li>
  <li>It makes HTML and JavaScript easier to read and maintain</li>
  <li>Cached JavaScript files can speed up page loads</li>
  <li>To add several script files to one page - use several script tags:</li>
</ul>
<pre>
&lt;script src="myScript1.js"&gt;&lt;/script&gt;
&lt;script src="myScript2.js"&gt;&lt;/script&gt;
</pre>
<h2>References</h2>
An external script can be referenced in 3 different ways:
<ul>
With a full URL (a full web address)
With a file path (like /js/)
Without any path
</ul>
This example uses a full URL to link to a JavaScript file:
<pre>&lt;script src="https://www.youtube.com/s/desktop/01530da7/jsbin/www-tampering.vflset/www-tampering.js"&gt;&lt;/script&gt;</pre>
This example uses a file path to link to myScript.js:
<pre>&lt;script src="/js/myScript.js"&gt;&lt;/script&gt;</pre>
This example uses no path to link to myScript.js:
<pre>&lt;script src="myScript.js"&gt;&lt;/script&gt;</pre>
