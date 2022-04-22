<a href="/JS/DOM/Document.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/DOM/HTML.md">Next &gt;</a>
<hr>
This page teaches you how to find and access HTML elements in an HTML page.
<h1>Finding HTML Elements</h1>
Often, with JavaScript, you want to manipulate HTML elements.
<br>
To do so, you have to find the elements first. There are several ways to do this:
<ul>
  <li><a href="#ID">Finding HTML elements by id</a></li>
  <li><a href="#Tag-Name">Finding HTML elements by tag name</a></li>
  <li><a href="#Class">Finding HTML elements by class name</a></li>
  <li><a href="#CSS-Selector">Finding HTML elements by CSS selectors</a></li>
  <li><a href="#Object-Collection">Finding HTML elements by HTML object collections</a></li>
</ul>
<h2>ID</h2>
The easiest way to find an HTML element in the DOM, is by using the element id.
<br>
This example finds the element with <code>id="demo":</code>
<pre>const element = document.getElementById("demo");</pre>
If the element is found, the method will return the element as an object (in element).
<br>
If the element is not found, element will contain <b>null</b>.
<h2>Tag Name</h2>
This example finds all <b>&lt;p&gt;</b> elements:
<pre>const element = document.getElementsByTagName("p");</pre>
<h2>Class</h2>
If you want to find all HTML elements with the same class name, use <b>getElementsByClassName()</b>.
<br>
This example returns a list of all elements with <code>class="exampl"</code>.
<pre>const x = document.getElementsByClassName("exampl");</pre>
<h2>CSS Selector</h2>
If you want to find all HTML elements that match a specified CSS selector (id, class names, types, attributes, values of attributes, etc), use the <b>querySelectorAll()</b> method.
<br>
This example returns a list of all <b>&lt;p&gt;</b> elements with <code>class="exampl"</code>.
<pre>const x = document.querySelectorAll("p.exampl");</pre>
You can also do it with <b>id</b>'s:
<pre>const x = document.querySelectorAll("p#demo");</pre>
<h2>Object Collection</h2>
This example finds the form element with id="frm1", in the forms collection, and displays all element values:
<pre>
const x = document.forms["frm1"];
let text = "";
for (let i = 0; i &lt; x.length; i++) {
  text += x.elements[i].value + "&lt;br&gt;";
}
document.getElementById("demo").innerHTML = text;
</pre>
The following HTML objects (and object collections) are also accessible:
<ul>
  <li>document.anchors</li>
  <li>document.body</li>
  <li>document.documentElement</li>
  <li>document.embeds</li>
  <li>document.forms</li>
  <li>document.head</li>
  <li>document.images</li>
  <li>document.links</li>
  <li>document.scripts</li>
  <li>document.title</li>
</ul>
