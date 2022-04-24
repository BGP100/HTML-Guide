<a href="/JS/DOM/Collections.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="https://bledy-guides.repl.co">Next &gt;</a>
<hr>
<h1>The HTML DOM NodeList Object</h1>
A NodeList object is a list (collection) of nodes extracted from a document.
<br>
A NodeList object is almost the same as an HTMLCollection object.
<br>
Some (older) browsers return a NodeList object instead of an HTMLCollection for methods like getElementsByClassName().
<br>
All browsers return a NodeList object for the property childNodes. 
<br>
Most browsers return a NodeList object for the method querySelectorAll().
<br>
The following code selects all <b>&lt;p&gt;</b> nodes in a document:
<pre>const myNodeList = document.querySelectorAll("p");</pre>
<pre>myNodeList[1]</pre>
<b>Note:</b> The index starts at 0.
<h2>Length</h2>
The length property defines the number of nodes in a node list:
<pre>myNodelist.length</pre>
The length property is useful when you want to loop through the nodes in a node list:
<pre>
const myNodelist = document.querySelectorAll("p");
for (let i = 0; i &lt; myNodelist.length; i++) {
  myNodelist[i].style.color = "red";
}
</pre>
<h2>Differences Between HTMLCollection and NodeList</h2>
A <b>NodeList</b> and an <b>HTMLcollection</b> is very much the same thing.
<br>
Both are array-like collections (lists) of nodes (elements) extracted from a document. The nodes can be accessed by index numbers. The index starts at 0.
<br>
Both have a <b>length</b> property that returns the number of elements in the list (collection).
<br>
An HTMLCollection is a collection of <b>document elements</b>.
<br>
A NodeList is a collection of <b>document elements</b> (element nodes, attribute nodes, and text nodes).
<br>
HTMLCollection items can be accessed by their name, id, or index number.
<br>
NodeList items can only be accessed by their index number.
<br>
An HTMLCollection is always a <b>live</b> collection. Example: If you add a <b>&lt;li&gt;</b> element to a list in the DOM, the list in the HTMLCollection will also change.
<br>
A NodeList is most often a <b>static</b> collection. Example: If you add a <b>&lt;li&gt;</b> element to a list in the DOM, the list in NodeList will not change.
<br>
The <b>getElementsByClassName()</b> and <b>getElementsByTagName()</b> methods return a live HTMLCollection.
<br>
The <b>querySelectorAll()</b> method returns a static NodeList.
<br>
The <b>childNodes</b> property returns a live NodeList.
<h1>Not an Array!</h1>
A NodeList may look like an array, but it is not.
<br>
You can loop through a NodeList and refer to its nodes by index.
<br>
But, you cannot use Array methods like push(), pop(), or join() on a NodeList.
