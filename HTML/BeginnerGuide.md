A consistent, clean, and tidy HTML code makes it easier for others to read and understand your code.
<br>
Here are some guidelines and tips for creating good HTML code.
<h1>Always Declare Document Type</h1>
Always declare the document type as the first line in your document.
<br>
The correct document type for HTML is:
<pre>&lt;!DOCTYPE html&gt;</pre>
<h1>Lowercase Elements</h1>
HTML allows mixing uppercase and lowercase letters in element names.
<br>
However, we recommend using lowercase element names, because:
<ul>
  <li>Mixing uppercase and lowercase names looks bad</li>
  <li>Developers normally use lowercase names</li>
  <li>Lowercase looks cleaner</li>
  <li>Lowercase is easier to write</li>
</ul>
<b>Good:</b>
<pre>
&lt;body&gt;
&lt;p&gt;This is a paragraph.&lt;/p&gt;
&lt;/body&gt;
</pre>
<b>Bad:</b>
<pre>
&lt;BODY&gt;
&lt;P&gt;This is a paragraph.&lt;/P&gt;
&lt;/BODY&gt;
</pre>
<h1>Lowercase Attributes</h1>
HTML allows mixing uppercase and lowercase letters in attribute names.
<br>
However, we recommend using lowercase attribute names, because:
<ul>
  <li>Mixing uppercase and lowercase names looks bad</li>
  <li>Developers normally use lowercase names</li>
  <li>Lowercase looks cleaner</li>
  <li>Lowercase is easier to write</li>
</ul>
<b>Good:</b>
<pre>&lt;a href="https://www.w3schools.com/html/"&gt;Visit my HTML tutorial&lt;/a&gt;</pre>
<b>Bad:</b>
<pre>&lt;a href="https://www.w3schools.com/html/"&gt;Visit my HTML tutorial&lt;/a&gt;</pre>
<h1>Close all elements</h1>
In HTML, you do not have to close all elements (for example the 'p' element).
<br>
However, we strongly recommend closing all HTML elements, like this:
<p></p>
<b>Good:</b>
<pre>
&lt;section&gt;
  &lt;p&gt;This is a paragraph.&lt;/p&gt;
  &lt;p&gt;This is a paragraph.&lt;/p&gt;
&lt;/section&gt;
</pre>
<b>Bad:</b>
<pre>
&lt;section&gt;
  &lt;p&gt;This is a paragraph.
  &lt;p&gt;This is a paragraph.
&lt;/section&gt;
</pre>
<h1>Always Quote Attributes</h1>
HTML allows attribute values without quotes.
<br>
However, we recommend quoting attribute values, because:
<ul>
  <li>Developers normally quote attribute values</li>
  <li>Quoted values are easier to read</li>
  <li>You MUST use quotes if the value contains spaces</li>
</ul>
<b>Good:</b>
<pre>&lt;table class="striped"&gt;</pre>
<b>Bad:</b>
<pre>&lt;table class=striped&gt;</pre>
<b>Very Bad:</b>
<pre>&lt;table class=table striped&gt;</pre>
<h1>Always Specify alt, width, and height for Images</h1>
Always specify the alt attribute for images. This attribute is important if the image for some reason cannot be displayed.
<br>
Also, always define the width and height of images. This reduces flickering, because the browser can reserve space for the image before loading.
<p></p>
<b>Good:</b>
<pre>&lt;img src="html5.gif" alt="HTML5" style="width:128px;height:128px"&gt;</pre>
<b>Bad:</b>
<pre>&lt;img src="html5.gif"&gt;</pre>
<h1>Spaces and Equals</h1>
HTML allows spaces around equal signs. But space-less is easier to read and groups entities better together.
<br>
<b>Good:</b>
<pre>&lt;link rel="stylesheet" href="styles.css"&gt;</pre>
<b>Bad:</b>
<pre>&lt;link rel = "stylesheet" href = "styles.css"&gt;</pre>
<h1>Avoid Long Code Lines</h1>
When using an HTML editor, it is NOT convenient to scroll right and left to read the HTML code.
<br>
Try to avoid too long code lines.
<h1>Never Skip &lt;title&gt; Element</h1>
The title element is required in HTML.
<br>
The contents of a page title is very important for search engine optimization (SEO)! The page title is used by search engine algorithms to decide the order when listing pages in search results.
<br>
The title element:
<ul>
  <li>Defines a title in the browser toolbar</li>
  <li>Provides a title for the page when it is added to favorites</li>
  <li>Displays a title for the page in search-engine results</li>
