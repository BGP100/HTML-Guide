An HTML iframe is used to display a web page within a web page.
<br>
<a href="https://github.com/BGP100/"><img src="https://i.imgur.com/MawZxP8.png" width="100%" height="auto"></a>
<h1>Syntax</h1>
The HTML <b>&lt;iframe&gt;</b> tag specifies an inline frame.
<br>
An inline frame is used to embed another document within the current HTML document.
<pre>&lt;iframe src="<em>url</em>" title="<em>description</em>"&gt;&lt;/iframe&gt;</pre>
<b>Tip:</b> It is a good practice to always include a title attribute for the &lt;iframe&gt;. This is used by screen readers to read out what the content of the iframe is.
<h1>Width & Height</h1>
Use the width and height attributes to specify the size of the iframe.
<br>
The width and height are specified in pixels by default:
<pre>&lt;iframe src="demo_iframe.html" width="300" height="200" title="Iframe Example"&gt;&lt;/iframe&gt;</pre>
Or you can add the style attribute and use the CSS width and height properties:
<pre>&lt;iframe src="demo_iframe.html" style="width:300px;height:200px;" title="Iframe Example"&gt;&lt;/iframe&gt;</pre>
<h1>Remove Border</h1>
By default, an iframe has a border around it.
<br>
To remove the border, add the style attribute and use the CSS border property:
<pre>&lt;iframe src="demo_iframe.html" style="border:none;width:300px;height:200px;" title="Iframe Example"&gt;&lt;/iframe&gt;</pre>
With CSS, you can also change the size, style and color of the iframe's border:
<pre>&lt;iframe src="demo_iframe.html" style="border:2px solid red;width:300px;height:200px;" title="Iframe Example"&gt;&lt;/iframe&gt;</pre>
<h1>Target Link</h1>
An iframe can be used as the target frame for a link.
<br>
The <b>target</b> attribute of the link must refer to the <b>name</b> attribute of the iframe:
<pre>
&lt;iframe src="demo_iframe.html" name="iframe_a" title="Iframe Example"&gt;&lt;/iframe&gt;
<p></p>
&lt;p&gt;&lt;a href="https://github.com/BGP100/" target="iframe_a"&gt;Profile&lt;/a&gt;&lt;/p&gt;
</pre>
