<a href="/HTML5/Code.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/HTML5/Quiz.md">Next &gt;</a>
<hr>
<h1>Some Changes</h1>
Most of the individual changes are a result of larger objectives in the design of the language. These objectives primarily include:
<ol>
  <li>Encouraging semantic (meaningful) markup</li>
  <li>Separating design from content</li>
  <li>Promoting accessibility and design responsiveness</li>
  <li>Reducing the overlap between HTML, CSS, and JavaScript</li>
  <li>Supporting rich media experiences while eliminating the need for plugins such as Flash or Java</li>
</ol>
<h1>New Tags</h1>
In previous versions of the language, common structural elements like page headers, navigation menus, and main content sections were all indicated with the same HTML element, the <b>&lt;div&gt;</b> tag. In HTML, there are a host of new semantic elements intended to indicate the basic structure of a page:
<ol>
  <li>&lt;article&gt;</li>
  <li>&lt;aside&gt;</li>
  <li>&lt;footer&gt;</li>
  <li>&lt;header&gt;</li>
  <li>&lt;main&gt;</li>
  <li>&lt;nav&gt;</li>
  <li>&lt;section&gt;</li>
</ol>
New text-level (inline) elements have also been introduced, such as <b>&lt;address&gt;</b> and <b>&lt;time&gt;</b>. These help search engines and other services to easily find information on a page, for display in other contexts. At the same time, existing inline elements which produce various effects like bold, italic, and underline have been refined or redefined to imply specific semantic meaning.
<h2>&lt;article&gt;</h2>
The <b>&lt;article&gt;</b> tag specifies independent, self-contained content.
<br>
An article should make sense on its own and it should be possible to distribute it independently from the rest of the site.
<br>
Potential sources for the <b>&lt;article&gt;</b> element:
<ul>
  <li>Forum post.</li>
  <li>Blog post.</li>
  <li>News story.</li>
</ul>
<b>Note:</b> The <b>&lt;article&gt;</b> element does not render as anything special in a browser. However, you can use CSS to style the <b>&lt;article&gt;</b> element (see example below).
<pre>
&lt;article&gt;
&lt;h2&gt;Google Chrome&lt;/h2&gt;
&lt;p&gt;Google Chrome is a web browser developed by Google, released in 2008. Chrome is the world's most popular web browser today!&lt;/p&gt;
&lt;/article&gt;
<p></p>
&lt;article&gt;
&lt;h2>Mozilla Firefox&lt;/h2&gt;
&lt;p&gt;Mozilla Firefox is an open-source web browser developed by Mozilla. Firefox has been the second most popular web browser since January, 2018.&lt;/p&gt;
&lt;/article&gt;
<p></p>
&lt;article>
&lt;h2&gt;Microsoft Edge&lt;/h2&gt;
&lt;p&gt;Microsoft Edge is a web browser developed by Microsoft, released in 2015. Microsoft Edge replaced Internet Explorer.&lt;/p&gt;
&lt;/article&gt;
</pre>
<h3>Browser Support</h3>
<table class="ws-table-all notranslate">
  <tr>
    <th>&lt;article&gt;</th>
    <th>Chrome</th>
    <th>Edge</th>
    <th>Firefox</th>
    <th>Safari</th>
    <th>Opera</th>
  </tr>
  <tr>
    <td>Version</td>
    <td>6.0</td>
    <td>9.0</td>
    <td>4.0</td>
    <td>5.0</td>
    <td>11.1</td>
  </tr>
</table>
<h3>Default CSS:</h3>
<pre>
article { 
  display: block;
}
</pre>
<h2>&lt;aside&gt;</h2>
The <b>&lt;aside&gt;</b> tag defines some content aside from the content it is placed in.
<br>
The aside content should be indirectly related to the surrounding content.
<br>
<b>Tip:</b> The <b>&lt;aside&gt;</b> content is often placed as a sidebar in a document.
<br>
<b>Note:</b> The <b>&lt;aside&gt;</b> element does not render as anything special in a browser. However, you can use CSS to style the <b>&lt;aside&gt;</b> element (see example below).
<pre>
&lt;p&gt;My family and I visited The Epcot center this summer. The weather was nice, and Epcot was amazing! I had a great summer together with my family!&lt;/p&gt;
<p></p>
&lt;aside&gt;
&lt;h4&gt;Epcot Center&lt;/h4&gt;
&lt;p&gt;Epcot is a theme park at Walt Disney World Resort featuring exciting attractions, international pavilions, award-winning fireworks and seasonal special events.&lt;/p&gt;
&lt;/aside&gt;
</pre>
<h3>Browser Support</h3>
<table class="ws-table-all notranslate">
  <tr>
    <th>&lt;article&gt;</th>
    <th>Chrome</th>
    <th>Edge</th>
    <th>Firefox</th>
    <th>Safari</th>
    <th>Opera</th>
  </tr>
  <tr>
    <td>Version</td>
    <td>6.0</td>
    <td>9.0</td>
    <td>4.0</td>
    <td>5.0</td>
    <td>11.1</td>
  </tr>
