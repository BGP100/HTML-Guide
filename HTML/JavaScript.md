<a href="/HTML/Iframe.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/HTML/FilePaths.md">Next &gt;</a>
<hr>
JavaScript makes HTML pages more dynamic and interactive.
<br>
<img src="https://i.imgur.com/JA5GEIC.png">
<pre>
&lt;h1&gt;My First JavaScript&lt;/h1&gt;
&lt;button type="button"
onclick="document.getElementById('demo').innerHTML = Date()"&gt;
Click me to display Date and Time.&lt;/button&gt;
</pre>
<h1>&lt;script&gt;</h1>
The HTML <b>&lt;script&gt;</b> tag is used to define a client-side script (JavaScript).
<br>
The <b>&lt;script&gt;</b> element either contains script statements, or it points to an external script file through the src attribute.
<br>
Common uses for JavaScript are image manipulation, form validation, and dynamic changes of content.
<br>
To select an HTML element, JavaScript most often uses the document.getElementById() method.
<br>
This JavaScript example writes "Hello JavaScript!" into an HTML element with id="demo":
<pre>
&lt;script&gt;
document.getElementById("demo").innerHTML = "Hello JavaScript!";
&lt;/script&gt;
</pre>
<h1>Examples</h1>
Here are some examples of what JavaScript can do:
<b>Changing Content:</b>
<pre>document.getElementById("demo").innerHTML = "Hello JavaScript!";</pre>
<b>Changing Styles:</b>
<pre>
document.getElementById("demo").style.fontSize = "25px";
document.getElementById("demo").style.color = "red";
document.getElementById("demo").style.backgroundColor = "yellow";
</pre>
<b>Changing Attributes:</b>
<pre>document.getElementById("image").src = "picture.gif";</pre>
<h1>&lt;noscript&gt;</h1>
The HTML <b>&lt;noscript&gt;</b> tag defines an alternate content to be displayed to users that have disabled scripts in their browser or have a browser that doesn't support scripts:
<pre>
&lt;script&gt;
document.getElementById("demo").innerHTML = "Hello JavaScript!";
&lt;/script&gt;
&lt;noscript&gt;Sorry, your browser does not support JavaScript!&lt;/noscript&gt;
</pre>
