<a href="/HTML/Links/Bookmarks.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/HTML/Images/Maps.md">Next &gt;</a>
<hr>
Images can improve the design and the appearance of a web page.
<br>
<img src="https://i.imgur.com/Dye2ssc.jpg" height="250px">
<img src="https://i.imgur.com/rUdy1Or.jpg" height="250px">
<img src="https://i.imgur.com/O9ioBM7.jpg" height="250px">
<h1>Syntax</h1>
The HTML <b>&lt;img&gt;</b> tag is used to embed an image in a web page.
<br>
Images are not technically inserted into a web page; images are linked to web pages. The <b>&lt;img&gt;</b> tag creates a holding space for the referenced image.
<br>
The <b>&lt;img&gt;</b> tag is empty, it contains attributes only, and does not have a closing tag.
<br>
The <b>&lt;img&gt;</b> tag has two required attributes:
<ul>
  <li>src - Specifies the path to the image</li>
  <li>alt - Specifies an alternate text for the image</li>
</ul>
<pre>&lt;img src="url" alt="alternatetext"&gt;</pre>
<h1>src</h1>
The required <b>src</b> attribute specifies the path (URL) to the image.
<p></p>
<b>Note:</b> When a web page loads, it is the browser, at that moment, that gets the image from a web server and inserts it into the page. Therefore, make sure that the image actually stays in the same spot in relation to the web page, otherwise your visitors will get a broken link icon. The broken link icon and the alt text are shown if the browser cannot find the image.
<pre>&lt;img src="//i.imgur.com/O9ioBM7.jpg" alt="Flowers in Chania"&gt;</pre>
<h1>alt</h1>
The required alt attribute provides an alternate text for an image, if the user for some reason cannot view it (because of slow connection, an error in the src attribute, or if the user uses a screen reader).
<br>
The value of the alt attribute should describe the image:
<pre>&lt;img src="//i.imgur.com/O9ioBM7.jpg" alt="Flowers in Chania"&gt;</pre>
If a browser cannot find an image, it will display the value of the alt attribute:
<img src="wrongname.gif" alt="Flowers in Chania">
<pre>&lt;img src="wrongname.gif" alt="Flowers in Chania"&gt;</pre>
<h1>Size</h1>
You can use the <b>style</b> attribute to specify the <b>width</b> and <b>height</b> of an image.
<pre>&lt;img src="img_girl.jpg" alt="Girl in a jacket" style="width:500px;height:600px;"&gt;</pre>
Alternatively, you can use the <b>width</b> and <b>height</b> attributes:
<pre>&lt;img src="img_girl.jpg" alt="Girl in a jacket" width="500" height="600"&gt;</pre>
The width and height attributes always define the <b>width</b> and <b>height</b> of the image in pixels.
<p></p>
<b>Note:</b> Always specify the <b>width</b> and <b>height</b> of an image. If width and height are not specified, the web page might flicker while the image loads.
<h1>Width & Height</h1>
The <b>width</b> and <b>height</b> attributes are valid in HTML.
<br>
However, I suggest using the <b>style</b> attribute. It prevents styles sheets from changing the size of images:
<pre>
&lt;style&gt;
img {
  width: 100%;
}
&lt;/style&gt;
</pre>
<h1>Images on another folder</h1>
If you have your images in a sub-folder, you must include the folder name in the src attribute:
<pre>&lt;img src="/images/GifImageWhatever.gif" alt="HTML5 Icon" style="width:128px;height:128px;"&gt;</pre>
<h1>Images on another server</h1>
Some web sites point to an image on another server.
<br>
To point to an image on another server, you must specify an absolute (full) URL in the src attribute:
<pre>&lt;img src="//html-calculator.bledygames.repl.co/favicon.png" alt="BGP100's Profile Photo"&gt;</pre>
<b>Notes on external images:</b> External images might be under copyright. If you do not get permission to use it, you may be in violation of copyright laws. In addition, you cannot control external images; it can suddenly be removed or changed.
<h1>GIFs</h1>
HTML allows animated Images:
<pre>&lt;img src="//i.imgur.com/gJInvyH.gif" alt="Computer Man" style="width:48px;height:48px;"&gt;</pre>
<h1>Image as Link</h1>
To use an image as a link, put the <b>&lt;img&gt;</b> tag inside the <b>&lt;a&gt;</b> tag:
<pre>
&lt;a href="//github.com/BGP100/HTML-Guide/"&gt;
  &lt;img src="//i.imgur.com/ixnaQfO.gif" alt="HTML tutorial" style="width:42px;height:42px;"&gt;&lt;/a&gt;
</pre>
<h1>Floating Images</h1>
Use the CSS <b>float</b> property to let the image float to the right or to the left of a text:
<pre>
&lt;p&gt;&lt;img src="smiley.gif" alt="Smiley face" style="float:right;width:42px;height:42px;"&gt;
The image will float to the right of the text.&lt;/p&gt;
<p></p>
&lt;p&gt;&lt;img src="smiley.gif" alt="Smiley face" style="float:left;width:42px;height:42px;"&gt;
The image will float to the left of the text.&lt;/p&gt;
</pre>
<h1>Formats</h1>
<table class="ws-table-all notranslate">
  <tr>
    <th>Abbreviation</th>
    <th>File Format</th>
    <th>File Extension</th>
  </tr>
  <tr>
    <td>APNG</td>
    <td>Animated Portable Network Graphics</td>
    <td>.apng</td>
  </tr>
  <tr>
    <td>GIF</td>
    <td>Graphics Interchange Format</td>
    <td>.gif</td>
  </tr>
  <tr>
    <td>ICO</td>
    <td>Microsoft Icon</td>
    <td>.ico, .cur </td>
  </tr>
  <tr>
    <td>JPEG</td>
    <td>Joint Photographic Expert Group image</td>
    <td>.jpg, .jpeg, .jfif, .pjpeg, .pjp</td>
  </tr>
  <tr>
    <td>PNG</td>
    <td>Portable Network Graphics</td>
    <td>.png</td>
  </tr>
  <tr>
    <td>SVG</td>
    <td>Scalable Vector Graphics</td>
    <td>.svg</td>
  </tr>
</table>
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
