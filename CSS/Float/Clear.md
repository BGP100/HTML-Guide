When we use the <b>float</b> property, and we want the next element below (not on right or left), we will have to use the <b>clear</b> property.
<br>
The <b>clear</b> property specifies what should happen with the element that is next to a floating element.
<br>
The <b>clear</b> property can have one of the following values:
<ul>
  <li><b>none</b> - The element is not pushed below left or right floated elements. This is default.</li>
  <li><b>left</b> - The element is pushed below left floated elements.</li>
  <li><b>right</b> - The element is pushed below right floated elements.</li>
  <li><b>both</b> - The element is pushed below both left and right floated elements.</li>
  <li><b>inherit</b> - The element inherits the clear value from its parent.</li>
</ul>
When clearing floats, you should match the clear to the float: If an element is floated to the left, then you should clear to the left. Your floated element will continue to float, but the cleared element will appear below it on the web page.
<pre>
div1 {
  float: left;
}
div2 {
  clear: left;
}
</pre>