</table>
<h3>Default CSS:</h3>
<pre>
aside { 
  display: block;
}
</pre>
<h2>&lt;footer&gt;</h2>
The <b>&lt;footer&gt;</b> tag defines a footer for a document or section.
<br>
A <b>&lt;footer&gt;</b> element typically contains:
<ul>
  <li>Authorship Information</li>
  <li>Copyright Information</li>
  <li>Contact Information</li>
  <li>Sitemap</li>
  <li>Back to top Links</li>
  <li>Related Documents</li>
</ul>
You can have several <b>&lt;footer&gt;</b> elements in one document.
<pre>
&lt;footer&gt;
  &lt;p&gt;Author: Hege Refsnes&lt;/p&gt;
  &lt;p&gt;&lt;a href="mailto:name@example.com">name@example.com&lt;/a&gt;&lt;/p&gt;
&lt;/footer&gt;
</pre>
<h3>Browser Support</h3>
<table class="ws-table-all notranslate">
  <tr>
    <th>&lt;article&gt;</th>
    <th>Chrome</th>
    <th>Edge</th>
    <th>Firefox</th>
    <th>Safari</th>
    <th>Opera</th>
  </tr>
  <tr>
    <td>Version</td>
    <td>6.0</td>
    <td>9.0</td>
    <td>4.0</td>
    <td>5.0</td>
    <td>11.1</td>
  </tr>
</table>
<h3>Default CSS:</h3>
<pre>
footer { 
  display: block;
}
</pre>
<h2>&lt;header&gt;</h2>
The <b>&lt;header&gt;</b> element represents a container for introductory content or a set of navigational links.
<br>
A <b>&lt;header&gt;</b> element typically contains:
<ul>
  <li>One or more heading elements (&lt;h1&gt; ••• &lt;h6&gt;)</li>
  <li>Logo or icon</li>
  <li>Authorship information</li>
</ul>
<b>Note:</b> You can have several <b>&lt;header&gt;</b> elements in one HTML document. However, <b>&lt;header&gt;</b> cannot be placed within a <b>&lt;footer&gt;</b>, <b>&lt;address&gt;</b> or another <b>&lt;header&gt;</b> element.
<pre>
&lt;article&gt;
  &lt;header&gt;
    &lt;h1&gt;A heading here&lt;/h1&gt;
    &lt;p&gt;Posted by John Doe&lt;/p&gt;
    &lt;p&gt;Some additional information here&lt;/p&gt;
  &lt;/header&gt;
  &lt;p&gt;Lorem Ipsum dolor set amet....&lt;/p&gt;
&lt;/article&gt;
</pre>
<h3>Browser Support</h3>
<table class="ws-table-all notranslate">
  <tr>
    <th>&lt;article&gt;</th>
    <th>Chrome</th>
    <th>Edge</th>
    <th>Firefox</th>
    <th>Safari</th>
    <th>Opera</th>
  </tr>
  <tr>
    <td>Version</td>
    <td>6.0</td>
    <td>9.0</td>
    <td>4.0</td>
    <td>5.0</td>
    <td>11.1</td>
  </tr>
