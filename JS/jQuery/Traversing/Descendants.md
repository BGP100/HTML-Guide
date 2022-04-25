<a href="/JS/jQuery/Traversing/Main.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/jQuery/Traversing/Siblings.md">Next &gt;</a>
<hr>
<h1>Traversing Up the DOM Tree</h1>
Two useful jQuery methods for traversing down the DOM tree are:
<ul>
  <li><a href="#children">children()</a></li>
  <li><a href="#find">find()</a></li>
</ul>
<h1>children()</h1>
The <b>children()</b> method returns all direct children of the selected element.
<br>
This method only traverses a single level down the DOM tree.
<br>
The following example returns all elements that are direct children of each <b>&lt;div&gt;</b> elements:
<pre>
$(document).ready(function(){
  $("div").children();
});
</pre>
You can also use an optional parameter to filter the search for children.
<br>
The following example returns all <b>&lt;p&gt;</b> elements with the class name "first", that are direct children of <b>&lt;div&gt;</b>:
<pre>
$(document).ready(function(){
  $("div").children("p.first");
});
</pre>
<h1>find()</h1>
The <b>find()</b> method returns descendant elements of the selected element, all the way down to the last descendant.
<br>
The following example returns all <b>&lt;span&gt;</b> elements that are descendants of <b>&lt;div&gt;</b>:
<pre>
$(document).ready(function(){
  $("div").find("span");
});
</pre>
The following example returns all descendants of <b>&lt;div&gt;</b>:
<pre>
$(document).ready(function(){
  $("div").find("*");
});
</pre>
