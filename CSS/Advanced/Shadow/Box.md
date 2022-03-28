The CSS box-shadow property is used to apply one or more shadows to an element.
<h1>Horizontal &amp; Vertical Shadows</h1>
In its simplest use, you only specify a horizontal and a vertical shadow. The default color of the shadow is the current text-color.
<br>
<img src="https://i.imgur.com/Bywgw0q.jpg" width="50%">
<pre>
div {
  box-shadow: 10px 10px;
}
</pre>
<h1>Specify a Color for the Shadow</h1>
The <b>color</b> parameter defines the color of the shadow.
<br>
<img src="https://i.imgur.com/NtTxiiw.jpg" width="50%">
<pre>
div {
  box-shadow: 10px 10px lightblue;
}
</pre>
<h1>Blur Shadow Effect</h1>
The <b>blur</b> parameter defines the blur radius. The higher the number, the more blurred the shadow will be.
<br>
<img src="https://i.imgur.com/MVX48yS.jpg" width="50%">
<pre>
div {
  box-shadow: 10px 10px 5px lightblue;
}
</pre>
<h1>Spread Radius of Shadows</h1>
The <b>spread</b> parameter defines the spread radius. A positive value increases the size of the shadow, a negative value decreases the size of the shadow.
<br>
<img src="https://i.imgur.com/D3Nm4DC.jpg" width="50%">
<pre>
div {
  box-shadow: 10px 10px 5px 12px lightblue;
}
</pre>
<h1>inset</h1>
The <b>inset</b> parameter changes the shadow from an outer shadow (outset) to an inner shadow.
<br>
<img src="https://i.imgur.com/JeqMYVP.jpg" width="50%">
<pre>
div {
  box-shadow: 10px 10px 5px lightblue inset;
}
</pre>
<h1>Multiple Shadows</h1>
An element can also have multiple shadows:
<pre>

</pre>
<h1>Cards</h1>
<img src="https://i.imgur.com/X4FRbVJ.jpg" width="50%">
<img src="https://i.imgur.com/D69Iq1L.jpg" width="50%">
<pre>
div.card {
  width: 250px;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
  text-align: center;
}
</pre>
