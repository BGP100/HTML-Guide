<a href="/CSS/Grid/Container.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/Responsive/Main.md">Next &gt;</a>
<hr>
<b>Note:</b> if you cant read text on images below, either you are blind or you have dark mode on.
<h1>Child Elements</h1>
A grid container contains grid items.
<br>
By default, a container has one grid item for each column, in each row, but you can style the grid items so that they will span multiple columns and/or rows.
<br>
<img src="https://i.imgur.com/62XcAD6.png">
<h1>grid-column</h1>
The <b>grid-column</b> property defines on which column(s) to place an item.
<br>
You define where the item will start, and where the item will end.
<br>
<img src="https://i.imgur.com/4vrDEOh.png">
<br>
To place an item, you can refer to line numbers, or use the keyword "span" to define how many columns the item will span.
<pre>
.item1 {
  grid-column: 1 / 5;
}
</pre>
<pre>
.item1 {
  grid-column: 1 / span 3;
}
</pre>
<pre>
.item2 {
  grid-column: 2 / span 3;
}
</pre>
<h1>grid-row</h1>
The <b>grid-row</b> property defines on which row to place an item.
<br>
You define where the item will start, and where the item will end.
<br>
<img src="https://i.imgur.com/emhKSV3.png">
<br>
To place an item, you can refer to line numbers, or use the keyword "span" to define how many rows the item will span:
<pre>
.item1 {
  grid-row: 1 / 4;
}
</pre>
<pre>
.item1 {
  grid-row: 1 / span 2;
}
</pre>
<h1>grid-area</h1>
The <b>grid-area</b> property can be used as a shorthand property for the <b>grid-row-start</b>, <b>grid-column-start</b>, <b>grid-row-end</b> and the <b>grid-column-end</b> properties.
<br>
<img src="https://i.imgur.com/490BD2v.png">
<pre>
.item8 {
  grid-area: 1 / 2 / 5 / 6;
}
</pre>
<pre>
.item8 {
  grid-area: 2 / 1 / span 2 / span 3;
}
</pre>
<h1>grid-area</h1>
The grid-area property can also be used to assign names to grid items.
<br>
<img src="https://i.imgur.com/OOIzcDR.png">
<br>
Named grid items can be referred to by the <b>grid-template-areas</b> property of the grid container.
<pre>
.item1 {
  grid-area: myArea;
}
.grid-container {
  grid-template-areas: 'myArea myArea myArea myArea myArea';
}
</pre>
Each row is defined by apostrophes (' ')
<br>
The columns in each row is defined inside the apostrophes, separated by a space.
<pre>
.item1 {
  grid-area: myArea;
}
.grid-container {
  grid-template-areas: 'myArea myArea . . .';
}
</pre>
<pre>
.grid-container {
  grid-template-areas: 'myArea myArea . . .' 'myArea myArea . . .';
}
</pre>
<pre>
.item1{grid-area:header;}
.item2{grid-area:menu;}
.item3{grid-area:main;}
.item4{grid-area:right;}
.item5{grid-area:footer;}
.grid-container {
  grid-template-areas: 'header header header header header header' 'menu main main main right right' 'menu footer footer footer footer footer';
}
</pre>
<h1>Order</h1>
The Grid Layout allows us to position the items anywhere we like.
<br>
<img src="https://i.imgur.com/Cb0OrLt.png">
<pre>
.item1 { grid-area: 1 / 3 / 2 / 4; }
.item2 { grid-area: 2 / 3 / 3 / 4; }
.item3 { grid-area: 1 / 1 / 2 / 2; }
.item4 { grid-area: 1 / 2 / 2 / 3; }
.item5 { grid-area: 2 / 1 / 3 / 2; }
.item6 { grid-area: 2 / 2 / 3 / 3; }
</pre>
<pre>
@media only screen and (max-width: 500px) {
  .item1 { grid-area: 1 / span 3 / 2 / 4; }
  .item2 { grid-area: 3 / 3 / 4 / 4; }
  .item3 { grid-area: 2 / 1 / 3 / 2; }
  .item4 { grid-area: 2 / 2 / span 2 / 3; }
  .item5 { grid-area: 3 / 1 / 4 / 2; }
  .item6 { grid-area: 2 / 3 / 3 / 4; }
}
</pre>
