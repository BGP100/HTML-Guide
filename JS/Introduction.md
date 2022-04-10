<a href="/JS/Home.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Where-To.md">Next &gt;</a>
<hr>
This chapter contains some examples of what JavaScript can do.
<h1>It can Change HTML Content</h1>
One of many JavaScript HTML methods is <b>getElementById()</b>.
<br>
The example below "finds" an HTML element (with id="demo"), and changes the element content (innerHTML) to "Hello JavaScript":
<pre>document.getElementById("demo").innerHTML = "Hello JavaScript";</pre>
JavaScript accepts both double and single quotes:
<pre>document.getElementById('demo').innerHTML = 'Hello JavaScript';</pre>
<h1>JavaScript Can Change HTML Attribute Values</h1>
In this example JavaScript changes the value of the <b>src</b> (source) attribute of an <b>&lt;img&gt;</b> tag:
<pre>
&lt;button onclick="document.getElementById('myImage').src='//i.imgur.com/EkDalgn.gif'"&gt;Turn the lights on&lt;/button&gt;
&lt;img id="myImage" src="//i.imgur.com/aovt6mx.gif" style="width:100px"&gt;
&lt;button onclick="document.getElementById('myImage').src='//i.imgur.com/aovt6mx.gif'"&gt;Turn the lights off&lt;/button&gt;
</pre>
<h1>It can Change HTML Styles</h1>
Changing the style of an HTML element, is a variant of changing an HTML attribute:
<pre>document.getElementById("demo").style.fontSize="35px";</pre>
<h1>It can Hide HTML Elements</h1>
Hiding HTML elements can be done by changing the <b>display</b> style:
<pre>document.getElementById("demo").style.display="none";</pre>
<h1>It can Show HTML Elements</h1>
Showing hidden HTML elements can also be done by changing the <b>display</b> style:
<pre>document.getElementById("demo").style.display="block";</pre>
<h1>Did You Know?</h1>
JavaScript and Java are completely different languages, both in concept and design.
<br>
JavaScript was invented by Brendan Eich in 1995, and became an ECMA standard in 1997.
<br>
ECMA-262 is the official name of the standard. ECMAScript is the official name of JavaScript.
