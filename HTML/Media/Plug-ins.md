Plug-ins are computer programs that extend the standard functionality of the browser.
<hr>
Plug-ins were designed to be used for many different purposes:
<ul>
  <li>To run Java applets.</li>
  <li>To run Microsoft ActiveX controls.</li>
  <li>To display Flash movies.</li>
  <li>To display maps.</li>
  <li>To scan for viruses.</li>
  <li>To verify a bank id.</li>
</ul>
<b>WARNING!!!</b>
<br>
Most browsers no longer support Java Applets and Plug-ins.
<br>
ActiveX controls are no longer supported in any browsers.
<br>
The support for Shockwave Flash has also been turned off in modern browsers.
<h1>The &lt;object&gt; Element</h1>
The <b>&lt;object&gt;</b> element is supported by all browsers.
<br>
The <b>&lt;object&gt;</b> element defines an embedded object within an HTML document.
<br>
It was designed to embed plug-ins (like Java applets, PDF readers, and Flash Players) in web pages, but can also be used to include HTML in HTML:
<pre>&lt;object width="100%" height="500px" data="snippet.html"&gt;&lt;/object&gt;</pre>
Or images if you like:
<pre>&lt;object data="audi.jpeg"&gt;&lt;/object&gt;</pre>
<h1>The &lt;embed&gt; Element</h1>
The <b>&lt;embed&gt;</b> element is supported in all major browsers.
<br>
The <b>&lt;embed&gt;</b> element also defines an embedded object within an HTML document.
<br>
Web browsers have supported the <b>&lt;embed&gt;</b> element for a long time. However, it has not been a part of the HTML specification before HTML5.
<pre>&lt;embed src="audi.jpeg"&gt;</pre>
The <b>&lt;embed&gt;</b> element can also be used to include HTML in HTML:
<pre>&lt;embed width="100%" height="500px" src="snippet.html"&gt;</pre>
