<a href="/JS/jQuery/Traversing/Main.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/jQuery/Traversing/Descendants.md">Next &gt;</a>
<hr>
The most basic filtering methods are <b>first()</b>, <b>last()</b> and <b>eq()</b>, which allow you to select a specific element based on its position in a group of elements.
<br>
Other filtering methods, like <b>filter()</b> and <b>not()</b> allow you to select elements that match, or do not match, a certain criteria.
<br>
<b>Filtering Methods:</b>
<ul>
  <li><a href="#first">first()</a></li>
  <li><a href="#last">last()</a></li>
  <li><a href="#eq">eq()</a></li>
  <li><a href="#filter">filter()</a></li>
  <li><a href="#not">not()</a></li>
</ul>
<h1>first()</h1>
The <b>first()</b> method returns the first element of the specified elements:
<pre>
$(document).ready(function(){
  $("div").first();
});
</pre>
<h1>last()</h1>
The <b>last()</b> method returns the last element of the specified elements:
<pre>
$(document).ready(function(){
  $("div").last();
});
</pre>
<h1>eq()</h1>
The <b>eq()</b> method returns an element with a specific index number of the selected elements:
<pre>
$(document).ready(function(){
  $("p").eq(1);
});
</pre>
<h1>filter()</h1>
The <b>filter()</b> method lets you specify a criteria. Elements that do not match the criteria are removed from the selection, and those that match will be returned:
<pre>
$(document).ready(function(){
  $("p").eq(1);
});
</pre>
<h1>not()</h1>
<b><i>Tip:</i></b> The <b>not()</b> method is the opposite of <b>filter()</b>.
<br>
The <b>not()</b> method returns all elements that do not match the criteria:
<pre>
$(document).ready(function(){
  $("p").not(".intro");
});
</pre>
