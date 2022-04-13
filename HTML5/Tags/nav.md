<a href="/HTML5/Tags/main.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/HTML5/Tags/section.md">Next &gt;</a>
<hr>
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
<h1>Browser Support</h1>
<table class="ws-table-all notranslate">
  <tr>
    <th>&lt;nav&gt;</th>
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
    <td>11.1</td>
  </tr>
</table>
<h1>Default CSS</h1>
<pre>
nav { 
  display: block;
}
</pre>
