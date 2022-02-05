A background image can be specified for almost any HTML element.
<br>
To add a background image on an HTML element, use the HTML style attribute and the CSS background-image property:
<pre>&lt;div style="background-image: url('img_girl.jpg');"&gt;</pre>
You can also specify the background image in the <b>&lt;style&gt;</b> element, in the <b>&lt;head&gt;</b> section:
<pre>
&lt;style&gt;
div {
  background-image: url('img_girl.jpg');
}
&lt;/style&gt;
</pre>
<h1>Background image on a page</h1>
If you want the entire page to have a background image, you must specify the background image on the <b>&lt;body&gt;</b> element:
<img src="https://images.alalgi.repl.co/769.png">
<pre>
&lt;style&gt;
body {
  background-image: url('img_girl.jpg');
}
&lt;/style&gt;
</pre>
To avoid the background image from repeating itself, set the background-repeat property to no-repeat.
<pre>
&lt;style&gt;
body {
  background-image: url('example_img_girl.jpg');
  background-repeat: no-repeat;
}
&lt;/style&gt;
</pre>
<h1>Cover</h1>
If you want the background image to cover the entire element, you can set the background-size property to cover.
<br>
Also, to make sure the entire element is always covered, set the background-attachment property to fixed:
<br>
This way, the background image will cover the entire element, with no stretching (the image will keep its original proportions):
<pre>
&lt;style&gt;
body {
  background-image: url('img_girl.jpg');
  background-repeat: no-repeat;
  background-attachment: fixed;
  background-size: cover;
}
&lt;/style&gt;
</pre>
<h1>Stretch</h1>
If you want the background image to stretch to fit the entire element, you can set the background-size property to 100% 100%:
<img src="https://www.w3schools.com/html/img_girl.jpg" width="100%" height="300px">
<pre>
&lt;style&gt;
body {
  background-image: url('img_girl.jpg');
  background-repeat: no-repeat;
  background-attachment: fixed;
  background-size: 100% 100%;
}
&lt;/style&gt;
</pre>
