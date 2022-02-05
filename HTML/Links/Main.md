Links are found in nearly all web pages. Links allow users to click their way from page to page.
<br>
HTML links are hyperlinks.
<br>
You can click on a link and jump to another document.
<br>
When you move the mouse over a link, the mouse arrow will turn into a little hand.
<br>
The HTML <b>&lt;a&gt;</b> tag defines a hyperlink. It has the following syntax:
<pre>&lt;a href="url"&gt;link text&lt;/a&gt;</pre>
The most important attribute of the <b>&lt;a&gt;</b> element is the <b>href</b> attribute, which indicates the link's destination.
<br>
The link text is the part that will be visible to the reader.
<br>
Clicking on the link text, will send the reader to the specified URL address.
<p></p>
<b>Example:</b>
<br>
<a href="https://replit.com/@BledyGames">Visit My Replit Profile!</a>
<pre>&lt;a href="https://replit.com/@BledyGames"&gt;Visit My Replit Profile!&lt;/a&gt;</pre>
By default, links will appear as follows in all browsers:
<ul>
  <li>An unvisited link is underlined and blue.</li>
  <li>A visited link is underlined and purple.</li>
  <li>A non-active link is underlined and red.</li>
</ul>
Links can of course be styled with CSS, to get another look!
<br>
By default, the linked page will be displayed in the current browser window. To change this, you must specify another target for the link.
<br>
The target attribute specifies where to open the linked document.
<br>
The target attribute can have one of the following values:
<ul>
  <li>&lowbar;self - Default. Opens the document in the same window/tab as it was clicked.</li>
  <li>&lowbar;blank - Opens the document in a new window or tab.</li>
  <li>&lowbar;parent - Opens the document in the parent frame.</li>
  <li>&lowbar;top - Opens the document in the full body of the window.</li>
</ul>
<pre>
&lt;a href="https://replit.com/@BledyGames" target="_self"&gt;Visit My Replit Profile!&lt;/a&gt;
&lt;a href="https://replit.com/@BledyGames" target="_blank"&gt;Visit My Replit Profile!&lt;/a&gt;
&lt;a href="https://replit.com/@BledyGames" target="_parent"&gt;Visit My Replit Profile!&lt;/a&gt;
&lt;a href="https://replit.com/@BledyGames" target="_top"&gt;Visit My Replit Profile!&lt;/a&gt;
</pre>
<h1>Absolutes & Relatives</h1>
Both examples above are using an absolute URL (a full web address) in the href attribute.
<br>
A local link (a link to a page within the same website) is specified with a relative URL (without the "https://www" part):
<pre>
&lt;h2&gt;Absolute URLs&lt;/h2&gt;
&lt;p&gt;&lt;a href="https://www.w3.org/">W3C&lt;/a&gt;&lt;/p&gt;
&lt;p&gt;&lt;a href="https://www.google.com/"&gt;Google&lt;/a&gt;&lt;/p&gt;
<p></p>
&lt;h2>Relative URLs&lt;/h2>
&lt;p&gt;&lt;a href="html_images.asp"&gt;HTML Images&lt;/a&gt;&lt;/p&gt;
&lt;p&gt;&lt;a href="/BGP100/HTML-Guide/"&gt;CSS Tutorial&lt;/a&gt;&lt;/p&gt;
</pre>
<h1>URL Images</h1>
To use an image as a link, just put the <b>&lt;img&gt;</b> tag inside the <b>&lt;a&gt;</b> tag:
<pre>
&lt;a href="/BGP/HTML-Guide/"&gt;
  &lt;img src="//www.w3schools.com/html/smiley.gif" alt="HTML tutorial" style="width:42px;height:42px;"&gt;&lt;/a&gt;
</pre>
<h1>eMail URLs</h1>
Use <b>mailto:</b> inside the href attribute to create a link that opens the user's email program (to let them send a new email):
<pre>&lt;a href="mailto:someone@example.com?&Subject=The%20Title%20of%20the%20eMail&Body=The%20Body%20of%20the%20eMail"&gt;Send email!&lt;/a&gt;</pre>
<h1>Buttons</h1>
To use an HTML button as a link, you have to add some <b>&lt;a&gt;</b> code.
<br>
<b>&lt;a&gt;</b> allows you to specify what happens at certain events, such as a click of a button:
<pre>
&lt;a href="https://replit.com/@BledyGames"&gt;
  &lt;button"&gt;Visit My Replit Profile!&lt;/button&gt;
</pre>
<h1>title</h1>
The <b>title</b> attribute specifies extra information about an element. The information is most often shown as a tooltip text when the mouse moves over the element.
<pre>&lt;a href="https://github.com/BGP100/HTML-Guide/" title="Go to HTML Guide page"&gt;Visit my HTML Tutorial&lt;/a&gt;</pre>
