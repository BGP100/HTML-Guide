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
<pre>
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
<b>To be continued. . .</b>
