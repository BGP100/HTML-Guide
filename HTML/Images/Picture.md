<a href="/HTML/Images/Background.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/HTML/Favicon.md">Next &gt;</a>
<hr>
The HTML &lt;picture&gt; element allows you to display different pictures for different devices or screen sizes.
<br>
<img src="https://www.w3schools.com/html/picture_example.jpg">
<br>
The HTML <b>&lt;picture&gt;</b> element gives web developers more flexibility in specifying image resources.
<br>
The <b>&lt;picture&gt;</b> element contains one or more <b>&lt;source&gt;</b> elements, each referring to different images through the srcset attribute. This way the browser can choose the image that best fits the current view and/or device.
<br>
Each <b>&lt;source&gt;</b> element has a media attribute that defines when the image is the most suitable.
<pre>
&lt;picture&gt;
  &lt;source media="(min-width: 650px)" srcset="img_food.jpg"&gt;
  &lt;source media="(min-width: 465px)" srcset="img_car.jpg"&gt;
  &lt;img src="img_girl.jpg"&gt;
&lt;/picture&gt;
</pre>
<b>Note:</b> Always specify an img element as the last child element of the picture element. The img element is used by browsers that do not support the picture element, or if none of the source tags match.
<h1>When to use it?</h1>
There are two main purposes for the <b>&lt;picture</b>&gt; element:
<p></p>
<b>1. Bandwidth</b>
If you have a small screen or device, it is not necessary to load a large image file. The browser will use the first source element with matching attribute values, and ignore any of the following elements.
<p></p>
<b>2. Format Support</b>
Some browsers or devices may not support all image formats. By using the picture element, you can add images of all formats, and the browser will use the first format it recognizes, and ignore any of the following elements.
<pre>
&lt;picture&gt;
  &lt;source srcset="img_avatar.png"&gt;
  &lt;source srcset="img_girl.jpg"&gt;
  &lt;img src="img_beatles.gif" alt="Beatles" style="width:auto;"&gt;
&lt;/picture&gt;
</pre>
<h1>Tags</h1>
<table class="ws-table-all notranslate">
  <tr>
    <th>Tag</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>&lt;img&gt;</td>
    <td>Defines an image</td>
  </tr>
  <tr>
    <td>&lt;map&gt;</td>
    <td>Defines an image map</td>
  </tr>
  <tr>
    <td>&lt;area&gt;</td>
    <td>Defines a clickable area inside an image map</td>
  </tr>
  <tr>
    <td>&lt;picture&gt;</td>
    <td>Defines a container for multiple image resources</td>
  </tr>
</table>
