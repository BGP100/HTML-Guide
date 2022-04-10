<a href="/CSS/Background/Image.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/Background/Attachment.md">Next &gt;</a>
<hr>
By default, the <b>background-image</b> property repeats an image both horizontally and vertically.
<br>
Some images should be repeated only horizontally or vertically, or they will look strange, like this:
<pre>
body {
  background-image: url("gradient_bg.png");
}
</pre>
If the image above is repeated only horizontally (<b>background-repeat: repeat-x;</b>), the background will look better:
<pre>
body {
  background-image: url("gradient_bg.png");
  background-repeat: repeat-x;
}
</pre>
<h1>no-repeat</h1>
Showing the background image only once is also specified by the <b>background-repeat</b> property:
<pre>
body {
  background-image: url("img_tree.png");
  background-repeat: no-repeat;
}
</pre>
In the example above, the background image is placed in the same place as the text. We want to change the position of the image, so that it does not disturb the text too much.
<h1>background-position</h1>
The <b>background-position</b> property is used to specify the position of the background image.
<pre>
body {
  background-image: url("img_tree.png");
  background-repeat: no-repeat;
  background-position: right top;
}
</pre>
