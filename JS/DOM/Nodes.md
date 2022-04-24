<a href="/JS/DOM/Navigation.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/DOM/Collections.md">Next &gt;</a>
<hr>
Adding and Removing Nodes (HTML Elements)
<h1>Creating New HTML Elements (Nodes)</h1>
To add a new element to the HTML DOM, you must create the element (element node) first, and then append it to an existing element.
<pre>
&lt;div id="div1"&gt;
  &lt;p id="p1"&gt;This is a paragraph.&lt;/p&gt;
  &lt;p id="p2"&gt;This is another paragraph.&lt;/p&gt;
&lt;/div&gt;
&lt;script&gt;
const para = document.createElement("p");
const node = document.createTextNode("This is new.");
para.appendChild(node);
const element = document.getElementById("div1");
element.appendChild(para);
&lt;/script&gt;
</pre>
<b>Explained:</b>
<br>
This code creates a new <b>&lt;p&gt;</b> element:
<pre>const para = document.createElement("p");</pre>
To add text to the <b>&lt;p&gt;</b> element, you must create a text node first. This code creates a text node:
<pre>const node = document.createTextNode("This is a new paragraph.");</pre>
Then you must append the text node to the <b>&lt;p&gt;</b> element:
<pre>para.appendChild(node);</pre>
Finally you must append the new element to an existing element.
<br>
This code finds an existing element:
<pre>const element = document.getElementById("div1");</pre>
This code appends the new element to the existing element:
<pre>element.appendChild(para);</pre>
<h1>insertBefore()</h1>
The <b>appendChild()</b> method in the previous example, appended the new element as the last child of the parent.
<br>
If you don't want that you can use the <b>insertBefore()</b> method:
<pre>
&lt;div id="div1"&gt;
  &lt;p id="p1"&gt;This is a paragraph.&lt;/p&gt;
  &lt;p id="p2"&gt;This is another paragraph.&lt;/p&gt;
&lt;/div&gt;
&lt;script&gt;
const para = document.createElement("p");
const node = document.createTextNode("This is new.");
para.appendChild(node);
const element = document.getElementById("div1");
const child = document.getElementById("p1");
element.insertBefore(para, child);
&lt;/script&gt;
</pre>
<h1>Removing Existing HTML Elements</h1>
To remove an HTML element, use the <b>remove()</b> method:
<pre>
&lt;div id="div1"&gt;
  &lt;p id="p1"&gt;This is a paragraph.&lt;/p&gt;
  &lt;p id="p2"&gt;This is another paragraph.&lt;/p&gt;
&lt;/div&gt;
&lt;script&gt;const elmnt = document.getElementById("p1"); elmnt.remove();&lt;/script&gt;
</pre>
<b>Explained:</b>
<br>
The HTML document contains a <b>&lt;div&gt;</b> element with two child nodes (two <b>&lt;p&gt;</b> elements):
<pre>
&lt;div&gt;
  &lt;p id="p1"&gt;This is a paragraph.&lt;/p&gt;
  &lt;p id="p2"&gt;This is another paragraph.&lt;/p&gt;
&lt;/div&gt;
</pre>
Find the element you want to remove:
<pre>const elmnt = document.getElementById("p1");</pre>
Then execute the <b>remove()</b> method on that element:
<pre>elmnt.remove();</pre>
<h1>Removing a Child Node</h1>
For browsers that does not support the remove() method, you have to find the parent node to remove an element:
<pre>
&lt;div id="div1"&gt;
  &lt;p id="p1"&gt;This is a paragraph.&lt;/p&gt;
  &lt;p id="p2"&gt;This is another paragraph.&lt;/p&gt;
&lt;/div&gt;
&lt;script&gt;
const parent = document.getElementById("div1");
const child = document.getElementById("p1");
parent.removeChild(child);
&lt;/script&gt;
</pre>
<b>Explained:</b>
This HTML document contains a <b>&lt;div&gt;</b> element with two child nodes (two <b>&lt;p&gt;</b> elements):
<pre>
&lt;div id="div1"&gt;
  &lt;p id="p1"&gt;This is a paragraph.&lt;/p&gt;
  &lt;p id="p2"&gt;This is another paragraph.&lt;/p&gt;
&lt;/div&gt;
</pre>
Find the element with <code>id="div1"</code>:
<pre>const parent = document.getElementById("div1");</pre>
Find the <b>&lt;p&gt;</b> element with <code>id="p1"</code>:
<pre>const child = document.getElementById("p1");</pre>
Remove the child from the parent:
<pre>parent.removeChild(child);</pre>
Here is a common workaround: Find the child you want to remove, and use its parentNode property to find the parent:
<pre>
const child = document.getElementById("p1");
child.parentNode.removeChild(child);
</pre>
<h1>Replacing HTML Elements</h1>
To replace an element to the HTML DOM, use the <b>replaceChild()</b> method:
<pre>
&lt;div id="div1"&gt;
  &lt;p id="p1"&gt;This is a paragraph.&lt;/p&gt;
  &lt;p id="p2"&gt;This is another paragraph.&lt;/p&gt;
&lt;/div&gt;
&lt;script&gt;
const para = document.createElement("p");
const node = document.createTextNode("This is new.");
para.appendChild(node);
const parent = document.getElementById("div1");
const child = document.getElementById("p1");
parent.replaceChild(para, child);
&lt;/script&gt;
</pre>
