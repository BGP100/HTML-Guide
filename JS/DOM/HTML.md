<a href="/JS/DOM/Methods.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/DOM/Elements.md">Next &gt;</a>
<hr>
The HTML DOM allows JavaScript to change the content of HTML elements.
<h1>Changing HTML Content</h1>
The easiest way to modify the content of an HTML element is by using the <b>innerHTML</b> property.
<br>
To change the content of an HTML element, use this syntax:
<pre>document.getElementById(<i>id</i>).innerHTML = <i>new HTML</i></pre>
This example changes the content of a <b>&lt;p&gt;</b> element:
<pre>
&lt;p id="p1"&gt;Hello World!&lt;/p&gt;
&lt;script&gt;document.getElementById("p1").innerHTML = "New text!";&lt;/script&gt;
</pre>
<b>Explained:</b>
<ul>
  <li>The HTML document above contains a &lt;p&gt; element with <code>id="p1"</code></li>
  <li>We use the HTML DOM to get the element with <code>id="p1"</code></li>
  <li>A JavaScript changes the content (<b>innerHTML</b>) of that element to <code>"New text!"</code></li>
  <li>This example changes the content of an <b>&lt;h1&gt;</b> element:</li>
</ul>
<pre>
&lt;h1 id="id01"&gt;Old Heading&lt;/h1&gt;
&lt;script&gt;
const element = document.getElementById("id01");
element.innerHTML = "New Heading";
&lt;/script&gt;
</pre>
<b>Explained:</b>
<ul>
  <li>The HTML document above contains an <b>&lt;h1&gt;</b> element with <code>id="id01"</code></li>
  <li>We use the HTML DOM to get the element with <code>id="id01"</code></li>
  <li>A JavaScript changes the content (<b>innerHTML</b>) of that element to "New Heading"</li>
</ul>
<h1>Changing HTML Attributes</h1>
To change the value of an HTML attribute, use this syntax:
<pre>document.getElementById(<i>id</i>).attribute = <i>new value</i></pre>
This example changes the value of the src attribute of an <b>&lt;img&gt;</b> element:
<pre>
&lt;img id="myImage" src="/imgs/smiley.jpg"&gt;
&lt;script&gt;document.getElementById("myImage").src = "/imgs/landscape.png";&lt;/script&gt;
</pre>
<b>Explained:</b>
<ul>
  <li>The HTML document above contains an <b>&lt;img&gt;</b> element with <code>id="myImage"</code></li>
  <li>We use the HTML DOM to get the element with <code>id="myImage"</code></li>
  <li>A JavaScript changes the <b>src</b> attribute of that element from "/imgs/smiley.jpg" to "/imgs/landscape.png"</li>
</ul>
<h1>Dynamic HTML Content</h1>
JavaScript can create dynamic HTML content:
<pre>document.getElementById("demo").innerHTML = "Date: " + Date();</pre>
<h1>document.write()</h1>
In JavaScript, <b>document.write()</b> can be used to write directly to the HTML output stream:
<pre>
&lt;p&gt;Bla bla bla&lt;/p&gt;
&lt;script&gt;document.write(Date());&lt;/script&gt;
&lt;p&gt;Bla bla bla&lt;/p&gt;
