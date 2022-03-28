With CSS you can add shadow to text and to elements.
<br>
In these chapters you will learn about the following properties:
<ul>
  <li><b>text-shadow</b></li>
  <li><b>box-shadow</b></li>
</ul>
<h1>Text Shadow</h1>
The CSS text-shadow property applies shadow to text.
<br>
In its simplest use, you only specify the horizontal shadow (2px) and the vertical shadow (2px):
<br>
<img src="https://i.imgur.com/Llk3XwQ.png">
<pre>
h1 {
  text-shadow: 2px 2px;
  background-color: blue;
}
</pre>
<hr>
Next, add a color to the shadow:
<br>
<img src="https://i.imgur.com/zi3SFYX.png">
<pre>
h1 {
  text-shadow: 2px 2px red;
}
</pre>
<hr>
Then, add a blur effect to the shadow:
<br>
<img src="https://i.imgur.com/PfDEwX6.png">
<pre>
h1 {
  text-shadow: 2px 2px 5px red;
}
</pre>
<hr>
The following example shows a white text with black shadow:
<br>
<img src="https://i.imgur.com/ZzVjg9Q.png" width="300px">
<pre>
h1 {
  color: white;
  text-shadow: 2px 2px 4px black;
}
</pre>
<hr>
The following example shows a red neon glow shadow:
<br>
<img src="https://i.imgur.com/PU40FQ3.png" width="280px">
<pre>
h1 {
  text-shadow: 0 0 3px red;
}
</pre>
<h1>Multiple Shadows</h1>
To add more than one shadow to the text, you can add a comma-separated list of shadows.
<br>
The following example shows a red and blue neon glow shadow:
<br>
<img src="https://i.imgur.com/OYfuwDe.png" width="290px">
<pre>
h1 {
  text-shadow: 0 0 3px #FF0000, 0 0 5px #0000FF;
}
</pre>
<hr>
The following example shows a white text with black, blue, and darkblue shadow:
<br>
<img src="https://i.imgur.com/8RBo6VW.png" width="300px">
<pre>
h1 {
  color: white;
  text-shadow: 1px 1px 2px black, 0 0 25px blue, 0 0 5px darkblue;
}
</pre>
<hr>
You can also use the text-shadow property to create a plain border around some text (without shadows):
<br>
<img src="https://i.imgur.com/1JO6LMA.png" width="280px">
<pre>
h1 {
  color: coral;
  text-shadow: -1px 0 black, 0 1px black, 1px 0 black, 0 -1px black;
}
</pre>
