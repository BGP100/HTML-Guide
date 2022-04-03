<b>Note:</b> if you cant read text on images below, either you are blind or you have dark mode on.
<hr>
The CSS Grid Layout Module offers a grid-based layout system, with rows and columns, making it easier to design web pages without having to use floats and positioning:
<br>
<img src="https://i.imgur.com/OOIzcDR.png">
<h1>Browser Support</h1>
The grid properties are supported in all modern browsers.
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
    <td>57.0</td>
    <td>16.0</td>
    <td>52.0</td>
    <td>10.0</td>
    <td>44.0</td>
  </tr>
</table>
<h1>Elements</h1>
A grid layout consists of a parent element, with one or more child elements.
<pre>
&lt;div class="grid-container"&gt;
  &lt;div class="grid-item"&gt;1&lt;/div&gt;
  &lt;div class="grid-item"&gt;2&lt;/div&gt;
  &lt;div class="grid-item"&gt;3&lt;/div&gt;
  &lt;div class="grid-item"&gt;4&lt;/div&gt;
  &lt;div class="grid-item"&gt;5&lt;/div&gt;
  &lt;div class="grid-item"&gt;6&lt;/div&gt;
  &lt;div class="grid-item"&gt;7&lt;/div&gt;
  &lt;div class="grid-item"&gt;8&lt;/div&gt;
  &lt;div class="grid-item"&gt;9&lt;/div&gt;
&lt;/div&gt;
</pre>
<pre>
.grid-item {
  background-color: rgba(255, 255, 255, 0.8);
  color:#000;  
  border: 1px solid rgba(0, 0, 0, 0.8);
}
</pre>
<img src="https://i.imgur.com/c9zEjGm.png">
<h1>Display</h1>
An HTML element becomes a grid container when its display property is set to <b>grid</b> or <b>inline-grid</b>.
<pre>
.grid-container {
  display: grid;
}
</pre>
<pre>
.grid-container {
  display: inline-grid;
}
</pre>
All direct children of the grid container automatically become <i>grid items</i>.
<h1>Columns</h1>
The vertical lines of grid items are called <b>columns</b>.
<br>
<img src="https://i.imgur.com/xnQPkl4.png">
<h1>Rows</h1>
The horizontal lines of grid items are called <b>rows</b>.
<br>
<img src="https://i.imgur.com/U0xWj16.png">
<h1>Gaps</h1>
The spaces between each column/row are called <b>gaps</b>.
<br>
<img src="https://i.imgur.com/B1x3fsg.png">
<br>
You can adjust the gap size by using one of the following properties:
<ul>
  <li><b>column-gap</b></li>
  <li><b>row-gap</b></li>
  <li><b>gap</b></li>
</ul>
<pre>
.grid-container {
  display: grid;
  column-gap: 50px;
}
</pre>
<pre>
.grid-container {
  display: grid;
  row-gap: 50px;
}
</pre>
<pre>
.grid-container {
  display: grid;
  gap: 50px 100px;
}
</pre>
<pre>
.grid-container {
  display: grid;
  gap: 50px;
}
</pre>
<h1>Lines</h1>
The lines between columns are called column lines.
<br>
The lines between rows are called row lines.
<br>
<img src="https://i.imgur.com/ccy6qBu.png">
<br>
Refer to line numbers when placing a grid item in a grid container:
<pre>
.item1 {
  grid-column-start: 1;
  grid-column-end: 3;
}
</pre>
<pre>
.item1 {
  grid-row-start: 1;
  grid-row-end: 3;
}
</pre>
