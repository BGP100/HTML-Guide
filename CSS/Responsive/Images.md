<a href="/CSS/Responsive/MediaQueries.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/Responsive/Videos.md">Next &gt;</a>
<hr>
<h1>width</h1>
If the <b>width</b> property is set to a percentage and the <b>height</b> property is set to "auto", the image will be responsive and scale up and down:
<pre>
img {
  width: 100%;
  height: auto;
}
</pre>
Notice that in the example above, the image can be scaled up to be larger than its original size. A better solution, in many cases, will be to use the <b>max-width</b> property instead.
<h1>max-width</h1>
If the <b>max-width</b> property is set to 100%, the image will scale down if it has to, but never scale up to be larger than its original size:
<pre>
img {
  max-width: 100%;
  height: auto;
}
</pre>
<h1>Background Images</h1>
Background images can also respond to resizing and scaling.
<br>
Here we will show three different methods:
<br>
1. If the <b>background-size</b> property is set to "contain", the background image will scale, and try to fit the content area. However, the image will keep its aspect ratio (the proportional relationship between the image's width and height):
<br>
<img src="https://i.imgur.com/n9z38iz.png" width="100%">
<br>
Here is the CSS code:
<pre>
div {
  width: 100%;
  height: 400px;
  background-image: url('//i.imgur.com/m0caW4s.jpg');
  background-repeat: no-repeat;
  background-size: contain;
  border: 1px solid red;
}
</pre>
2. If the <b>background-size</b> property is set to "100% 100%", the background image will stretch to cover the entire content area:
<br>
<img src="https://i.imgur.com/TEKx9rX.png" width="100%">
<br>
Here is the CSS code:
<pre>
div {
  width: 100%;
  height: 400px;
  background-image: url('img_flowers.jpg');
  background-size: 100% 100%;
  border: 1px solid red;
}
</pre>
3. If the <b>background-size</b> property is set to "cover", the background image will scale to cover the entire content area. Notice that the "cover" value keeps the aspect ratio, and some part of the background image may be clipped:
<br>
<img src="https://i.imgur.com/y7MeIYF.png" width="100%">
<br>
Here is the CSS code:
<pre>
div {
  width: 100%;
  height: 400px;
  background-image: url('img_flowers.jpg');
  background-size: cover;
  border: 1px solid red;
}
</pre>
<h1>Different Sizes Between Browsers</h1>
A large image can be perfect on a big computer screen, but useless on a small device. Why load a large image when you have to scale it down anyway? To reduce the load, or for any other reasons, you can use media queries to display different images on different devices.
<pre>
/* For width smaller than 400px: */
body {
  background-image: url('img_smallflower.jpg');
}
/* For width 400px and larger: */
@media only screen and (min-width: 400px) {
  body {
    background-image: url('img_flowers.jpg');
  }
}
</pre>
You can use the media query <b>min-device-width</b>, instead of <b>min-width</b>, which checks the device width, instead of the browser width. Then the image will not change when you resize the browser window:
<pre>
/* For devices smaller than 400px: */
body {
  background-image: url('img_smallflower.jpg');
}
/* For devices 400px and larger: */
@media only screen and (min-device-width: 400px) {
  body {
    background-image: url('img_flowers.jpg');
  }
}
</pre>
<h1>Using the &lt;picture&gt; Element</h1>
The HTML <b>&lt;picture&gt;</b> element allows you to define different images for different browser window sizes.
<br>
Resize the browser window to see how the image below change depending on the width:
<br>
<img src="https://i.imgur.com/m0caW4s.jpg">
<pre>
&lt;picture&gt;
  &lt;source srcset="img_smallflower.jpg" media="(max-width: 600px)"&gt;
  &lt;source srcset="img_flowers.jpg" media="(max-width: 1500px)"&gt;
  &lt;source srcset="flowers.jpg"&gt;
  &lt;img src="img_smallflower.jpg" alt="Flowers"&gt;
&lt;/picture&gt;
</pre>
