With the CSS border-image property, you can set an image to be used as the border around an element.
<hr>
The CSS border-image property allows you to specify an image to be used instead of the normal border around an element.
<br>
The property has three parts:
<ul>
  <li>The image to use as the border</li>
  <li>Where to slice the image</li>
  <li>Define whether the middle sections should be repeated or stretched</li>
</ul>
We will use the following image (//i.imgur.com/XWyLB6K.png):
<br>
<img src="https://i.imgur.com/XWyLB6K.png">
<br>
The <b>border-image</b> property takes the image and slices it into nine sections, like a tic-tac-toe board. It then places the corners at the corners, and the middle sections are repeated or stretched as you specify.
<br>
<b>Note:</b> For border-image to work, the element also needs the border property set!
<br>
Here, the middle sections of the image are repeated to create the border:
<br>
<img src="https://i.imgur.com/o07E3nF.jpg">
<pre>
#borderimg {
  border: 10px solid transparent;
  padding: 15px;
  border-image: url(//i.imgur.com/XWyLB6K.png) 30 round;
}
</pre>
Here, the middle sections of the image are stretched to create the border:
<br>
<img src="https://i.imgur.com/bhfpW8J.png">
<pre>
#borderimg {
  border: 10px solid transparent;
  padding: 15px;
  border-image: url(//i.imgur.com/XWyLB6K.png) 30 stretch;
}
</pre>
<h1>More Examples</h1>
<img src="https://i.imgur.com/wPdWmQ4.jpg">
<pre>
#borderimg {
  border: 10px solid transparent;
  padding: 15px;
  border-image: url(//i.imgur.com/XWyLB6K.png) 50 round;
}
</pre>
<img src="https://i.imgur.com/nR1opxr.jpg">
<pre>
#borderimg {
  border: 10px solid transparent;
  padding: 15px;
  border-image: url(//i.imgur.com/XWyLB6K.png) 20% round;
}
</pre>
<img src="https://i.imgur.com/otSDxxE.jpg">
<pre>
#borderimg {
  border: 10px solid transparent;
  padding: 15px;
  border-image: url(//i.imgur.com/XWyLB6K.png) 30% round;
}
</pre>
