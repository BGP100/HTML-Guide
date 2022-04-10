<a href="/HTML/Lists/Main.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/HTML/Lists/Ordered.md">Next &gt;</a>
<hr>
The HTML ul tag defines an unordered (bulleted) list.
<br>
An unordered list starts with the ul tag. Each list item starts with the li tag.
<br>
The list items will be marked with bullets (small black circles) by default:
<pre>
&lt;ul&gt;
  &lt;li&gt;Coffee&lt;/li&gt;
  &lt;li&gt;Tea&lt;/li&gt;
  &lt;li&gt;Milk&lt;/li&gt;
&lt;/ul&gt;
</pre>
<h1>Markers</h1>
The CSS list-style-type property is used to define the style of the list item marker. It can have one of the following values:
<br>
<b>Disc:</b>
<pre>
&lt;ul style="list-style-type:disc;"&gt;
  &lt;li&gt;Coffee&lt;/li&gt;
  &lt;li&gt;Tea&lt;/li&gt;
  &lt;li&gt;Milk&lt;/li&gt;
&lt;/ul&gt;
</pre>
<b>Circle:</b>
<pre>
&lt;ul style="list-style-type:circle;"&gt;
  &lt;li&gt;Coffee&lt;/li&gt;
  &lt;li&gt;Tea&lt;/li&gt;
  &lt;li&gt;Milk&lt;/li&gt;
&lt;/ul&gt;
</pre>
<b>Square:</b>
<pre>
&lt;ul style="list-style-type:square;"&gt;
  &lt;li&gt;Coffee&lt;/li&gt;
  &lt;li&gt;Tea&lt;/li&gt;
  &lt;li&gt;Milk&lt;/li&gt;
&lt;/ul&gt;
</pre>
<b>None:</b>
<pre>
&lt;ul style="list-style-type:none;"&gt;
  &lt;li&gt;Coffee&lt;/li&gt;
  &lt;li&gt;Tea&lt;/li&gt;
  &lt;li&gt;Milk&lt;/li&gt;
&lt;/ul&gt;
</pre>
<h1>Nested</h1>
Lists can be nested (list inside of list):
<pre>
&lt;ul&gt;
  &lt;li&gt;Coffee&lt;/li&gt;
  &lt;li&gt;Tea
    &lt;ul&gt;
      &lt;li&gt;Black tea&lt;/li&gt;
      &lt;li&gt;Green tea&lt;/li&gt;
    &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li&gt;Milk&lt;/li&gt;
&lt;/ul&gt;
</pre>
<h1>Horizontal Lists</h1>
HTML lists can be styled in many different ways with CSS.
<br>
One popular way is to style a list horizontally, to create a navigation menu:
<b>CSS:</b>
<pre>
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  overflow: hidden;
  background-color: #333333;
}
li {
  float: left;
}
li a {
  display: block;
  color: white;
  text-align: center;
  padding: 16px;
  text-decoration: none;
}
li a:hover {
  background-color: #111111;
}
</pre>
<b>HTML:</b>
<pre>
&lt;ul&gt;
  &lt;li&gt;&lt;a href="#home">Home&lt;/a&gt;&lt;/li&gt;
  &lt;li&gt;&lt;a href="#news">News&lt;/a&gt;&lt;/li&gt;
  &lt;li&gt;&lt;a href="#contact">Contact&lt;/a&gt;&lt;/li&gt;
  &lt;li&gt;&lt;a href="#about">About&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
</pre>
