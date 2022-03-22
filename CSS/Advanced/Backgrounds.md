In this chapter you will learn how to add multiple background images to one element.
<br>
You will also learn about the following properties:
<ul>
  <li><b>background-size</b></li>
  <li><b>background-origin</b></li>
  <li><b>background-clip</b></li>
</ul>
CSS allows you to add multiple background images for an element, through the <b>background-image</b> property.
<br>
The different background images are separated by commas, and the images are stacked on top of each other, where the first image is closest to the viewer.
<br>
The following example has two background images, the first image is a flower (aligned to the bottom and right) and the second image is a paper background (aligned to the top-left corner):
<pre>
#example1 {
  background-image: url(//i.imgur.com/9yp0jIC.webp), url(//i.imgur.com/RaRUUk.webp);
  background-position: right bottom, left top;
  background-repeat: no-repeat, repeat;
}
</pre>
Multiple background images can be specified using either the individual background properties (as above) or the <b>background</b> shorthand property.
<br>
The following example uses the <b>background</b> shorthand property (same result as example above):
<pre>
#example1 {
  background: url(//i.imgur.com/9yp0jIC.webp) right bottom no-repeat, url(//i.imgur.com/RaRUUk.webp) left top repeat;
</pre>
<h1>Background Size</h1>
The CSS background-size property allows you to specify the size of background images.
<br>
The size can be specified in lengths, percentages, or by using one of the two keywords: contain or cover.
<br>
The following example resizes a background image to much smaller than the original image (using pixels):
<br>
<img src="https://i.imgur.com/LdM1b6F.jpg" width="100%">
Here is the code:
<pre>
#div1 {
  background: url(//i.imgur.com/9yp0jIC.webp);
  background-size: 100px 80px;
  background-repeat: no-repeat;
}
</pre>
The two other possible values for <b>background-size</b> are <b>contain</b> and <b>cover</b>.
<br>
The <b>contain</b> keyword scales the background image to be as large as possible (but both its width and its height must fit inside the content area). As such, depending on the proportions of the background image and the background positioning area, there may be some areas of the background which are not covered by the background image.
<br>
The <b>cover</b> keyword scales the background image so that the content area is completely covered by the background image (both its width and height are equal to or exceed the content area). As such, some parts of the background image may not be visible in the background positioning area.
<br>
The following example illustrates the use of <b>contain</b> and <b>cover</b>:
<pre>
#div1 {
  background: url(//i.imgur.com/9yp0jIC.webp);
  background-size: contain;
  background-repeat: no-repeat;
}
#div2 {
  background: url(//i.imgur.com/9yp0jIC.webp);
  background-size: cover;
  background-repeat: no-repeat;
}
</pre>
<h1>Multiple Sizes</h1>
The <b>background-size</b> property also accepts multiple values for background size (using a comma-separated list), when working with multiple backgrounds.
<br>
The following example has three background images specified, with different background-size value for each image:
<pre>
#example1 {
  background: url(//i.imgur.com/VcWkMKH.webp) left top no-repeat, url(//i.imgur.com/9yp0jIC.webp) right bottom no-repeat, url(//i.imgur.com/RaRUUk.webp) left top repeat;
  background-size: 50px, 130px, auto;
}
</pre>
<h1>Full Size Background</h1>
Now we want to have a background image on a website that covers the entire browser window at all times.
<br>
The requirements are as follows:
<ul>
  <li><b>Fill the entire page with the image (no white space)</b></li>
  <li><b>Scale image as needed</b></li>
  <li><b>Center image on page</b></li>
  <li><b>Do not cause scrollbars</b></li>
</ul>
The following example shows how to do it; Use the <b>&lt;html&gt;</b> element (the <b>&lt;html&gt;</b> element is always at least the height of the browser window). Then set a fixed and centered background on it. Then adjust its size with the background-size property:
<pre>
html {
  background: url(//i.imgur.com/tkgGGdT.webp) no-repeat center fixed;
  background-size: cover;
}
</pre>
<h1>Hero Image</h1>
You could also use different background properties on a <b>&lt;div&gt;</b> to create a hero image (a large image with text), and place it where you want.
<pre>
.hero-image {
  background: url(//i.imgur.com/tkgGGdT.webp) no-repeat center;
  background-size: cover;
  height: 500px;
  position: relative;
}
</pre>
<h1>background-origin</h1>
The CSS <b>background-origin</b> property specifies where the background image is positioned.
<br>
The property takes three different values:
<ul>
  <li><b>border-box</b> - the background image starts from the upper left corner of the border.</li>
  <li><b>padding-box</b> - (default) the background image starts from the upper left corner of the padding edge.</li>
  <li><b>content-box</b> - the background image starts from the upper left corner of the content.</li>
</ul>
The following example illustrates the <b>background-origin</b> property:
<pre>
#example1 {
  border: 10px solid black;
  padding: 35px;
  background: url(//i.imgur.com/9yp0jIC.webp);
  background-repeat: no-repeat;
  background-origin: content-box;
}
</pre>
<h1>background-clip</h1>
The CSS <b>background-clip</b> property specifies the painting area of the background.
<br>
The property takes three different values:
<ul>
border-box - (default) the background is painted to the outside edge of the border
padding-box - the background is painted to the outside edge of the padding
content-box - the background is painted within the content box
</ul>
The following example illustrates the <b>background-clip</b> property:
<pre>
#example1 {
  border: 10px dotted black;
  padding: 35px;
  background: yellow;
  background-clip: content-box;
}
</pre>
