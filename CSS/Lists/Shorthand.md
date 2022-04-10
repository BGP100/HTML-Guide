<a href="/CSS/Lists/RemoveDefault.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/Lists/Styling.md">Next &gt;</a>
<hr>
The <b>list-style</b> property is a shorthand property. It is used to set all the list properties in one declaration:
<pre>
ul {
  list-style: square inside url("//i.imgur.com/GvhqiWe.gif");
}
</pre>
When using the shorthand property, the order of the property values are:
<ul>
<li><b>list-style-type</b> (if a list-style-image is specified, the value of this property will be displayed if the image for some reason cannot be displayed)</li>
<li><b>list-style-position</b> (specifies whether the list-item markers should appear inside or outside the content flow)</li>
<li><b>list-style-image</b> (specifies an image as the list item marker)</li>
</ul>
If one of the property values above are missing, the default value for the missing property will be inserted, if any.
