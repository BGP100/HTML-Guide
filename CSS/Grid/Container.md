<b>Note:</b> if you cant read text on images below, either you are blind or you have dark mode on.
<hr>
To make an HTML element behave as a grid container, you have to set the display property to grid or inline-grid.
<br>
Grid containers consist of grid items, placed inside columns and rows.
<br>
<img src="https://i.imgur.com/nf2e6D7.png">
<h1>grid-template-columns</h1>
The <b>grid-template-columns</b> property defines the number of columns in your grid layout, and it can define the width of each column.
<br>
The value is a space-separated-list, where each value defines the width of the respective column.
<br>
If you want your grid layout to contain 4 columns, specify the width of the 4 columns, or "auto" if all columns should have the same width.
<pre>
.grid-container {
  display: grid;
  grid-template-columns: auto auto auto auto;
}
</pre>
The grid-template-columns property can also be used to specify the size (width) of the columns.
<pre>
.grid-container {
  display: grid;
  grid-template-columns: 80px 200px auto 40px;
}
</pre>
<h1>grid-template-rows</h1>
The <b>grid-template-rows</b> property defines the height of each row.
<br>
<img src="https://i.imgur.com/nf2e6D7.png">
<br>
The value is a space-separated-list, where each value defines the height of the respective row:
<pre>
.grid-container {
  display: grid;
  grid-template-rows: 80px 200px;
}
</pre>
<h1>justify-content</h1>
The <b>justify-content</b> property is used to align the whole grid inside the container.
<br>
<img src="https://i.imgur.com/STmVHk2.png">
<pre>
.grid-container {
  display: grid;
  justify-content: space-evenly;
}
</pre>
<pre>
.grid-container {
  display: grid;
  justify-content: space-around;
}
</pre>
<pre>
.grid-container {
  display: grid;
  justify-content: space-between;
}
</pre>
<pre>
.grid-container {
  display: grid;
  justify-content: center;
}
</pre>
<pre>
.grid-container {
  display: grid;
  justify-content: start;
}
</pre>
<pre>
.grid-container {
  display: grid;
  justify-content: end;
}
</pre>
<h1>align-content</h1>
The <b>align-content</b> property is used to vertically align the whole grid inside the container.
<br>
<img src="https://i.imgur.com/HfbLi6W.png">
<pre>
.grid-container {
  display: grid;
  height: 400px;
  align-content: center;
}
</pre>
<pre>
.grid-container {
  display: grid;
  height: 400px;
  align-content: space-evenly;
}
</pre>
<pre>
.grid-container {
  display: grid;
  height: 400px;
  align-content: space-around;
}
</pre>
<pre>
.grid-container {
  display: grid;
  height: 400px;
  align-content: space-between;
}
</pre>
<pre>
.grid-container {
  display: grid;
  height: 400px;
  align-content: start;
}
</pre>
<pre>
.grid-container {
  display: grid;
  height: 400px;
  align-content: end;
}
</pre>
