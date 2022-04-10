<a href="/CSS/Selectors.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/Comments.md">Next &gt;</a>
<hr>
There are three ways of inserting a style sheet:
<ul>
  <li>External CSS</li>
  <li>Internal CSS</li>
  <li>Inline CSS</li>
</ul>
<h1>External</h1>
With an external style sheet, you can change the look of an entire website by changing just one file!
<br>
Each HTML page must include a reference to the external style sheet file inside the <b>&lt;link&gt;</b> element, inside the head section.
<pre>
&lt;head&gt;
  &lt;link rel="stylesheet" href="style.css"&gt;
&lt;/head&gt;
</pre>
External styles are defined within the <b>&lt;link&gt;</b> element, inside the <b>&lt;head&gt;</b> section of an HTML page:
<br>
<b>"mystyle.css"</b>
<pre>
body {
  background-color: lightblue;
}
h1, p {
  color: navy;
  margin-left: 20px;
}
</pre>
<h1>Internal</h1>
An internal style sheet may be used if one single HTML page has a unique style.
<br>
The internal style is defined inside the <b>&lt;style&gt;</b> element, inside the head section.
<pre>
&lt;head&gt;
  &lt;style&gt;
    body {
      background-color: lightblue;
    }
    h1, p {
      color: navy;
      margin-left: 20px;
    }
  &lt;/style&gt;
&lt;/head&gt;
</pre>
<h1>Inline</h1>
An inline style may be used to apply a unique style for a single element.
<br>
To use inline styles, add the style attribute to the relevant element. The style attribute can contain any CSS property.
<pre>
&lt;h1 style="color:blue;text-align:center;"&gt;This is a heading&lt;/h1&gt;
&lt;p style="color:red;"&gt;This is a paragraph.&lt;/p&gt;
</pre>
