<a href="/CSS/Advanced/Flexbox/Container.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/Advanced/Flexbox/Responsive.md">Next &gt;</a>
<hr>
<h1>Child Elements</h1>
The direct child elements of a flex container automatically becomes flexible (flex) items.
<br>
<img src="https://i.imgur.com/6eyR02u.png" width="100%">
<br>
The element above represents four blue flex items inside a grey flex container.
<pre>
&lt;div class="flex-container"&gt;
  &lt;div&gt;1&lt;/div&gt;
  &lt;div&gt;2&lt;/div&gt;
  &lt;div&gt;3&lt;/div&gt;
  &lt;div&gt;4&lt;/div&gt;
&lt;/div&gt;
</pre>
<h1>order</h1>
The order property specifies the order of the flex items.
<br>
<img src="https://i.imgur.com/5wqrCRM.png" width="100%">
<br>
The first flex item in the code does not have to appear as the first item in the layout.
<br>
The order value must be a number, default value is 0.
<pre>
&lt;div class="flex-container"&gt;
  &lt;div style="order:3"&gt;1&lt;/div&gt;
  &lt;div style="order:2"&gt;2&lt;/div&gt;
  &lt;div style="order:4"&gt;3&lt;/div&gt;
  &lt;div style="order:1"&gt;4&lt;/div&gt;
&lt;/div&gt;
</pre>
<h1>flex-grow</h1>
The <b>flex-grow</b> property specifies how much a flex item will grow relative to the rest of the flex items.
<br>
<img src="https://i.imgur.com/Qmkhlln.png" width="100%">
<br>
The value must be a number, default value is 0.
<pre>
&lt;div class="flex-container"&gt;
  &lt;div style="flex-grow:1"&gt;1&lt;/div&gt;
  &lt;div style="flex-grow:1"&gt;2&lt;/div&gt;
  &lt;div style="flex-grow:8"&gt;3&lt;/div&gt;
&lt;/div&gt;
</pre>
<h1>flex-shrink</h1>
The <b>flex-shrink</b> property specifies how much a flex item will shrink relative to the rest of the flex items.
<br>
<img src="https://i.imgur.com/i47nc0a.png" width="100%">
<br>
The value must be a number, default value is 1.
<pre>
&lt;div class="flex-container"&gt;
  &lt;div&gt;1&lt;/div&gt;
  &lt;div&gt;2&lt;/div&gt;
  &lt;div style="flex-shrink:0"&gt;3&lt;/div&gt;
  &lt;div&gt;4&lt;/div&gt;
  &lt;div&gt;5&lt;/div&gt;
  &lt;div&gt;6&lt;/div&gt;
  &lt;div&gt;7&lt;/div&gt;
  &lt;div&gt;8&lt;/div&gt;
  &lt;div&gt;9&lt;/div&gt;
  &lt;div&gt;1&lt;/div&gt;
&lt;/div&gt;
</pre>
<h1>flex-basis</h1>
The <b>flex-basis</b> property specifies the initial length of a flex item.
<br>
<img src="https://i.imgur.com/7LZ1HQl.png" width="100%">
<pre>
&lt;div class="flex-container"&gt;
  &lt;div&gt;1&lt;/div&gt;
  &lt;div&gt;2&lt;/div&gt;
  &lt;div style="flex-basis: 200px"&gt;3&lt;/div&gt;
  &lt;div&gt;4&lt;/div&gt;
&lt;/div&gt;
</pre>
<h1>flex</h1>
The <b>flex</b> property is a shorthand property for the flex-grow, flex-shrink, and flex-basis properties.
<pre>
&lt;div class="flex-container"&gt;
  &lt;div&gt;1&lt;/div&gt;
  &lt;div&gt;2&lt;/div&gt;
  &lt;div style="flex: 0 0 200px"&gt;3&lt;/div&gt;
  &lt;div&gt;4&lt;/div&gt;
&lt;/div&gt;
</pre>
<h1>align-self</h1>
The <b>align-self</b> property specifies the alignment for the selected item inside the flexible container.
<br>
The <b>align-self</b> property overrides the default alignment set by the container's align-items property.
<br>
<img src="https://i.imgur.com/99aMHK0.png" width="100%">
<br>
In these examples we use a 200 pixels high container, to better demonstrate the align-self property:
<pre>
&lt;div class="flex-container"&gt;
  &lt;div&gt;1&lt;/div&gt;
  &lt;div&gt;2&lt;/div&gt;
  &lt;div style="align-self: center"&gt;3&lt;/div&gt;
  &lt;div&gt;4&lt;/div&gt;
&lt;/div&gt;
</pre>
<pre>
&lt;div class="flex-container"&gt;
  &lt;div&gt;1&lt;/div&gt;
  &lt;div style="align-self: flex-start"&gt;2&lt;/div&gt;
  &lt;div style="align-self: flex-end"&gt;3&lt;/div&gt;
  &lt;div&gt;4&lt;/div&gt;
&lt;/div&gt;
</pre>
