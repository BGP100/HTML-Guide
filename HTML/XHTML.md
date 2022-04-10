<a href="/HTML/URL-Encode.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/HTML/Forms/Main.md">Next &gt;</a>
<hr>
XHTML is a stricter, more XML-based version of HTML.
<h1>What is it?</h1>
<ul>
  <li>XHTML stands for E<strong>X</strong>tensible <strong>H</strong>yper<strong>T</strong>ext <strong>M</strong>arkup <strong>L</strong>anguage</li>
  <li>XHTML is a stricter, more XML-based version of HTML</li>
  <li>XHTML is HTML defined as an XML application</li>
  <li>XHTML is supported by all major browsers</li>
</ul>
<h1>Why XHTML?</h1>
XML is a markup language where all documents must be marked up correctly (be "well-formed").
<br>
XHTML was developed to make HTML more extensible and flexible to work with other data formats (such as XML). In addition, browsers ignore errors in HTML pages, and try to display the website even if it has some errors in the markup. So XHTML comes with a much stricter error handling.
<h1>The Most Important Differences from HTML</h1>
<ul>
  <li>&lt;!DOCTYPE&gt; is <strong>mandatory</strong></li>
  <li>The xmlns attribute in &lt;html&gt; is <strong>mandatory</strong></li>
  <li>&lt;html&gt;, &lt;head&gt;, &lt;title&gt;, and &lt;body&gt; are <strong>mandatory</strong></li>
  <li>Elements must always be <b> properly nested</b></li>
  <li>Elements must always be <b>closed</b></li>
  <li>Elements must always be in <b>lowercase</b></li>
  <li>Attribute names must always be in <b>lowercase</b></li>
  <li>Attribute values must always be <b>quoted</b></li>
  <li>Attribute minimization is <b>forbidden</b></li>
</ul>
<h1>&lt;!DOCTYPE html&gt; is Mandatory?</h1>
An XHTML document must have an XHTML !DOCTYPE declaration.
<br>
The html, head, title, and body elements must also be present, and the xmlns attribute in html must specify the xml namespace for the document.
<pre>
&lt;!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.1//EN" "//www.w3.org/TR/xhtml11/DTD/xhtml11.dtd"&gt;
&lt;html xmlns="http://www.w3.org/1999/xhtml"&gt;
  &lt;head&gt;
    &lt;title&gt;Title of document&lt;/title&gt;
  &lt;/head&gt;
  &lt;body&gt;
    <i>some content here...</i>
  &lt;/body&gt;
&lt;/html&gt;
</pre>
<h1>Elements Must be Properly Nested</h1>
In XHTML, elements must always be properly nested within each other, like this:
<p></p>
<b>Correct:</b>
<pre>&lt;b&gt;&lt;i&gt;Some text&lt;/i&gt;&lt;/b&gt;</pre>
<b>Wrong:</b>
<pre>&lt;b&gt;&lt;i&gt;Some text&lt;/b&gt;&lt;/i&gt;</pre>
<h1>Elements MUST Always be Closed</h1>
Info covered in <a href="BeginnerGuide.md#Close-all-elements">Beginner Guide.</a>
<h1>Empty Elements Must Always be Closed</h1>
In XHTML, empty elements must always be closed, like this:
<p></p>
<b>Correct:</b>
<pre>
A break: &lt;br /&gt;
A horizontal rule: &lt;hr /&gt;
An image: &lt;img src="example.jpg" /&gt;
</pre>
<b>Wrong:</b>
<pre>
A break: &lt;br&gt;
A horizontal rule: &lt;hr&gt;
An image: &lt;img src="example.jpg"&gt;
</pre>
<h1>Elements Must be in Lowercase</h1>
Info covered in <a href="BeginnerGuide.md#Lowercase-Elements">Beginner Guide.</a>
<h1>Attributes Must be in Lowercase</h1>
Info covered in <a href="BeginnerGuide.md#Lowercase-Attributes">Beginner Guide.</a>
<h1>Always Quote Attributes</h1>
Info covered in <a href="BeginnerGuide.md#Always-Quote-Attributes">Beginner Guide.</a>
<h1>Attribute Minimization is Forbidden</h1>
In XHTML, attribute minimization is forbidden:
<p></p>
<b>Correct:</b>
<pre>&lt;input type="checkbox" name="vehicle" value="car" checked="checked" /&gt;</pre>
<b>Wrong:</b>
<pre>&lt;input type="checkbox" name="vehicle" value="car" checked /&gt;</pre>
