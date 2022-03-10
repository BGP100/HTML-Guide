In these chapters, you will learn about the following CSS background properties:
<ul>
  <li>background-color
  <li>background-image
  <li>background-repeat
  <li>background-attachment
  <li>background-position
  <li>background (shorthand property)
</ul>
The <b>background-color</b> property specifies the background color of an element.
<pre>
body {
  background-color: lightblue;
}
</pre>
<h1>Other Colors</h1>
You can set the background color for any HTML elements:
<pre>
h1 {
  background-color: green;
}

div {
  background-color: lightblue;
}

p {
  background-color: yellow;
}
</pre>
<h1>Opacity</h1>
The opacity property specifies the opacity of an element. It can take a value from 0.0 - 1.0. The lower value, the more transparent:
<img src="https://i.imgur.com/Wmr8FPU.jpg" width="100%">
<pre>
div {
  background-color: green;
  opacity: 0.3;
}
</pre>
<h1>Opacity with RGBA</h1>
If you do not want to apply opacity to child elements, like in our example above, use RGBA color values. The following example sets the opacity for the background color and not the text:
<img src="https://i.imgur.com/Wmr8FPU.jpg" width="100%">
You learned from our CSS Colors Chapter, that you can use RGB as a color value. In addition to RGB, you can use an RGB color value with an alpha channel (RGBA) - which specifies the opacity for a color.
<br>
An RGBA color value is specified with: rgba(red, green, blue, alpha). The alpha parameter is a number between 0.0 (fully transparent) and 1.0 (fully opaque).
<br>
<b>Tip:</b> You will learn more about RGBA Colors in our CSS Colors Chapter.
<pre>
div {
  background: rgba(0, 128, 0, 0.3) /* Green background with 30% opacity */
}
</pre>
