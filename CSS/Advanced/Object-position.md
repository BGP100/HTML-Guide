<a href="/CSS/Advanced/Object-fit.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/Advanced/Masking.md">Next &gt;</a>
<hr>
The CSS object-position property is used to specify how an <b>&lt;img&gt;</b> or <b>&lt;video&gt;</b> should be positioned within its container.
<hr>
Look at the following image from Paris, which is 400x300 pixels:
<br>
<img src="https://i.imgur.com/YHAVU6Z.jpg">
<br>
Next, we use object-fit: cover; to keep the aspect ratio and to fill the given dimension. However, the image will be clipped to fit, like this:
<br>
<img src="https://i.imgur.com/EqFCz1l.jpg">
<pre>
img {
  width: 200px;
  height: 300px;
  object-fit: cover;
}
</pre>
<h1>Using the Property</h1>
Let's say that the part of the image that is shown, is not positioned as we want. To position the image, we will use the object-position property.
<br>
Here we will use the object-position property to position the image so that the great old building is in center:
<br>
<img src="https://i.imgur.com/k8Wvvoj.jpg" width="24%">
<pre>
img {
  width: 200px;
  height: 300px;
  object-fit: cover;
  object-position: 80% 100%;
}
</pre>
Here we will use the object-position property to position the image so that the famous Eiffel Tower is in center:
<br>
<img src="https://i.imgur.com/EqFCz1l.jpg">
<pre>
img {
  width: 200px;
  height: 300px;
  object-fit: cover;
  object-position: 15% 100%;
}
</pre>
