<a href="/CSS/Float/Examples.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/Align.md">Next &gt;</a>
<hr>
Compared to <b>display: inline</b>, the major difference is that <b>display: inline-block</b> allows to set a width and height on the element.
<br>
Also, with <b>display: inline-block</b>, the top and bottom margins/paddings are respected, but with <b>display: inline</b> they are not.
<br>
Compared to <b>display: block</b>, the major difference is that <b>display: inline-block</b> does not add a line-break after the element, so the element can sit next to other elements.
<br>
The following example shows the different behavior of <b>display: inline</b>, <b>display: inline-block</b> and <b>display: block</b>:
<pre>
span.a {
  display: inline; /* the default for span */
  width: 100px;
  height: 100px;
  padding: 5px;
  border: 1px solid blue; 
  background-color: yellow; 
}
span.b {
  display: inline-block;
  width: 100px;
  height: 100px;
  padding: 5px;
  border: 1px solid blue; 
  background-color: yellow; 
}
span.c {
  display: block;
  width: 100px;
  height: 100px;
  padding: 5px;
  border: 1px solid blue; 
  background-color: yellow; 
}
</pre>
<h1>Creating Navigation Links</h1>
One common use for <b>display: inline-block</b> is to display list items horizontally instead of vertically. The following example creates horizontal navigation links:
<pre>
.nav {
  background-color: yellow; 
  list-style-type: none;
  text-align: center; 
  padding: 0;
  margin: 0;
}
.nav li {
  display: inline-block;
  font-size: 20px;
  padding: 20px;
}
</pre>
