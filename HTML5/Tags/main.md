<a href="/HTML5/Tags/header.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/HTML5/Tags/nav.md">Next &gt;</a>
<hr>
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
<h1>Browser Support</h1>
<table class="ws-table-all notranslate">
  <tr>
    <th>&lt;main&gt;</th>
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
<h1>Default CSS</h1>
<pre>
main { 
  margin: 0;
  padding: auto;
  background-color: white;
}
</pre>
