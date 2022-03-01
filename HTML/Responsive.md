Responsive web design is about creating web pages that look good on all devices!
<br>
A responsive web design will automatically adjust for different screen sizes and viewports.
<hr>
Responsive Web Design is about using HTML and CSS to automatically resize, hide, shrink, or enlarge, a website, to make it look good on all devices (desktops, tablets, and phones):
<br>
<img src="https://i.imgur.com/3IpXKcc.jpg">
<h1>Viewport</h1>
To create a responsive website, add the following <b>&lt;meta&gt;</b> tag to all your web pages:
<pre>&lt;meta name="viewport" content="width=device-width, initial-scale=1.0"&gt;</pre>
This will set the viewport of your page, which will give the browser instructions on how to control the page's dimensions and scaling.
<br>
Here is an example of a web page without the viewport meta tag, and the same web page with the viewport meta tag:
<p></p>
<b>Without viewport:</b>
<img src="https://i.imgur.com/a3YL2Oy.png">
<p></p>
<b>With viewport:</b>
<img src="https://i.imgur.com/kpxDfHy.png">
<h1>Images</h1>
Responsive images are images that scale nicely to fit any browser size.
<h2>width</h2>
If the CSS <b>width</b> property is set to 100%, the image will be responsive and scale up and down:
<br>
<img src="https://i.imgur.com/EZqJ6si.jpg" width="100%">
<pre>&lt;img src="img_girl.jpg" style="width:100%;"&gt;</pre>
Notice that in the example above, the image can be scaled up to be larger than its original size. A better solution, in many cases, will be to use the max-width property instead.
<h2>max-width</h2>
If the max-width property is set to 100%, the image will scale down if it has to, but never scale up to be larger than its original size:
<br>
<img src="https://i.imgur.com/EZqJ6si.jpg">
<pre>&lt;img src="img_girl.jpg" style="max-width:100%;height:auto;"&gt;</pre>
<h2>Different Sizes Between Browsers</h2>
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
<h1>Text Size</h1>
The text size can be set with a "vw" unit, which means the "viewport width".
<br>
That way the text size will follow the size of the browser window:
<br>
<img src="https://i.imgur.com/qXBUj73.jpg">
<pre>&lt;h1 style="font-size:10vw"&gt;Hello World&lt;/h1&gt;</pre>
<h1>Media Queries</h1>
In addition to resize text and images, it is also common to use media queries in responsive web pages.
<br>
With media queries you can define completely different styles for different browser sizes.
<br>
Example: resize the browser window to see that the three div elements below will display horizontally on large screens and stacked vertically on small screens:
<br>
<img src="https://i.imgur.com/66b4n6h.jpg">
<pre>
.left, .right {
  float: left;
  width: 20%; /* The width is 20%, by default */
}
.main {
  float: left;
  width: 60%; /* The width is 60%, by default */
}
/* Use a media query to add a breakpoint at 800px: */
@media screen and (max-width: 800px) {
  .left, .main, .right {
    width: 100%;
  }
}
</pre>
<h1>Full Web Example</h1>
A responsive web page should look good on large desktop screens and on small mobile phones.
<br>
<img src="https://i.imgur.com/g4O7vWi.jpg">
<h1>Frameworks</h1>
All popular CSS Frameworks offer responsive design.
<br>
They are free, and easy to use.
<h1>W3.CSS</h1>
W3.CSS is a modern CSS framework with support for desktop, tablet, and mobile design by default.
<br>
W3.CSS is smaller and faster than similar CSS frameworks.
<br>
W3.CSS is designed to be a high quality alternative to Bootstrap.
<br>
W3.CSS is designed to be independent of jQuery or any other JavaScript library.
<img src="https://i.imgur.com/FHOBRLe.jpg">
<pre>
&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;meta name="viewport" content="width=device-width, initial-scale=1"&gt;
&lt;link rel="stylesheet" href="https://raw.githubusercontent.com/BGP100/HTML-Guide/main/Extras/W3-CSS"&gt;
&lt;body&gt;
&lt;div class="w3-container w3-green"&gt;
  &lt;h1&gt;W3Schools Demo&lt;/h1&gt;
  &lt;p&gt;Resize this responsive page!&lt;/p&gt;
&lt;/div&gt;
&lt;div class="w3-row-padding"&gt;
  &lt;div class="w3-third"&gt;
    &lt;h2&gt;London&lt;/h2&gt;
    &lt;p&gt;London is the capital city of England.&lt;/p&gt;
    &lt;p&gt;It is the most populous city in the United Kingdom, with a metropolitan area of over 13 million inhabitants.&lt;/p&gt;
  &lt;/div&gt;
  &lt;div class="w3-third"&gt;
    &lt;h2&gt;Paris&lt;/h2&gt;
    &lt;p&gt;Paris is the capital of France.&lt;/p&gt;
    &lt;p>The Paris area is one of the largest population centers in Europe, with more than 12 million inhabitants.&lt;/p&gt;
  &lt;/div&gt;
  &lt;div class="w3-third"&gt;
    &lt;h2&gt;Tokyo&lt;/h2&gt;
    &lt;p&gt;Tokyo is the capital of Japan.&lt;/p&gt;
    &lt;p&gt;It is the center of the Greater Tokyo Area, and the most populous metropolitan area in the world.&lt;/p&gt;
  &lt;/div&gt;
&lt;/div&gt;
&lt;/body&gt;
&lt;/html&gt;
</pre>
<h1>BootStrap</h1>
Another popular CSS framework is Bootstrap. Bootstrap uses HTML, CSS and jQuery to make responsive web pages.
