<a href="/JS/jQuery/Traversing/Descendants.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/jQuery/Traversing/Filtering.md">Next &gt;</a>
<hr>
<h1>Traversing Sideways in The DOM Tree</h1>
There are many useful jQuery methods for traversing sideways in the DOM tree:
<ul>
  <li><a href="#siblings">siblings()</a></li>
  <li><a href="#next">next()</a></li>
  <li><a href="#nextAll">nextAll()</a></li>
  <li><a href="#nextUntil">nextUntil()</a></li>
  <li><a href="#prev">prev()</a></li>
  <li><a href="#prevAll">prevAll()</a></li>
  <li><a href="#prevUntil">prevUntil()</a></li>
</ul>
<h1>siblings()</h1>
The <b>siblings()</b> method returns all sibling elements of the selected element:
<pre>
$(document).ready(function(){
  $("h2").siblings();
});
</pre>
<h1>next()</h1>
The <b>next()</b> method returns the next sibling element of the selected element:
<pre>
$(document).ready(function(){
  $("h2").next();
});
</pre>
<h1>nextAll()</h1>
The <b>nextAll()</b> method returns all next sibling elements of the selected element:
<pre>
$(document).ready(function(){
  $("h2").nextAll();
});
</pre>
<h1>nextUntil()</h1>
The <b>nextUntil()</b> method returns all next sibling elements between two given arguments:
<pre>
$(document).ready(function(){
  $("h2").nextUntil("h6");
});
</pre>
<h1>prev()</h1>
The <b>prev()</b> method works just like the methods above but with reverse functionality; it returns previous sibling elements (traverse backwards along sibling elements in the DOM tree, instead of forward):
<h1>prevAll()</h1>
The <b>prevAll()</b> method works just like the methods above but with reverse functionality; it returns previous sibling elements (traverse backwards along sibling elements in the DOM tree, instead of forward):
<h1>prevUntil()</h1>
The <b>prevUntil()</b> method works just like the methods above but with reverse functionality; it returns previous sibling elements (traverse backwards along sibling elements in the DOM tree, instead of forward):
