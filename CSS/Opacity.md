<a href="/CSS/Pseudo-Element.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/NavigationBar/Main.md">Next &gt;</a>
<hr>
The <b>opacity</b> property specifies the opacity/transparency of an element.
<hr>
The <b>opacity</b> property can take a value from 0.0 - 1.0. The lower value, the more transparent:
<br>
<b>0.2 Opacity:</b>
<br>
<img src="https://i.imgur.com/Aw3IHWe.png" width="286px" height="190px">
<br>
<b>0.5 Opacity:</b>
<br>
<img src="https://i.imgur.com/Onh3HPn.png" width="286px" height="190px">
<br>
<b>1.0 Opacity (default):</b>
<br>
<img src="https://i.imgur.com/FPZIybF.png" width="286px" height="190px">
<pre>
img {
  opacity: 0.5;
}
</pre>
<h1>Hover Opacity Effect</h1>
The <b>opacity</b> property is often used together with the <b>:hover</b> selector to change the opacity on mouse-over:
<pre>
img {
  opacity: 0.5;
}
img:hover {
  opacity: 1.0;
}
</pre>
The first CSS block is similar to the code in Example 1. In addition, we have added what should happen when a user hovers over one of the images. In this case we want the image to NOT be transparent when the user hovers over it. The CSS for this is <b>opacity:1;</b>.
<br>
When the mouse pointer moves away from the image, the image will be transparent again.
<pre>
img {
  opacity: 1.0;
}
img:hover {
  opacity: 0.5;
}
</pre>
<h1>Transparent Elements</h1>
When using the <b>opacity</b> property to add transparency to the background of an element, all of its child elements inherit the same transparency. This can make the text inside a fully transparent element hard to read:
<br>
<img src="https://i.imgur.com/33iizzh.png" width="100%">
<pre>
div.op1 {
  opacity: 1.0;
}
div.op0-6 {
  opacity: 0.6;
}
div.op0-3 {
  opacity: 0.3;
}
div.op0-1 {
  opacity: 0.1;
}
</pre>
<h1>Transparent Elements with RGBA</h1>
If you do not want to apply opacity to child elements, like in our example above, use <b>RGBA</b> color values. The following example sets the opacity for the background color and not the text:
<br>
<img src="https://i.imgur.com/s6oBxCE.png" width="100%">
<pre>
div.op1 {
  background: rgba(76, 175, 80, 1.0) /* Green background with 100% opacity */
}
div.op0-6 {
  background: rgba(76, 175, 80, 0.3) /* Green background with 60% opacity */
}
div.op0-3 {
  background: rgba(76, 175, 80, 0.3) /* Green background with 30% opacity */
}
div.op0-1 {
  background: rgba(76, 175, 80, 0.1) /* Green background with 10% opacity */
}
</pre>
<h1>Text in Transparent Box</h1>
<img src="https://i.imgur.com/pxtOn9P.png" width="100%">
<pre>
div.background {
  background: url(klematis.jpg) repeat;
  border: 2px solid black;
}
div.transbox {
  margin: 30px;
  background-color: #ffffff;
  border: 1px solid black;
  opacity: 0.6;
}
div.transbox p {
  margin: 5%;
  font-weight: bold;
  color: #000000;
}
</pre>
