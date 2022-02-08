A file path describes the location of a file in a web site's folder structure.
<table class="ws-table-all">
  <tr>
    <th style="width:280px">Path</th><th>Description</th>
  </tr>
  <tr>
    <td>&lt;img src=&quot;picture.jpg&quot;&gt;</td>
    <td>The &quot;picture.jpg&quot; file is located in the same folder as the current page</td>
  </tr>
  <tr>
    <td>&lt;img src=&quot;images/picture.jpg&quot;&gt;</td>
    <td>The &quot;picture.jpg&quot; file is located in the images folder in the current folder</td>
  </tr>
  <tr>
    <td>&lt;img src=&quot;/images/picture.jpg&quot;&gt;</td>
    <td>The &quot;picture.jpg&quot; file is located in the images folder at the root of the current web</td>
  </tr>
  <tr>
    <td>&lt;img src=&quot;../picture.jpg&quot;&gt;</td>
    <td>The &quot;picture.jpg&quot; file is located in the folder one level up from the current folder</td>
  </tr>
</table>
A file path describes the location of a file in a web site's folder structure.
<br>
File paths are used when linking to external files, like:
<ul>
  <li>Web Pages</li>
  <li>Images</li>
  <li>Style Sheets</li>
  <li>JavaScripts</li>
</ul>
<h1>Absolutes</h1>
An absolute file path is the full URL to a file:
<pre>&lt;img src="//www.w3schools.com/images/picture.jpg"&gt;</pre>
<h1>Relatives</h1>
A relative file path points to a file relative to the current page.
<br>
In the following example, the file path points to a file in the images folder located at the root of the current web:
<pre>&lt;img src="/images/picture.jpg"&gt;</pre>
In the following example, the file path points to a file in the images folder located in the current folder:
<pre>&lt;img src="images/picture.jpg"&gt;</pre>
In the following example, the file path points to a file in the images folder located in the folder one level up from the current folder:
<pre>&lt;img src="../images/picture.jpg"&gt;</pre>
<h1>Practice</h1>
It is best practice to use relative file paths (if possible).
<br>
When using relative file paths, your web pages will not be bound to your current base URL. All links will work on your own computer (localhost) as well as on your current public domain and your future public domains.
