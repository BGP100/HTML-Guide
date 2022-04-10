<a href="/CSS/Advanced/ImageReflection.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/Advanced/Object-position.md">Next &gt;</a>
<hr>
The CSS object-fit property is used to specify how an <b>&lt;img&gt;</b> or <b>&lt;video&gt;</b> should be resized to fit its container.
<hr>
The CSS object-fit property is used to specify how an <b>&lt;img&gt;</b> or <b>&lt;video&gt;</b> should be resized to fit its container.
<br>
This property tells the content to fill the container in a variety of ways; such as "preserve that aspect ratio" or "stretch up and take up as much space as possible".
<br>
Look at the following image from Paris. This image is 400 pixels wide and 300 pixels high:
<br>
<img src="https://i.imgur.com/YHAVU6Z.jpg">
<br>
However, if we style the image above to be half its width (200 pixels) and same height (300 pixels), it will look like this:
<br>
<img src="https://i.imgur.com/xEUMnxe.jpg">
<pre>
img {
  width: 200px;
  height: 300px;
}
</pre>
We see that the image is being squished to fit the container of 200x300 pixels (its original aspect ratio is destroyed).
<br>
Here is where the object-fit property comes in. The object-fit property can take one of the following values:
<ul>
  <li><b>fill</b> - This is default. The image is resized to fill the given dimension. If necessary, the image will be stretched or squished to fit</li>
  <li><b>contain</b> - The image keeps its aspect ratio, but is resized to fit within the given dimension</li>
  <li><b>cover</b> - The image keeps its aspect ratio and fills the given dimension. The image will be clipped to fit</li>
  <li><b>none</b> - The image is not resized</li>
  <li><b>scale-down</b> - the image is scaled down to the smallest version of <b>none</b> or <b>contain</b></li>
</ul>
<h1>cover</h1>
If we use <b>object-fit: cover;</b> the image keeps its aspect ratio and fills the given dimension. The image will be clipped to fit:
<br>
<img src="https://i.imgur.com/EqFCz1l.jpg">
<pre>
img {
  width: 200px;
  height: 300px;
  object-fit: cover;
}
</pre>
<h1>contain</h1>
If we use <b>object-fit: contain;</b> the image keeps its aspect ratio, but is resized to fit within the given dimension:
<br>
<img src="https://i.imgur.com/6xtYbU2.jpg">
<pre>
img {
  width: 200px;
  height: 300px;
  object-fit: contain;
}
</pre>
<h1>fill</h1>
If we use <b>object-fit: fill;</b> the image is resized to fill the given dimension. If necessary, the image will be stretched or squished to fit:
<br>
<img src="https://i.imgur.com/xEUMnxe.jpg">
<pre>
img {
  width: 200px;
  height: 300px;
  object-fit: fill;
}
</pre>
<h1>none</h1>
If we use <b>object-fit: none;</b> the image is not resized:
<br>
<img src="https://i.imgur.com/EqFCz1l.jpg">
<pre>
img {
  width: 200px;
  height: 300px;
  object-fit: none;
}
</pre>
<h1>scale-down</h1>
If we use <b>object-fit: scale-down;</b> the image is scaled down to the smallest version of none or contain:
<br>
<img src="https://i.imgur.com/6xtYbU2.jpg">
<pre>
img {
  width: 200px;
  height: 300px;
  object-fit: scale-down;
}
</pre>
<h1>Example</h1>
The following example demonstrates all the possible values of the object-fit property in one example:
<pre>
.fill{object-fit:fill;}
.contain{object-fit:contain;}
.cover{object-fit:cover;}
.scale-down{object-fit:scale-down;}
.none{object-fit:none;}
</pre>
