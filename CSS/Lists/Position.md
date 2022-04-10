<a href="/CSS/Lists/Images.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/Lists/RemoveDefault.md">Next &gt;</a>
<hr>
The <b>list-style-position</b> property specifies the position of the list-item markers (bullet points).
<br>
"list-style-position: outside;" means that the bullet points will be outside the list item. The start of each line of a list item will be aligned vertically. This is default:
<br>
<img src="https://i.imgur.com/Ml0uGn7.jpg" width="25%">
<br>
"list-style-position: inside;" means that the bullet points will be inside the list item. As it is part of the list item, it will be part of the text and push the text at the start:
<br>
<img src="https://i.imgur.com/bEaH363.jpg" width="25%">
<pre>
ul.a {
  list-style-position: outside;
}
ul.b {
  list-style-position: inside;
}
</pre>
