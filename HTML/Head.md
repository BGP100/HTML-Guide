<a href="/HTML/FilePaths.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/HTML/Layout.md">Next &gt;</a>
<hr>
The HTML <b>&lt;head&gt;</b> element is a container for the following elements: <b>&lt;title&gt;</b>, <b>&lt;style&gt;</b>, <b>&lt;meta&gt;</b>, <b>&lt;link&gt;</b>, <b>&lt;script&gt;</b>, and <b>&lt;base&gt;</b>.
<br>
The <b>&lt;head&gt;</b> element is a container for metadata (data about data) and is placed between the <html> tag and the <body> tag.
<br>
HTML metadata is data about the HTML document. Metadata is not displayed.
<br>
Metadata typically define the document title, character set, styles, scripts, and other meta information.
<h1>title</h1>
The title element defines the title of the document. The title must be text-only, and it is shown in the browser's title bar or in the page's tab.
<br>
The title element is required in HTML documents!
<br>
The contents of a page title is very important for search engine optimization (SEO)! The page title is used by search engine algorithms to decide the order when listing pages in search results.
<br>
The title element:
<ul>
  <li>Defines a title in the browser toolbar.</li>
  <li>Provides a title for the page when it is added to favorites.</li>
  <li>Displays a title for the page in search engine-results.</li>
</ul>
So, try to make the title as accurate and meaningful as possible!
<br>
A simple HTML document:
<pre>
&lt;head&gt;
  &lt;title&gt;A Meaningful Page Title&lt;/title&gt;
&lt;/head&gt;
</pre>
<h1>style</h1>
The style element is used to define style information for a single HTML page:
<pre>
&lt;head&gt;
  &lt;style&gt;
    body {background-color: powderblue;}
    h1 {color: red;}
    p {color: blue;}
  &lt;/style&gt;
&lt;/head&gt;
</pre>
<h1>link</h1>
The link element defines the relationship between the current document and an external resource.
<br>
The link tag is most often used to link to external style sheets:
<pre>
&lt;head&gt;
  &lt;style&gt;
    &lt;link rel="stylesheet" href="mystyle.css"&gt;
  &lt;/style&gt;
&lt;/head&gt;
</pre>
<h1>meta</h1>
The meta element is typically used to specify the character set, page description, keywords, author of the document, and viewport settings.
<br>
The metadata will not be displayed on the page, but are used by browsers (how to display content or reload page), by search engines (keywords), and other web services.
<h3>Examples</h3>
<b>Define the character set used:</b>
<pre>
&lt;meta charset="UTF-8"&gt;
</pre>
<b>Define keywords for search engines:</b>
<pre>
&lt;meta name="keywords" content="HTML, CSS, JavaScript"&gt;
</pre>
<b>Define a description of your web page:</b>
<pre>
&lt;meta name="description" content="Free Web tutorials"&gt;
</pre>
<b>Define the author of a page:</b>
<pre>
&lt;meta name="author" content="John Doe"&gt;
</pre>
<b>Refresh document every 30 seconds:</b>
<pre>
&lt;meta http-equiv="refresh" content="30"&gt;
</pre>
<b>Setting the viewport to make your website look good on all devices:</b>
<pre>
&lt;meta name="viewport" content="width=device-width, initial-scale=1.0"&gt;
</pre>
<h2>Viewport</h2>
The viewport is the user's visible area of a web page. It varies with the device - it will be smaller on a mobile phone than on a computer screen.
<br>
You should include the following <meta> element in all your web pages:
<pre>
&lt;meta name="viewport" content="width=device-width, initial-scale=1.0"&gt;
</pre>
This gives the browser instructions on how to control the page's dimensions and scaling.
<br>
The width=device-width part sets the width of the page to follow the screen-width of the device (which will vary depending on the device).
<br>
The initial-scale=1.0 part sets the initial zoom level when the page is first loaded by the browser.
<br>
Here is an example of a web page without the viewport meta tag, and the same web page with the viewport meta tag:
<br>
Without Viewport:
<img src="https://i.imgur.com/WmlObjq.jpg" width="200px" height="auto">
<br>
With Viewport:
<img src="https://i.imgur.com/66NihmH.jpg" width="200px" height="auto">
<h1>script</h1>
The <script> element is used to define client-side JavaScripts.
<br>
The following JavaScript writes "Hello JavaScript!" into an HTML element with id="demo":
<pre>
&lt;head&gt;
  &lt;script&gt;
    function myFunction() {
      document.getElementById("demo").innerHTML = "Hello JavaScript!";
    }
  &lt;/script&gt;
&lt;/head&gt;
</pre>
<h1>base</h1>
The base element specifies the base URL and/or target for all relative URLs in a page.
<br>
The base tag must have either an href or a target attribute present, or both.
<br>
There can only be one single base element in a document!
<pre>
&lt;head&gt;
&lt;base href="https://www.w3schools.com/" target="_blank"&gt;
&lt;/head&gt;
<p></p>
&lt;body&gt;
&lt;img src="images/stickman.gif" width="24" height="39" alt="Stickman"&gt;
&lt;a href="tags/tag_base.asp"&gt;HTML base Tag&lt;/a&gt;
&lt;/body&gt;
</pre>
<h1>Tags</h1>
<table class="ws-table-all notranslate">
<tr>
<th style="width:20%">Tag</th>
<th>Description</th>
</tr>
<tr>
<td>&lt;head&gt;</td>
<td>Defines information about the document</td>
</tr>
<tr>
<td>&lt;title&gt;</td>
<td>Defines the title of a document</td>
</tr>
<tr>
<td>&lt;base&gt;</td>
<td>Defines a part of text in an alternate voice or mood</td>
</tr>
<tr>
<td>&lt;link&gt;</td>
<td>Defines smaller text</td>
</tr>
<tr>
<td>&lt;meta&gt;</td>
<td>Defines important text</td>
</tr>
<tr>
<td>&lt;script&gt;</td>
<td>Defines subscripted text</td>
</tr>
<tr>
<td>&lt;style&gt;</td>
<td>Defines superscripted text</td>
</tr>
</table>