</table>
<h3>Default CSS:</h3>
<pre>
header { 
  display: block;
}
</pre>
<h2>&lt;main&gt;</h2>
The <b>&lt;main&gt;</b> tag specifies the main content of a document.
<br>
The content inside the <b>&lt;main&gt;</b> element should be unique to the document. It should not contain any content that is repeated across documents such as sidebars, navigation links, copyright information, site logos, and search forms.
<br>
<b>Note:</b> There must not be more than one <b>&lt;main&gt;</b> element in a document. The <b>&lt;main&gt;</b> element must NOT be a descendant of an <b>&lt;article&gt;</b>, <b>&lt;aside&gt;</b>, <b>&lt;footer&gt;</b>, <b>&lt;header&gt;</b>, or <b>&lt;nav&gt;</b> element.
<pre>
&lt;main&gt;
  &lt;h1&gt;Most Popular Browsers&lt;/h1&gt;
  &lt;p&gt;Chrome, Firefox, and Edge are the most used browsers today.&lt;/p&gt;
  &lt;article&gt;
    &lt;h2&gt;Google Chrome&lt;/h2&gt;
    &lt;p&gt;Google Chrome is a web browser developed by Google, released in 2008. Chrome is the world's most popular web browser today!&lt;/p&gt;
  &lt;/article&gt;
  &lt;article&gt;
    &lt;h2&gt;Mozilla Firefox&lt;/h2&gt;
    &lt;p&gt;Mozilla Firefox is an open-source web browser developed by Mozilla. Firefox has been the second most popular web browser since January, 2018.&lt;/p&gt;
  &lt;/article&gt;
  &lt;article&gt;
    &lt;h2&gt;Microsoft Edge&lt;/h2&gt;
    &lt;p&gt;Microsoft Edge is a web browser developed by Microsoft, released in 2015. Microsoft Edge replaced Internet Explorer.&lt;/p&gt;
  &lt;/article&gt;
&lt;/main&gt;
</pre>
<h3>Browser Support</h3>
<table class="ws-table-all notranslate">
  <tr>
    <th>&lt;article&gt;</th>
    <th>Chrome</th>
    <th>Edge</th>
    <th>Firefox</th>
    <th>Safari</th>
    <th>Opera</th>
  </tr>
  <tr>
    <td>Version</td>
    <td>26.0</td>
    <td>12.0</td>
    <td>21.0</td>
    <td>7.0</td>
    <td>16.0</td>
  </tr>
</table>
<h3>Default CSS:</h3>
<pre>
main { 
  margin: 0;
  padding: auto;
  background-color: white;
}
</pre>
<h2>&lt;nav&gt;</h2>
The <b>&lt;nav&gt;</b> tag defines a set of navigation links.
<br>
Notice that NOT all links of a document should be inside a <b>&lt;nav&gt;</b> element. The <b>&lt;nav&gt;</b> element is intended only for major block of navigation links.
<br>
Browsers, such as screen readers for disabled users, can use this element to determine whether to omit the initial rendering of this content.
<pre>
&lt;nav&gt;
  &lt;a href="/html/"&gt;HTML&lt;/a&gt;
  &lt;span&gt;|&lt;/span&gt;
  &lt;a href="/css/"&gt;CSS&lt;/a&gt;
  &lt;span&gt;|&lt;/span&gt;
  &lt;a href="/js/"&gt;JavaScript&lt;/a&gt;
  &lt;span&gt;|&lt;/span&gt;
  &lt;a href="/python/"&gt;Python&lt;/a&gt;
&lt;/nav&gt;
</pre>
<h3>Browser Support</h3>
<table class="ws-table-all notranslate">
  <tr>
    <th>&lt;article&gt;</th>
    <th>Chrome</th>The <b>&lt;nav&gt;</b> tag defines a set of navigation links.
<br>
Notice that NOT all links of a document should be inside a <b>&lt;nav&gt;</b> element. The <b>&lt;nav&gt;</b> element is intended only for major block of navigation links.
<br>
Browsers, such as screen readers for disabled users, can use this element to determine whether to omit the initial rendering of this content.
<pre>
&lt;nav&gt;
  &lt;a href="/html/"&gt;HTML&lt;/a&gt;
  &lt;span&gt;|&lt;/span&gt;
  &lt;a href="/css/"&gt;CSS&lt;/a&gt;
  &lt;span&gt;|&lt;/span&gt;
  &lt;a href="/js/"&gt;JavaScript&lt;/a&gt;
  &lt;span&gt;|&lt;/span&gt;
  &lt;a href="/python/"&gt;Python&lt;/a&gt;
&lt;/nav&gt;
</pre>
    <th>Edge</th>
    <th>Firefox</th>
    <th>Safari</th>
    <th>Opera</th>
  </tr>
  <tr>
    <td>Version</td>
    <td>5.0</td>
    <td>9.0</td>
    <td>4.0</td>
    <td>5.0</td>
    <td>11.1</td>
  </tr>
