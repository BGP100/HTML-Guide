<a href="/HTML/Lists/Unordered.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/HTML/Lists/Description.md">Next &gt;</a>
<hr>
The HTML ol tag defines an ordered list. An ordered list can be numerical or alphabetical.
<br>
An ordered list starts with the ol tag. Each list item starts with the li tag.
<br>
The list items will be marked with numbers by default:
<pre>
&lt;ol&gt;
  &lt;li&gt;Coffee&lt;/li&gt;
  &lt;li&gt;Tea&lt;/li&gt;
  &lt;li&gt;Milk&lt;/li&gt;
&lt;/ol&gt;
</pre>
<h1>Types</h1>
<b>Numbers:</b>
<pre>
&lt;ol type="1"&gt;
  &lt;li&gt;Coffee&lt;/li&gt;
  &lt;li&gt;Tea&lt;/li&gt;
  &lt;li&gt;Milk&lt;/li&gt;
&lt;/ol&gt;
</pre>
<b>Uppercase Letters:</b>
<pre>
&lt;ol type="A"&gt;
  &lt;li&gt;Coffee&lt;/li&gt;
  &lt;li&gt;Tea&lt;/li&gt;
  &lt;li&gt;Milk&lt;/li&gt;
&lt;/ol&gt;
</pre>
<b>Lowercase Letters:</b>
<pre>
&lt;ol type="a"&gt;
  &lt;li&gt;Coffee&lt;/li&gt;
  &lt;li&gt;Tea&lt;/li&gt;
  &lt;li&gt;Milk&lt;/li&gt;
&lt;/ol&gt;
</pre>
<b>Uppercase Roman Numbers:</b>
<pre>
&lt;ol type="I"&gt;
  &lt;li&gt;Coffee&lt;/li&gt;
  &lt;li&gt;Tea&lt;/li&gt;
  &lt;li&gt;Milk&lt;/li&gt;
&lt;/ol&gt;
</pre>
<b>Lowercase Roman Numbers:</b>
<pre>
&lt;ol type="i"&gt;
  &lt;li&gt;Coffee&lt;/li&gt;
  &lt;li&gt;Tea&lt;/li&gt;
  &lt;li&gt;Milk&lt;/li&gt;
&lt;/ol&gt;
</pre>
<h1>Control Counting</h1>
By default, an ordered list will start counting from 1. If you want to start counting from a specified number, you can use the start attribute:
<pre>
&lt;ol start="50"&gt;
  &lt;li&gt;Coffee&lt;/li&gt;
  &lt;li&gt;Tea&lt;/li&gt;
  &lt;li&gt;Milk&lt;/li&gt;
&lt;/ol&gt;
</pre>
<h1>Nested</h1>
Lists can be nested (list inside of list):
<pre>
&lt;ol&gt;
  &lt;li&gt;Coffee&lt;/li&gt;
  &lt;li&gt;Tea
    &lt;ol&gt;
      &lt;li&gt;Black tea&lt;/li&gt;
      &lt;li&gt;Green tea&lt;/li&gt;
    &lt;/ol&gt;
  &lt;/li&gt;
  &lt;li&gt;Milk&lt;/li&gt;
&lt;/ol&gt;
</pre>
