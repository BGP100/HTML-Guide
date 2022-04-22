<a href="/JS/DOM/Methods.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/DOM/Elements.md">Next &gt;</a>
<hr>
The HTML DOM document object is the owner of all other objects in your web page.
<h1>The Document Object</h1>
The document object represents your web page.
<br>
If you want to access any element in an HTML page, you always start with accessing the document object.
<br>
Below are some examples of how you can use the document object to access and manipulate HTML.
<h1>Changing HTML Elements</h1>
<table class="ws-table-all notranslate">
  <tr>
    <th>Property</th>
    <th>Description</th>
  </tr>
  <tr>
    <td><em>element</em>.innerHTML = <em>new html content</em></td>
    <td>Change the inner HTML of an element</td>
  </tr>
  <tr>
    <td><em>element</em>.<em>attribute = new value</em></td>
    <td>Change the attribute value of an HTML element</td>
  </tr>
  <tr>
    <td><em>element</em>.style.<em>property = new style</em></td>
    <td>Change the style of an HTML element</td>
  </tr>
</table>
<table class="ws-table-all notranslate">
  <tr>
    <th>Method</th>
    <th>Description</th>
  </tr>
  <tr>
    <td><em>element</em>.setAttribute<em>(attribute, value)</em></td>
    <td>Change the attribute value of an HTML element</td>
  </tr>
</table>
<h1>Adding and Deleting Elements</h1>
<table class="ws-table-all notranslate">
  <tr>
    <th>Method</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>document.createElement(<em>element</em>)</td>
    <td>Create an HTML element</td>
  </tr>
  <tr>
    <td>document.removeChild(<em>element</em>)</td>
    <td>Remove an HTML element</td>
  </tr>
  <tr>
    <td>document.appendChild(<em>element</em>)</td>
    <td>Add an HTML element</td>
  </tr>
  <tr>
    <td>document.replaceChild(<em>new, old</em>)</td>
    <td>Replace an HTML element</td>
  </tr>
  <tr>
    <td>document.write(<em>text</em>)</td>
    <td>Write into the HTML output stream</td>
  </tr>
</table>
<h1>Adding Events Handlers</h1>
<table class="ws-table-all notranslate">
  <tr>
    <th>Method</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>document.getElementById(<em>id</em>).onclick = function(){<em>code</em>}</td>
    <td>Adding event handler code to an onclick event</td>
  </tr>
</table>
<h1>Finding HTML Objects</h1>
The first HTML DOM Level 1 (1998), defined 11 HTML objects, object collections, and properties. These are still valid in HTML5.
<br>
Later, in HTML DOM Level 3, more objects, collections, and properties were added.
<table class="ws-table-all notranslate">
  <tr>
    <th>Property</th>
    <th>Description</th>
    <th>DOM</th>
  </tr>
  <tr>
    <td>document.anchors</td>
    <td>Returns all &lt;a&gt; elements that have a name attribute</td>
    <td>1</td>
  </tr>
  <tr>
    <td>document.applets</td>
    <td><span class="deprecated">Deprecated</span></td>
    <td>1</td>
  </tr>
  <tr>
    <td>document.baseURI</td>
    <td>Returns the absolute base URI of the document</td>
    <td>3</td>
  </tr>
  <tr>
    <td>document.body</td>
    <td>Returns the &lt;body&gt; element </td>
    <td>1</td>
  </tr>
  <tr>
    <td>document.cookie</td>
    <td>Returns the document's cookie</td>
    <td>1</td>
  </tr>
  <tr>
    <td>document.doctype</td>
    <td>Returns the document's doctype</td>
    <td>3</td>
  </tr>
  <tr>
    <td>document.documentElement</td>
    <td>Returns the &lt;html&gt; element </td>
    <td>3</td>
  </tr>
  <tr>
    <td>document.documentMode</td>
    <td>Returns the mode used by the browser</td>
    <td>3</td>
  </tr>
  <tr>
    <td>document.documentURI</td>
    <td>Returns the URI of the document </td>
    <td>3</td>
  </tr>
  <tr>
    <td>document.domain</td>
    <td>Returns the domain name of the document server </td>
    <td>1</td>
  </tr>
  <tr>
    <td>document.domConfig</td>
    <td><span class="deprecated">Obsolete.</span></td>
    <td>3</td>
  </tr>
  <tr>
    <td>document.embeds</td>
    <td>Returns all &lt;embed&gt; elements</td>
    <td>3</td>
  </tr>
  <tr>
    <td>document.forms</td>
    <td>Returns all &lt;form&gt; elements </td>
    <td>1</td>
  </tr>
  <tr>
    <td>document.head</td>
    <td>Returns the &lt;head&gt; element</td>
    <td>3</td>
  </tr>
  <tr>
    <td>document.images</td>
    <td>Returns all &lt;img&gt; elements </td>
    <td>1</td>
  </tr>
  <tr>
    <td>document.implementation</td>
    <td>Returns the DOM implementation</td>
    <td>3</td>
  </tr>
  <tr>
    <td>document.inputEncoding</td>
    <td>Returns the document's encoding (character set)</td>
    <td>3</td>
  </tr>
  <tr>
    <td>document.lastModified</td>
    <td>Returns the date and time the document was updated</td>
    <td>3</td>
  </tr>
  <tr>
    <td>document.links</td>
    <td>Returns all &lt;area&gt; and &lt;a&gt; elements that have a href attribute</td>
    <td>1</td>
  </tr>
  <tr>
    <td>document.readyState</td>
    <td>Returns the (loading) status of the document</td>
    <td>3</td>
  </tr>
  <tr>
    <td>document.referrer</td>
    <td>Returns the URI of the referrer (the linking document)</td>
    <td>1</td>
  </tr>
  <tr>
    <td>document.scripts</td>
    <td>Returns all &lt;script&gt; elements</td>
    <td>3</td>
  </tr>
  <tr>
    <td>document.strictErrorChecking</td>
    <td>Returns if error checking is enforced</td>
    <td>3</td>
  </tr>
  <tr>
    <td>document.title</td>
    <td>Returns the &lt;title&gt; element </td>
    <td>1</td>
  </tr>
  <tr>
    <td>document.URL</td>
    <td>Returns the complete URL of the document </td>
    <td>1</td>
  </tr>
</table>
