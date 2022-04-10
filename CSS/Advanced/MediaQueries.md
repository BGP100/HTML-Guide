<a href="/CSS/Advanced/BoxSizing.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/Advanced/Flexbox/Main.md">Next &gt;</a>
<hr>
The <b>@media</b> rule, introduced in CSS2, made it possible to define different style rules for different media types.
<br>
Examples: You could have one set of style rules for computer screens, one for printers, one for handheld devices, one for television-type devices, and so on.
<br>
Unfortunately these media types never got a lot of support by devices, other than the print media type.
<hr>
Media queries in CSS3 extended the CSS2 media types idea: Instead of looking for a type of device, they look at the capability of the device.
<br>
Media queries can be used to check many things, such as:
<ul>
  <li>width and height of the viewport</li>
  <li>width and height of the device</li>
  <li>orientation (is the tablet/phone in landscape or portrait mode?)</li>
  <li>resolution</li>
</ul>
Using media queries are a popular technique for delivering a tailored style sheet to desktops, laptops, tablets, and mobile phones (such as iPhone and Android phones).
<h1>Browser Support</h1>
The numbers in the table specifies the first browser version that fully supports the <b>@media</b> rule.
<table class="ws-table-all notranslate">
  <tr>
    <th>Browser</th>
    <th>Chrome</th>
    <th>Edge</th>
    <th>Firefox</th>
    <th>Safari</th>
    <th>Opera</th>
  </tr>
  <tr>
    <td>Version</td>
    <td>49.0</td>
    <td>15.0</td>
    <td>31.0</td>
    <td>9.1</td>
    <td>36.0</td>
  </tr>
</table>
<h1>Syntax</h1>
A media query consists of a media type and can contain one or more expressions, which resolve to either true or false.
<pre>
@media not|only <i>mediatype</i> and (<i>expressions</i>) {
  CSS-Code;
}
</pre>
The result of the query is true if the specified media type matches the type of device the document is being displayed on and all expressions in the media query are true. When a media query is true, the corresponding style sheet or style rules are applied, following the normal cascading rules.
<br>
Unless you use the not or only operators, the media type is optional and the all type will be implied.
<br>
You can also have different stylesheets for different media:
<pre>&lt;link rel="stylesheet" media="<i>mediatype</i> and (<i>expressions</i>)" href="<i>print.css</i>"&gt;</pre>
<h1>All Media Types</h1>
<table class="ws-table-all notranslate">
  <tr>
    <th>Type</th>
    <th>Description</th>
  </tr>  
  <tr>
    <td>all</td>
    <td>Used for all media type devices</td>
  </tr>
  <tr>
    <td>print</td>
    <td>Used for printers</td>
  </tr>
    <tr>
    <td>screen</td>
    <td>Used for computer screens, tablets, smart-phones etc.</td>
    </tr>
  <tr>
    <td>speech</td>
    <td>Used for screenreaders that &quot;reads&quot; the page out loud</td>
  </tr>
</table>
<h1>Examples</h1>
One way to use media queries is to have an alternate CSS section right inside your style sheet.
<br>
The following example changes the background-color to lightgreen if the viewport is 480 pixels wide or wider (if the viewport is less than 480 pixels, the background-color will be pink):
<pre>
@media screen and (min-width: 480px) {
  body {
    background-color: lightgreen;
  }
}
</pre>
The following example shows a menu that will float to the left of the page if the viewport is 480 pixels wide or wider (if the viewport is less than 480 pixels, the menu will be on top of the content):
<pre>
@media screen and (min-width: 480px) {
  #leftsidebar {width: 200px; float: left;}
  #main {margin-left: 216px;}
}
</pre>
