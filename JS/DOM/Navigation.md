<a href="/JS/DOM/Events.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/DOM/Nodes.md">Next &gt;</a>
<hr>
With the HTML DOM, you can navigate the node tree using node relationships.
<h1>Nodes</h1>
According to the W3C HTML DOM standard, everything in an HTML document is a node:
<ul>
  <li>The entire document is a document node</li>
  <li>Every HTML element is an element node</li>
  <li>The text inside HTML elements are text nodes</li>
  <li>Every HTML attribute is an attribute node (deprecated)</li>
  <li>All comments are comment nodes</li>
</ul>
<img src="https://i.imgur.com/2bFZh33.png">
<br>
With the HTML DOM, all nodes in the node tree can be accessed by JavaScript.
<br>
New nodes can be created, and all nodes can be modified or deleted.
<h1>Node Relationships</h1>
The nodes in the node tree have a hierarchical relationship to each other.
<br>
The terms parent, child, and sibling are used to describe the relationships.
<ul>
  <li>In a node tree, the top node is called the root (or root node)</li>
  <li>Every node has exactly one parent, except the root (which has no parent)</li>
  <li>A node can have a number of children</li>
  <li>Siblings (brothers or sisters) are nodes with the same parent</li>
</ul>
<img src="https://i.imgur.com/7ruhn7b.png">
<pre>
&lt;html&gt;
  &lt;head&gt;
    &lt;title&gt;DOM Tutorial&lt;/title&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;DOM Lesson one&lt;/h1&gt;
    &lt;p&gt;Hello world!&lt;/p&gt;
  &lt;/body&gt;
&lt;/html&gt;
</pre>
From the HTML above you can read:
<ul>
  <li><code>&lt;html&gt;</code> is the root node.</li>
  <li><code>&lt;html&gt;</code> has no parents.</li>
  <li><code>&lt;html&gt;</code> is the parent of <code>&lt;head&gt;</code> and <code>&lt;body&gt;</code>.</li>
  <li><code>&lt;head&gt;</code> is the first child of <code>&lt;html&gt;</code>.</li>
  <li><code>&lt;body&gt;</code> is the last child of <code>&lt;html&gt;</code>.</li>
</ul>
and:
<ul>
  <li><code>&lt;head&gt;</code> has one child: <code>&lt;title&gt;</code>.</li>
  <li><code>&lt;title&gt;</code> has one child (a text node): "DOM Tutorial".</li>
  <li><code>&lt;body&gt;</code> has two children: <code>&lt;h1&gt;</code> and <code>&lt;p&gt;</code>.</li>
  <li><code>&lt;h1&gt;</code> has one child: "DOM Lesson one".</li>
  <li><code>&lt;p&gt;</code> has one child: "Hello world!".</li>
  <li><code>&lt;h1&gt;</code> and <code>&lt;p&gt;</code> are siblings.</li>
</ul>
<h1>Navigating Between Nodes</h1>
You can use the following node properties to navigate between nodes with JavaScript:
<ul>
  <li><b>parentNode</b></li>
  <li><b>childNodes[<i>nodenumber</i>]</b></li>
  <li><b>firstChild</b></li>
  <li><b>lastChild</b></li>
  <li><b>nextSibling</b></li>
  <li><b>previousSibling</b></li>
</ul>
<h1>Child Nodes and Node Values</h1>
Example:
<pre>&lt;title id="demo"&gt;DOM Tutorial&lt;/title&gt;</pre>
The element node <b>&lt;title&gt;</b> (in the example above) does not contain text.
<br>
It contains a text node with the value "DOM Tutorial".
<br>
The value of the text node can be accessed by the node's <b>innerHTML</b> property:
<pre>myTitle = document.getElementById("demo").innerHTML;</pre>
Accessing the innerHTML property is the same as accessing the <b>nodeValue</b> of the first child:
<pre>myTitle = document.getElementById("demo").firstChild.nodeValue;</pre>
Accessing the first child can also be done like this:
<pre>myTitle = document.getElementById("demo").childNodes[0].nodeValue;</pre>
All the (3) following examples retrieves the text of an <b>&lt;h1&gt;</b> element and copies it into a <b>&lt;p&gt;</b> element:
<pre>
&lt;h1 id="id01"&gt;My First Page&lt;/h1&gt;
&lt;p id="id02"&gt;&lt;/p&gt;
&lt;script&gt;document.getElementById("id02").innerHTML = document.getElementById("id01").innerHTML;&lt;/script&gt;
</pre>
<pre>
&lt;h1 id="id01"&gt;My First Page&lt;/h1&gt;
&lt;p id="id02"&gt;&lt;/p&gt;
&lt;script&gt;document.getElementById("id01").innerHTML = document.getElementById("id02").firstChild.nodeValue;&lt;/script&gt;
</pre>
<pre>
&lt;h1 id="id01"&gt;My First Page&lt;/h1&gt;
&lt;p id="id02"&gt;&lt;/p&gt;
&lt;script&gt;document.getElementById("id02").innerHTML = document.getElementById("id01").firstNodes[0].nodeValue;&lt;/script&gt;
</pre>
<h1>innerHTML</h1>
In this tutorial we use the innerHTML property to retrieve the content of an HTML element.
<br>
However, learning the other methods above is useful for understanding the tree structure and the navigation of the DOM.
<h1>Root Nodes</h1>
There are two special properties that allow access to the full document:
<ul>
  <li><b>document.body</b> - The body of the document</li>
  <li><b>document.documentElement</b> - The full document</li>
