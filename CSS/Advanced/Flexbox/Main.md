<a href="/CSS/Advanced/MediaQueries.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/Advanced/Flexbox/Container.md">Next &gt;</a>
<hr>
<img src="https://i.imgur.com/z1nK93j.png" width="100%">
<hr>
Before the Flexbox Layout module, there were four layout modes:
<ul>
Block, for sections in a webpage
Inline, for text
Table, for two-dimensional table data
Positioned, for explicit position of an element
</ul>
The Flexible Box Layout Module, makes it easier to design flexible responsive layout structure without using float or positioning.
<h1>Browser Support</h1>
The flexbox properties are supported in all modern browsers.
<table class="ws-table-all notranslate">
  <tr>
    <th>Browser</th>
    <th>Chrome</th>
    <th>Edge</th>
    <th>Firefox</th>
    <th>Safari</th>
    <th>Opera</th>
  </tr>
  <tr>
    <td>Version</td>
    <td>49.0</td>
    <td>15.0</td>
    <td>31.0</td>
    <td>9.1</td>
    <td>36.0</td>
  </tr>
</table>
<h1>Elements</h1>
To start using the Flexbox model, you need to first define a flex container.
<br>
<img src="https://i.imgur.com/JO6Mtim.png" width="100%">
<br>
The element above represents a flex container (the blue area) with three flex items.
<pre>
&lt;div class="flex-container"&gt;
  &lt;div&gt;1&lt;/div&gt;
  &lt;div&gt;2&lt;/div&gt;
  &lt;div&gt;3&lt;/div&gt;
&lt;/div&gt;
</pre>
