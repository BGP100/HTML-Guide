<a href="/JS/DOM/Nodes.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/DOM/Node-Lists.md">Next &gt;</a>
<hr>
<h1>The HTMLCollection Object</h1>
The <b>getElementsByTagName()</b> method returns an HTMLCollection object.
<br>
An HTMLCollection object is an array-like list (collection) of HTML elements.
<br>
The following code selects all <b>&lt;p&gt;</b> elements in a document:
<pre>const myCollection = document.getElementsByTagName("p");</pre>
<pre>myCollection[1]</pre>
<b>Note:</b> The index starts at 0.
<h2>Length</h2>
The length property defines the number of elements in an HTMLCollection:
<pre>myCollection.length</pre>
The length property is useful when you want to loop through the elements in a collection:
<pre>
const myCollection = document.getElementsByTagName("p");
for (let i = 0; i &lt; myCollection.length; i++) {
  myCollection[i].style.color = "red";
}
</pre>
<h3>Note !!!</h3>
An HTMLCollection is NOT an array!
<br>
An HTMLCollection may look like an array, but it is not.
<br>
You can loop through the list and refer to the elements with a number (just like an array).
<br>
However, you cannot use array methods like valueOf(), pop(), push(), or join() on an HTMLCollection.
