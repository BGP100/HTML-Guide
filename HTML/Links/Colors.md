An HTML link is displayed in a different color depending on whether it has been visited, is unvisited, or is active.
<br>
By default, a link will appear like this (in all browsers):
<ul>
  <li>An unvisited link is underlined and blue.</li>
  <li>A visited link is underlined and purple.</li>
  <li>A non-active link is underlined and red.</li>
</ul>
You can change the link state colors, by using CSS:
<pre>
&lt;style&gt;
a:link {
  color: green;
  background-color: transparent;
  text-decoration: none;
}
a:visited {
  color: pink;
  background-color: transparent;
  text-decoration: none;
}
a:hover {
  color: red;
  background-color: transparent;
  text-decoration: underline;
}
a:active {
  color: yellow;
  background-color: transparent;
  text-decoration: underline;
}
&lt;/style&gt;
</pre>
<h1>Buttons</h1>
A link can also be styled as a button, by using CSS.
<pre>
&lt;style&gt;
a:link, a:visited {
  background-color: #f44336;
  color: white;
  padding: 15px 25px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
}

a:hover, a:active {
  background-color: red;
}
&lt;/style&gt;
</pre>