</ul>
So, try to make the title as accurate and meaningful as possible:
<pre>&lt;title&gt;HTML Style Guide and Coding Conventions&lt;/title&gt;</pre>
<h1>Omitting html and body Tags?</h1>
An HTML page will validate without the html and body tags:
<pre>
&lt;!DOCTYPE html&gt;
&lt;head&gt;
  &lt;title&gt;Page Title&lt;/title&gt;
&lt;/head&gt;

&lt;h1&gt;This is a heading&lt;/h1&gt;
&lt;p&gt;This is a paragraph.&lt;/p&gt;
</pre>
However, we strongly recommend to always add the html and body tags!
<br>
Omitting body can produce errors in older browsers.
<br>
Omitting html and body can also crash DOM and XML software.
<h1>Omitting head Tag?</h1>
The HTML head tag can also be omitted.
<br>
Browsers will add all elements before body, to a default head element.
<pre>
&lt;!DOCTYPE html&gt;
&lt;html&gt;
  &lt;title&gt;Page Title&lt;/title&gt;
&lt;body&gt;

&lt;h1&gt;This is a heading&lt;/h1&gt;
&lt;p&gt;This is a paragraph.&lt;/p&gt;

&lt;/body&gt;
&lt;/html&gt;
</pre>
<h1>Close Empty Elements?</h1>
In HTML, it is optional to close empty elements.
<pre>&lt;meta charset="utf-8"&gt;</pre>
<pre>&lt;meta charset="utf-8" /&gt;</pre>
If you expect XML/XHTML software to access your page, keep the closing slash ( /), because it is required in XML and XHTML.
<h1>The lang Attribute</h1>
You should always include the lang attribute inside the &lt;html&gt; tag, to declare the language of the Web page. This is meant to assist search engines and browsers.
<pre>&lt;html lang="en"&gt;</pre>
<pre>&lt;html lang="en-us"&gt;</pre>
<h1>Meta Data</h1>
To ensure proper interpretation and correct search engine indexing, both the language and the character encoding &lt;meta charset="<i>charset</i>"&gt; should be defined as early as possible in an HTML document:
<pre>&lt;meta charset="UTF-8"&gt;</pre>
<h1>Viewport</h1>
<a href="Responsive.md#Viewport">Click Here</a> to know more about Viewport.
<h1>Comments</h1>
<a href="Comments.md">Click Here</a> to know more about Comments.
<h1>StyleSheets</h1>
Short CSS rules can be written compressed, like this:
<pre>p.intro{font-family:Verdana;font-size:16em;}</pre>
Long CSS rules should be written over multiple lines:
<pre>
body {
  background-color: lightgrey;
  font-family: "Arial Black", Helvetica, sans-serif;
  font-size: 16em;
  color: black;
}
</pre>
<h1>Use Lowercase File Names</h1>
Some web servers (Apache, Unix) are case sensitive about file names: "london.jpg" cannot be accessed as "London.jpg".
<br>
Other web servers (Microsoft, IIS) are not case sensitive: "london.jpg" can be accessed as "London.jpg".
<br>
If you use a mix of uppercase and lowercase, you have to be aware of this.
<br>
If you move from a case-insensitive to a case-sensitive server, even small errors will break your web!
<br>
To avoid these problems, always use lowercase file names!
<h1>File Extensions</h1>
HTML files should have a .html extension (.htm is allowed).
<br>
CSS files should have a .css extension.
<br>
JavaScript files should have a .js extension.
<h1>What is the Difference Between HTML and HTM?</h1>
There is no difference between the .htm and .html file extensions!
<br>
Both will be treated as HTML by any web browser and web server.
<h1>Default Filename</h1>
When a URL does not specify a filename at the end (like "//preview.bledygamesweb.repl.co/"), the server just adds a default filename, such as "index.html", "index.htm", "default.html", or "default.htm".
<br>
If your server is configured only with "index.html" as the default filename, your file must be named "index.html", and not "default.html".
<br>
However, servers can be configured with more than one default filename; usually you can set up as many default filenames as you want.
