<a href="/JS/jQuery/Effects/Chaining.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/jQuery/Traversing/Ancestors.md">Next &gt;</a>
<hr>
<h1>Traversing Up the DOM Tree</h1>
Three useful jQuery methods for traversing up the DOM tree are:
<ul>
  <li><a href="#parent">parent()</a></li>
  <li><a href="#parents">parents()</a></li>
  <li><a href="#parentsUntil">parentsUntil()</a></li>
</ul>
<h1>parent()</h1>
The parent() method returns the direct parent element of the selected element.
<br>
This method only traverse a single level up the DOM tree.
<br>
The following example returns the direct parent element of each <b>&lt;span&gt;</b> elements:
<pre>
$(document).ready(function(){
  $("span").parent();
});
</pre>
<h1>parents()</h1>
The parents() method returns all ancestor elements of the selected element, all the way up to the document's root element (<b>&lt;html&gt;</b>).
<br>
The following example returns all ancestors of all <b>&lt;span&gt;</b> elements:
<pre>
$(document).ready(function(){
  $("span").parents();
});
</pre>
You can also use an optional parameter to filter the search for ancestors.
<br>
The following example returns all ancestors of all <b>&lt;span&gt;</b> elements that are <b>&lt;ul&gt;</b> elements:
<pre>
$(document).ready(function(){
  $("span").parents("ul");
});
</pre>
<h1>parentsUntil()</h1>
The <b>parentsUntil()</b> method returns all ancestor elements between two given arguments.
<br>
The following example returns all ancestor elements between a <b>&lt;span&gt;</b> and a <b>&lt;div&gt;</b> element:
<pre>
$(document).ready(function(){
  $("span").parentsUntil("div");
});
</pre>