</ul>
<pre>
&lt;h2&gt;JavaScript HTMLDOM&lt;/h2&gt;
&lt;p&gt;Displaying &lt;b&gt;document.body&lt;/b&gt;&lt;/p&gt;
&lt;p id="demo"&gt;&lt;/p&gt;
&lt;script&gt;document.getElementById("demo").innerHTML = document.body.innerHTML;&lt;/script&gt;
</pre>
<pre>
&lt;h2&gt;JavaScript HTMLDOM&lt;/h2&gt;
&lt;p&gt;Displaying &lt;b&gt;document.body&lt;/b&gt;&lt;/p&gt;
&lt;p id="demo"&gt;&lt;/p&gt;
&lt;script&gt;document.getElementById("demo").innerHTML = document.documentElement.innerHTML;&lt;/script&gt;
</pre>
<h1>nodeName</h1>
The <b>nodeName</b> property specifies the name of a node.
<ul>
  <li><b>nodeName</b> is read-only</li>
  <li><b>nodeName</b> of an element node is the same as the tag name</li>
  <li><b>nodeName</b> of an attribute node is the attribute name</li>
  <li><b>nodeName</b> of a text node is always <b>#text</b></li>
  <li><b>nodeName</b> of the document node is always <b>#document</b></li>
</ul>
<pre>
&lt;h2&gt;JavaScript HTMLDOM&lt;/h2&gt;
&lt;p&gt;Displaying &lt;b&gt;document.body&lt;/b&gt;&lt;/p&gt;
&lt;p id="demo"&gt;&lt;/p&gt;
&lt;script&gt;document.getElementById("id02").innerHTML = document.getElementById("id01").nodeName;&lt;/script&gt;
</pre>
<h1>nodeValue</h1>
The <b>nodeValue</b> property specifies the value of a node.
<ul>
  <li><b>nodeValue</b> for element nodes is null</li>
  <li><b>nodeValue</b> for text nodes is the text itself</li>
  <li><b>nodeValue</b> for attribute nodes is the attribute value</li>
</ul>
<h1>nodeType</h1>
The <b>nodeType</b> property is read only. It returns the type of a node.
<pre>
&lt;h2&gt;JavaScript HTMLDOM&lt;/h2&gt;
&lt;p&gt;Displaying &lt;b&gt;document.body&lt;/b&gt;&lt;/p&gt;
&lt;p id="demo"&gt;&lt;/p&gt;
&lt;script&gt;document.getElementById("id02").innerHTML = document.getElementById("id01").nodeType;&lt;/script&gt;
</pre>
The most important nodeType properties are:
<table class="ws-table-all notranslate">
  <tr>
    <th>Node</th>
    <th>Type</th>
    <th>Example</th>
  </tr>
  <tr>
    <td>ELEMENT_NODE</td>
    <td>1</td>
    <td>&lt;h1 class=&quot;heading&quot;&gt;BledyGuides&lt;/h1&gt;</td>
  </tr>
  <tr>
    <td>ATTRIBUTE_NODE</td>
    <td>2</td>
    <td>&nbsp;class = &quot;heading&quot; (deprecated)</td>
  </tr>
  <tr>
    <td>TEXT_NODE</td>
    <td>3</td>
    <td>BledyGuides</td>
  </tr>
  <tr>
    <td>COMMENT_NODE</td>
    <td>8</td>
    <td>&lt;!-- This is a comment --&gt;</td>
  </tr>
  <tr>
    <td>DOCUMENT_NODE</td>
    <td>9</td>
    <td>The HTML document itself (the parent of &lt;html&gt;)</td>
  </tr>
  <tr>
    <td>DOCUMENT_TYPE_NODE</td>
    <td>10</td>
    <td>&lt;!DOCTYPE html&gt;</td>
  </tr>
</table>
