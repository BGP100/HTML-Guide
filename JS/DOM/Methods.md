HTML DOM methods are actions you can perform (on HTML Elements).
<br>
HTML DOM properties are values (of HTML Elements) that you can set or change.
<h1>The Programming Interface</h1>
The HTML DOM can be accessed with JavaScript (and with other programming languages).
<br>
In the DOM, all HTML elements are defined as objects.
<br>
The programming interface is the properties and methods of each object.
<br>
A property is a value that you can get or set (like changing the content of an HTML element).
<br>
A method is an action you can do (like add or deleting an HTML element).
<h1>Example</h1>
The following example changes the content (the <b>innerHTML</b>) of the <b>&lt;p&gt;</b> element with <code>id="demo"</code>:
<pre>
&lt;p id="demo"&gt;&lt;/p&gt;
&lt;script&gt;document.getElementById("demo").innerHTML = "Hello World!";&lt;/script&gt;
</pre>
In the example above, <b>getElementById</b> is a method, while <b>innerHTML</b> is a property.
<h1>getElementById</h1>
The most common way to access an HTML element is to use the <b>id</b> of the element.
<br>
In the example above the <b>getElementById</b> method used <code>id="demo"</code> to find the element.
<h1>innerHTML</h1>
The easiest way to get the content of an element is by using the <b>innerHTML</b> property.
<br>
The <b>innerHTML</b> property is useful for getting or replacing the content of HTML elements.