</table>
<h3>Default CSS:</h3>
<pre>
nav { 
  display: block;
}
</pre>
<h2>&lt;section&gt;</h2>
The <b>&lt;section&gt;</b> tag defines a section of a document.
<pre>
&lt;section&gt;
&lt;h2&gt;WWF History&lt;/h2&gt;
&lt;p&gt;The World Wide Fund for Nature (WWF) is an international organization working on issues regarding the conservation, research and restoration of the environment, formerly named the World Wildlife Fund. WWF was founded in 1961.&lt;/p&gt;
&lt;/section&gt;
&lt;section&gt;
&lt;h2&gt;WWF's Symbol&lt;/h2&gt;
&lt;p&gt;The Panda has become the symbol of WWF. The well-known panda logo of WWF originated from a panda named Chi Chi that was transferred from the Beijing Zoo to the London Zoo in the same year of the establishment of WWF.&lt;/p&gt;
&lt;/section&gt;
</pre>
<h3>Browser Support</h3>
<table class="ws-table-all notranslate">
  <tr>
    <th>&lt;article&gt;</th>
    <th>Chrome</th>
    <th>Edge</th>
    <th>Firefox</th>
    <th>Safari</th>
    <th>Opera</th>
  </tr>
  <tr>
    <td>Version</td>
    <td>5.0</td>
    <td>9.0</td>
    <td>4.0</td>
    <td>5.0</td>
    <td>11.5</td>
  </tr>
</table>
<h3>Default CSS:</h3>
<pre>
section { 
  display: block;
}
</pre>
<h1>Removed Tags</h1>
All the tags on this list are removed in HTML5 (but can be replaced with css):
<ol>
  <li>&lt;acronym&gt;</li>
  <li>&lt;applet&gt;</li>
  <li>&lt;basefont&gt;</li>
  <li>&lt;big&gt;</li>
  <li>&lt;center&gt;</li>
  <li>&lt;dir&gt;</li>
  <li>&lt;font&gt;</li>
  <li>&lt;frame&gt;</li>
  <li>&lt;frameset&gt;</li>
  <li>&lt;noframes&gt;</li>
  <li>&lt;strike&gt;</li>
  <li>&lt;tt&gt;</li>
</ol>
<h2>&lt;acronym&gt;</h2>
Instead, use <a href="/HTML/Tags/abbr.md">&lt;abbr&gt;</b>
<h2>&lt;applet&gt;</h2>
Instead, use <a href="/HTML/Tags/embed.md">&lt;embed&gt;</a> or <a href="/HTML/Tags/object.md">&lt;object&gt;</a>
<h2>&lt;basefont&gt;</h2>
Instead, use CSS:
<pre>
basefont {
  color: red;
}
</pre>
<h2>&lt;big&gt;</h2>
Instead, use CSS:
<pre>
big {
  font-size: 30px;
}
</pre>
<h2>&lt;center&gt;</h2>
Instead, use CSS:
<pre>
center {
  text-align: center;
}
</pre>
<h2>&lt;dir&gt;</h2>
Instead, use <a href="/HTML/Tags/ul.md">&lt;ul&gt;</a>
<h2>&lt;font&gt;</h2>
Instead, use CSS:
<pre>
font.verdana {
  font-family: verdana;
}
font.courier-new {
  font-family: "Courier New";
}
font.sans-serif {
  font-family: "Source Sans Pro", sans-serif;
}
</pre>
<h2>&lt;frame&gt;</h2>
Not Supported anymore.
<h2>&lt;frameset&gt;</h2>
Not Supported anymore.
<h2>&lt;noframes&gt;</h2>
Not Supported anymore.
<h2>&lt;strike&gt;</h2>
Instead, use <a href="/HTML/Tags/del.md">&lt;del&gt;</a> or <a href="/HTML/Tags/s.md">&lt;s&gt;</a>
<h2>&lt;tt&gt;</h2>
<b>Tip:</b> tt means "teletype text", like monospace.
<br>
Instead, use CSS:
<pre>
tt.lucida-console {
  font-family: "Lucida Console", monospace;
}
</pre>
<h1>Other Stuff</h1>
Along with strongly encouraging semantic (meaningful) markup, the HTML5 specification strongly discourages non-meaningful markup — markup intended only to tell the browser how to display things. This includes things like:
<ul>
  <li>declaring fonts and text colors.</li>
  <li>setting text alignment or justification.</li>
  <li>placing borders on tables.</li>
  <li>defining how text wraps around images.</li>
</ul>
Most of the HTML features that allowed for these sorts of things have been completely deprecated. The few that are still officially supported come with warnings that they are usually not recommended practices.
<br>
There are primarily two reasons to prefer this separation:
<ul>
  <li>It is easier to maintain and redesign a site if the style declarations are confined to CSS.</li>
  <li>Users view web content in a lot of different contexts — desktops, laptops, tablets, mobile phones, RSS readers, and many others. Styles and design decisions that make sense in one environment don’t always make sense in another. So it is much better to provide semantic information and let the content be adapted to the context.</li>
</ul>
