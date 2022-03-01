Semantic elements = elements with a meaning.
<h1>What are they?</h1>
A semantic element clearly describes its meaning to both the browser and the developer.
<br>
Examples of non-semantic elements: <b>&lt;div&gt;</b> and <b>&lt;span&gt;</b> - Tells nothing about its content.
<br>
Examples of semantic elements: <b>&lt;form&gt;</b>, <b>&lt;table&gt;</b>, and <b>&lt;article&gt;</b> - Clearly defines its content.
<h1>Elements</h1>
Many web sites contain HTML code like: div id="nav"> div class="header"> div id="footer"> to indicate navigation, header, and footer.
<br>
In HTML there are some semantic elements that can be used to define different parts of a web page:
<ul>
  <li><a href="#article">&lt;article&gt;</a></li>
  <li><a href="#aside">&lt;aside&gt;</a></li>
  <li><a href="#details">&lt;details&gt;</a></li>
  <li><a href="#figcaption">&lt;figcaption&gt;</a></li>
  <li><a href="#figure">&lt;figure&gt;</a></li>
  <li><a href="#footer">&lt;footer&gt;</a></li>
  <li><a href="#header">&lt;header&gt;</a></li>
  <li><a href="#main">&lt;main&gt;</a></li>
  <li><a href="#mark">&lt;mark&gt;</a></li>
  <li><a href="#nav">&lt;nav&gt;</a></li>
  <li><a href="#section">&lt;section&gt;</a></li>
  <li><a href="#summary">&lt;summary&gt;</a></li>
  <li><a href="#time">&lt;time&gt;</a></li>
</ul>
<img src="https://i.imgur.com/G1MnBfF.gif">
<h1>article</h1>
The <b>article</b> element specifies independent, self-contained content.
<br>
An article should make sense on its own, and it should be possible to distribute it independently from the rest of the web site.
<br>
Examples of where the <b>article</b> element can be used:
<ul>
  <li>Forum posts</li>
  <li>Blog posts</li>
  <li>User comments</li>
  <li>Product cards</li>
  <li>Newspaper articles</li>
</ul>
<pre>
.all-browsers {
  margin: 0;
  padding: 5px;
  background-color: lightgray;
}
.all-browsers > h1, .browser {
  margin: 10px;
  padding: 5px;
}
.browser {
  background: white;
}
.browser > h2, p {
  margin: 4px;
  font-size: 90%;
}
</pre>
<pre>
&lt;article class="all-browsers"&gt;
  &lt;h1&gt;Most Popular Browsers&lt;/h1&gt;
  &lt;article class="browser"&gt;
    &lt;h2&gt;Google Chrome&lt;/h2&gt;
    &lt;p&gt;Google Chrome is a web browser developed by Google, released in 2008. Chrome is the world's most popular web browser today!&lt;/p&gt;
  &lt;/article&gt;
  &lt;article class="browser"&gt;
    &lt;h2&gt;Mozilla Firefox&lt;/h2&gt;
    &lt;p&gt;Mozilla Firefox is an open-source web browser developed by Mozilla. Firefox has been the second most popular web browser since January, 2018.&lt;/p&gt;
  &lt;/article&gt;
  &lt;article class="browser"&gt;
    &lt;h2&gt;Microsoft Edge&lt;/h2&gt;
    &lt;p&gt;Microsoft Edge is a web browser developed by Microsoft, released in 2015. Microsoft Edge replaced Internet Explorer.&lt;/p&gt;
  &lt;/article&gt;
&lt;/article&gt;
</pre>
<h1>aside</h1>
The aside element defines some content aside from the content it is placed in (like a sidebar).
<br>
The aside content should be indirectly related to the surrounding content.
<pre>
&lt;p&gt;My family and I visited The Epcot center this summer. The weather was nice, and Epcot was amazing! I had a great summer together with my family!&lt;/p&gt;
&lt;aside&gt;
&lt;h4&gt;Epcot Center&lt;/h4&gt;
&lt;p&gt;Epcot is a theme park at Walt Disney World Resort featuring exciting attractions, international pavilions, award-winning fireworks and seasonal special events.&lt;/p&gt;
&lt;/aside&gt;
&lt;p&gt;My family and I visited The Epcot center this summer. The weather was nice, and Epcot was amazing! I had a great summer together with my family!&lt;/p&gt;
&lt;p&gt;My family and I visited The Epcot center this summer. The weather was nice, and Epcot was amazing! I had a great summer together with my family!&lt;/p&gt;
</pre>
<pre>
aside {
  width: 30%;
  padding-left: 15px;
  margin-left: 15px;
  float: right;
  font-style: italic;
  background-color: lightgray;
}
</pre>
<img src="https://i.imgur.com/NLz8Bju.jpg" width="40%">
<h1>figcaption</h1>
The <b>figcaption</b> tag defines a caption for a <a href="#figure">figure</a> element. The <b>figcaption</b> element can be placed as the first or as the last child of a <a href="#figure">figure</a> element.
<br>
The <b>img</b> element defines the actual image/illustration.
<pre>
&lt;figure&gt;
  &lt;img src="//i.imgur.com/e2WGQia.jpg" alt="Trulli"&gt;
  &lt;figcaption&gt;Fig1. - Trulli, Puglia, Italy.&lt;/figcaption&gt;
