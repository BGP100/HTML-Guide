<a href="/CSS/Advanced/Flexbox/Main.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/Advanced/Flexbox/Items.md">Next &gt;</a>
<hr>
Like we specified in the previous chapter, this is a flex container (the blue area) with three flex items:
<br>
<img src="https://i.imgur.com/JO6Mtim.png" width="100%">
<br>
The flex container becomes flexible by setting the display property to flex:
<pre>
.flex-container {
  display: flex;
}
</pre>
The <b>flex-direction</b> property defines in which direction the container wants to stack the flex items.
<br>
<img src="https://i.imgur.com/Fa7Dei0.png" width="100%">
<pre>
.flex-container {
  display: flex;
  flex-direction: column;
}
</pre>
<pre>
.flex-container {
  display: flex;
  flex-direction: column-reverse;
}
</pre>
<pre>
.flex-container {
  display: flex;
  flex-direction: row;
}
</pre>
<pre>
.flex-container {
  display: flex;
  flex-direction: row-reverse;
}
</pre>
The <b>flex-wrap</b> property specifies whether the flex items should wrap or not.
<br>
The examples below have 12 flex items, to better demonstrate the <b>flex-wrap</b> property.
<br>
<img src="https://i.imgur.com/aRc8shx.png" width="100%">
<pre>
.flex-container {
  display: flex;
  flex-wrap: wrap;
}
</pre>
<pre>
.flex-container {
  display: flex;
  flex-wrap: nowrap;
}
</pre>
<pre>
.flex-container {
  display: flex;
  flex-wrap: wrap-reverse;
}
</pre>
<h1>The Property</h1>
The <b>flex-flow</b> property is a shorthand property for setting both the <b>flex-direction</b> and <b>flex-wrap</b> properties.
<pre>
.flex-container {
  display: flex;
  flex-flow: row wrap;
}
</pre>
<h1>justify-content</h1>
The <b>justify-content</b> property is used to align the flex items:
<br>
<img src="https://i.imgur.com/jrFZqLN.png" width="100%">
<pre>
.flex-container {
  display: flex;
  justify-content: center;
}
</pre>
<pre>
.flex-container {
  display: flex;
  justify-content: flex-start;
}
</pre>
<pre>
.flex-container {
  display: flex;
  justify-content: flex-end;
}
</pre>
<pre>
.flex-container {
  display: flex;
  justify-content: space-around;
}
</pre>
<pre>
.flex-container {
  display: flex;
  justify-content: space-between;
}
</pre>
<h1>align-items</h1>
The <b>align-items</b> property is used to align the flex items.
<br>
<img src="https://i.imgur.com/cjhJGzZ.png" width="100%">
<br>
In these examples we use a 200 pixels high container, to better demonstrate the align-items property.
<pre>
.flex-container {
  display: flex;
  height: 200px;
  align-items: center;
}
</pre>
<pre>
.flex-container {
  display: flex;
  height: 200px;
  align-items: flex-start;
}
</pre>
<pre>
.flex-container {
  display: flex;
  height: 200px;
  align-items: flex-end;
}
</pre>
<pre>
.flex-container {
  display: flex;
  height: 200px;
  align-items: stretch;
}
</pre>
<pre>
.flex-container {
  display: flex;
  height: 200px;
  align-items: baseline;
}
</pre>
<h1>align-content</h1>
The <b>align-content</b> property is used to align the flex lines.
<br>
<img src="https://i.imgur.com/X9GPQDp.png" width="100%">
<br>
In these examples we use a 600 pixels high container, with the flex-wrap property set to wrap, to better demonstrate the align-content property.
<pre>
.flex-container {
  display: flex;
  height: 600px;
  flex-wrap: wrap;
  align-content: space-between;
}
</pre>
<pre>
.flex-container {
  display: flex;
  height: 600px;
  flex-wrap: wrap;
  align-content: space-around;
}
</pre>
<pre>
.flex-container {
  display: flex;
  height: 600px;
  flex-wrap: wrap;
  align-content: stretch;
}
</pre>
<pre>
.flex-container {
  display: flex;
  height: 600px;
  flex-wrap: wrap;
  align-content: center;
}
</pre>
<pre>
.flex-container {
  display: flex;
  height: 600px;
  flex-wrap: wrap;
  align-content: flex-start;
}
</pre>
<pre>
.flex-container {
  display: flex;
  height: 600px;
  flex-wrap: wrap;
  align-content: flex-end;
}
</pre>
<h1>Cenetring</h1>
In the following example we will solve a very common style problem: perfect centering.
<br>
<img src="https://i.imgur.com/gTxUIzx.png" width="100%">
<pre>
.flex-container {
  display: flex;
  height: 300px;
  justify-content: center;
  align-items: center;
}
</pre>
