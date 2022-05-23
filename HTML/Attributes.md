<a href="/HTML/Elements.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/HTML/Heading.md">Next &gt;</a>
<hr>
<ul>
  <li>All HTML elements can have attributes</li>
  <li>Attributes provide additional information about elements</li>
  <li>Attributes are always specified in the start tag</li>
  <li>Attributes usually come in name/value pairs like: name="value"</li>
</ul>
<h1>href</h1>
The <a> tag defines a hyperlink. The href attribute specifies the URL of the page the link goes to:
<pre>&lt;a href="//github.com/BGP100/HTML-Guide"&gt;Visit the HTML Guide&lt;/a&gt;</pre>
<h1>src</h1>
The &lt;img&gt; tag is used to embed an image in an HTML page. The src attribute specifies the path to the image to be displayed:
<pre>&lt;img src="//preview.bledygamesweb.repl.co/favicon.png"&gt;</pre>
There are two ways to specify the URL in the src attribute:
<br>
<b>1.</b> Absolute URL - Links to an external image that is hosted on another website. Example: src="//preview.bledygamesweb.repl.co/favicon.png".
<br>
Note: External images might be under copyright. If you do not get permission to use it, you may be in violation of copyright laws. In addition, you cannot control external images; it can suddenly be removed or changed.
<br>
<b>2.</b> Relative URL - Links to an image that is hosted within the website. Here, the URL does not include the domain name. If the URL begins without a slash, it will be relative to the current page. Example: src="/favicon.png". If the URL begins with a slash, it will be relative to the domain. Example: src="/favicon.png".
<br>
Tip: It is almost always best to use relative URLs. They will not break if you change domain.
<h1>width &amp; height</h1>
The &lt;img&gt; tag should also contain the width and height attributes, which specifies the width and height of the image (in pixels):
<pre>&lt;img src="//preview.bledygamesweb.repl.co/favicon.png" width="500" height="600"&gt;</pre>
<h1>alt</h1>
The required alt attribute for the &lt;img&gt; tag specifies an alternate text for an image, if the image for some reason cannot be displayed. This can be due to slow connection, or an error in the src attribute, or if the user uses a screen reader.
<pre>&lt;img src="//preview.bledygamesweb.repl.co/favicon.png" alt="BGP100 Image"&gt;</pre>
<h1>title</h1>
The title attribute defines some extra information about an element.
<br>
The value of the title attribute will be displayed as a tooltip when you mouse over the element:
<pre>&lt;p title="I'm a tooltip"&gt;This is a paragraph.&lt;/p&gt;</pre>