&lt;/figure&gt;
</pre>
<h1>figure</h1>
The <figure> tag specifies self-contained content, like illustrations, diagrams, photos, code listings, etc.
<br>
The <a href="#figcaption">figcaption</a> tag defines a caption for a <b>figure</b> element. The <a href="#figcaption">figcaption</a> element can be placed as the first or as the last child of a <b>figure</b> element.
<br>
The <b>img</b> element defines the actual image/illustration.
<pre>
&lt;figure&gt;
  &lt;img src="//i.imgur.com/e2WGQia.jpg" alt="Trulli"&gt;
  &lt;figcaption&gt;Fig1. - Trulli, Puglia, Italy.&lt;/figcaption&gt;
&lt;/figure&gt;
</pre>
<h1>footer</h1>
The <b>footer</b> element defines a footer for a document or section.
<br>
A <b>footer</b> element typically contains:
<ul>
  <li>Authorship information</li>
  <li>Copyright information</li>
  <li>Contact information</li>
  <li>Sitemap</li>
  <li>Back to top links</li>
  <li>Related documents</li>
</ul>
You can have several <b>footer</b> elements in one document.
<pre>
&lt;footer&gt;
  &lt;p&gt;Author: Hege Refsnes&lt;/p&gt;
  &lt;p&gt;a href="mailto:hege@example.com"&gt;hege@example.com&lt;/a&gt;&lt;/p&gt;
&lt;/footer&gt;
</pre>
<h1>header</h1>
The header element represents a container for introductory content or a set of navigational links.
<br>
A header element typically contains:
<ul>
  <li>One or more heading elements (&lt;h1&gt; ••• &lt;h6&gt;)</li>
  <li>Logo or icon</li>
  <li>Authorship information</li>
  <li>A title</li>
</ul>
<pre>
&lt;header&gt;
  &lt;h1&gt;What Does WWF Do?&lt;/h1&gt;
  &lt;p&gt;WWF's mission:&lt;/p&gt;
&lt;/header&gt;
</pre>
<h1>main</h1>
The &lt;main&gt; tag specifies the main content of a document.
<br>
The content inside the &lt;main&gt; element should be unique to the document. It should not contain any content that is repeated across documents such as sidebars, navigation links, copyright information, site logos, and search forms.
<p></p>
It's too much code, <a href="https://github.com/BGP100/News/blob/main/index.html">click here</a> for an example.
<h1>mark</h1>
The mark tag defines text that should be marked or highlighted.
<h1>nav</h1>
The <b>&lt;nav&gt;</b> element defines a set of navigation links.
<p></p>
Notice that NOT all links of a document should be inside a <nav> element. The <nav> element is intended only for major block of navigation links.
<br>
Browsers, such as screen readers for disabled users, can use this element to determine whether to omit the initial rendering of this content.
<h1>section</h1>
The <b>section</b> element defines a section in a document.
<br>
According to W3C's HTML documentation: "A section is a thematic grouping of content, typically with a heading".
<br>
Examples of where a <b>section</b> element can be used:
<ul>
  <li>Chapters</li>
  <li>Introduction</li>
  <li>News items</li>
  <li>Contact information</li>
</ul>
A web page could normally be split into sections for introduction, content, and contact information.
<pre>
&lt;section&gt;
&lt;h1&gt;WWF&lt;/h1&gt;
&lt;p&gt;The World Wide Fund for Nature (WWF) is an international organization working on issues regarding the conservation, research and restoration of the environment, formerly named the World Wildlife Fund. WWF was founded in 1961.&lt;/p&gt;
&lt;/section&gt;
</pre>
<h1>summary</h1>
The summary tag defines a visible heading for the details element. The heading can be clicked to view/hide the details.
<br>
<b>Note:</b> The summary element should be the first child element of the details element.
<img src="https://i.imgur.com/MRCK8mP.jpg">
<pre>
&lt;details&gt;
&lt;summary&gt;Epcot Center&lt;/summary&gt;
Epcot is a theme park at Walt Disney World Resort featuring exciting attractions, international pavilions, award-winning fireworks and seasonal special events.
&lt;/details&gt;
</pre>
<img src="https://i.imgur.com/MRCK8mP.jpg">
<h1>time</h1>
The <b>&lt;time&gt;</b> tag defines a specific time (or datetime).
<br>
The <b>datetime</b> attribute of this element is used translate the time into a machine-readable format so that browsers can offer to add date reminders through the user's calendar, and search engines can produce smarter search results.
<b>Note:</b> The time element does not render as anything special in any of the major browsers.
<img src="https://i.imgur.com/CuFqIQf.jpg">
