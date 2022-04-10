<a href="/CSS/Borders/Main.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/Borders/Colors.md">Next &gt;</a>
<hr>
The <b>border-width</b> property specifies the width of the four borders.
<br>
The width can be set as a specific size (in px, pt, cm, em, etc) or by using one of the three pre-defined values: thin, medium, or thick:
<pre>
p.one {
  border-style: solid;
  border-width: 5px;
}
p.two {
  border-style: solid;
  border-width: medium;
}
p.three {
  border-style: dotted;
  border-width: 2px;
}
p.four {
  border-style: dotted;
  border-width: thick;
}
</pre>
<img src="https://i.imgur.com/m3uHrp3.png">
<br>
<img src="https://i.imgur.com/f61A1GH.png">
<br>
<img src="https://i.imgur.com/84V4K7W.png">
<br>
<img src="https://i.imgur.com/pIcg6I0.png">
<h1>Specific Side Widths</h1>
The <b>border-width</b> property can have from one to four values (for the top border, right border, bottom border, and the left border):
<pre>
p.one {
  border-style: solid;
  border-width: 5px 20px; /* 5px top and bottom, 20px on the sides */
}
p.two {
  border-style: solid;
  border-width: 20px 5px; /* 20px top and bottom, 5px on the sides */
}
p.three {
  border-style: solid;
  border-width: 25px 10px 4px 35px; /* 25px top, 10px right, 4px bottom and 35px left */
}
</pre>
<img src="https://i.imgur.com/gQR3JDG.png">
<br>
<img src="https://i.imgur.com/m2MhbGP.png">
<br>
<img src="https://i.imgur.com/4ncP8Dy.png">
