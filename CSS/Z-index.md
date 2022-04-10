<a href="/CSS/Position.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/Overflow.md">Next &gt;</a>
<hr>
The <b>z-index</b> property specifies the stack order of an element.
<br>
When elements are positioned, they can overlap other elements.
<br>
The <b>z-index</b> property specifies the stack order of an element (which element should be placed in front of, or behind, the others).
<br>
An element can have a positive or negative stack order:
<br>
<img src="https://i.imgur.com/5rHGCjW.jpg" width="69%">
<pre>
img {
  position: absolute;
  left: 0px;
  top: 0px;
  z-index: -1;
}
</pre>
<b><i>Note:</i></b> <b>z-index</b> only works on positioned elements (position: absolute, position: relative, position: fixed, or position: sticky) and flex items (elements that are direct children of display: flex elements).
<br>
<a href="Position.md">Click Here</a> to know more about positioned elements.
