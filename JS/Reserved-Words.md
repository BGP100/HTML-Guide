<a href="/JS/Performance.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Versions/Main.md">Next &gt;</a>
<hr>
In JavaScript you cannot use these reserved words as variables, labels, or function names:
<table class="ws-table-all">
  <tr>
    <td>abstract</td>
    <td>arguments</td>
    <td>await <code>*</code></td>
    <td>boolean</td>
  </tr>
  <tr>
    <td>break</td>
    <td>byte</td>
    <td>case</td>
    <td>catch</td>
  </tr>
  <tr>
    <td>char</td>
    <td>class <code>*</code></td>
    <td>const</td>
    <td>continue</td>
  </tr>
  <tr>
    <td>debugger</td>
    <td>default</td>
    <td>delete</td>
    <td>do</td>
  </tr>
  <tr>
    <td>double</td>
    <td>else</td>
    <td>enum <code>*</code></td>
    <td>eval</td>
  </tr>
  <tr>
    <td>export <code>*</code></td>
    <td>extends <code>*</code></td>
    <td>false</td>
    <td>final</td>
  </tr>
  <tr>
    <td>finally</td>
    <td>float</td>
    <td>for</td>
    <td>function</td>
  </tr>
  <tr>
    <td>goto</td>
    <td>if</td>
    <td>implements</td>
    <td>import <code>*</code></td>
  </tr>
  <tr>
    <td>in</td>
    <td>instanceof</td>
    <td>int</td>
    <td>interface</td>
  </tr>
  <tr>
    <td>let <code>*</code></td>
    <td>long</td>
    <td>native</td>
    <td>new</td>
  </tr>
  <tr>
    <td>null</td>
    <td>package</td>
    <td>private</td>
    <td>protected</td>
  </tr>
  <tr>
    <td>public</td>
    <td>return</td>
    <td>short</td>
    <td>static</td>
  </tr>
  <tr>
    <td>super <code>*</code></td>
    <td>switch</td>
    <td>synchronized</td>
    <td>this</td>
  </tr>
  <tr>
    <td>throw</td>
    <td>throws</td>
    <td>transient</td>
    <td>true</td>
  </tr>
  <tr>
    <td>try</td>
    <td>typeof</td>
    <td>var</td>
    <td>void</td>
  </tr>
  <tr>
    <td>volatile</td>
    <td>while</td>
    <td>with</td>
    <td>yield</td>
  </tr>
</table>
Words marked with <code>*</code> are new in ECMAScript 5 and 6.
<h1>Removed Reserved Words</h1>
The following reserved words have been removed from the ECMAScript 5/6 standard:
<table class="ws-table-all">
  <tr>
    <td>abstract</td>
    <td>boolean</td>
    <td>byte</td>
    <td>char</td>
  </tr>
  <tr>
    <td>double</td>
    <td>final</td>
    <td>float</td>
    <td>goto</td>
  </tr>
  <tr>
    <td>int</td>
    <td>long</td>
    <td>native</td>
    <td>short</td>
  </tr>
  <tr>
    <td>synchronized</td>
    <td>throws</td>
    <td>transient</td>
    <td>volatile</td>
  </tr>
</table>
<h1>Objects, Properties, and Methods</h1>
You should also avoid using the name of JavaScript built-in objects, properties, and methods:
<table class="ws-table-all">
  <tr>
    <td>Array</td>
    <td>Date</td>
    <td>eval</td>
    <td>function</td>
  </tr>
  <tr>
    <td>hasOwnProperty</td>
    <td>Infinity</td>
    <td>isFinite</td>
    <td>isNaN</td>
  </tr>
  <tr>
    <td>isPrototypeOf</td>
    <td>length</td>
    <td>Math</td>
    <td>NaN</td>
  </tr>
  <tr>
    <td>name</td>
    <td>Number</td>
    <td>Object</td>
    <td>prototype</td>
  </tr>
  <tr>
    <td>String</td>
    <td>toString</td>
    <td>undefined</td>
    <td>valueOf</td>
  </tr>
</table>
<h1>Java Reserved Words</h1>
JavaScript is often used together with Java. You should avoid using some Java objects and properties as JavaScript identifiers:
<table class="ws-table-all">
  <tr>
    <td>getClass</td>
    <td>java</td>
    <td>JavaArray</td>
  </tr>
  <tr>
    <td>JavaObject</td>
    <td>JavaPackage</td>
    <td>javaClass</td>
  </tr>
</table>
<h2>Other Reserved Words</h2>
JavaScript can be used as the programming language in many applications.
<br>
You should also avoid using the name of HTML and Window objects and properties:
<table class="ws-table-all">
  <tr>
    <td>alert</td>
    <td>all</td>
    <td>anchor</td>
    <td>anchors</td>
  </tr>
  <tr>
    <td>area</td>
    <td>assign</td>
    <td>blur</td>
    <td>button</td>
  </tr>
  <tr>
    <td>checkbox</td>
    <td>clearInterval</td>
    <td>clearTimeout</td>
    <td>clientInformation</td>
  </tr>
  <tr>
    <td>close</td>
    <td>closed</td>
    <td>confirm</td>
    <td>constructor</td>
  </tr>
  <tr>
    <td>crypto</td>
    <td>decodeURI</td>
    <td>decodeURIComponent</td>
    <td>defaultStatus</td>
  </tr>
  <tr>
    <td>document</td>
    <td>element</td>
    <td>elements</td>
    <td>embed</td>
  </tr>
  <tr>
    <td>embeds</td>
    <td>encodeURI</td>
    <td>encodeURIComponent</td>
    <td>escape</td>
  </tr>
  <tr>
    <td>event</td>
    <td>fileUpload</td>
    <td>focus</td>
    <td>form</td>
  </tr>
  <tr>
    <td>forms</td>
    <td>frame</td>
    <td>innerHeight</td>
    <td>innerWidth</td>
  </tr>
  <tr>
    <td>layer</td>
    <td>layers</td>
    <td>link</td>
    <td>location</td>
  </tr>
  <tr>
    <td>mimeTypes</td>
    <td>navigate</td>
    <td>navigator</td>
    <td>frames</td>
  </tr>
  <tr>
    <td>frameRate</td>
    <td>hidden</td>
    <td>history</td>
    <td>image</td>
  </tr>
  <tr>
    <td>images</td>
    <td>offscreenBuffering</td>
    <td>open</td>
    <td>opener</td>
  </tr>
  <tr>
    <td>option</td>
    <td>outerHeight</td>
    <td>outerWidth</td>
    <td>packages</td>
  </tr>
  <tr>
    <td>pageXOffset</td>
    <td>pageYOffset</td>
    <td>parent</td>
    <td>parseFloat</td>
  </tr>
  <tr>
    <td>parseInt</td>
    <td>password</td>
    <td>pkcs11</td>
    <td>plugin</td>
  </tr>
  <tr>
    <td>prompt</td>
    <td>propertyIsEnum</td>
    <td>radio</td>
    <td>reset</td>
  </tr>
  <tr>
    <td>screenX</td>
    <td>screenY</td>
    <td>scroll</td>
    <td>secure</td>
  </tr>
  <tr>
    <td>select</td>
    <td>self</td>
    <td>setInterval</td>
    <td>setTimeout</td>
  </tr>
  <tr>
    <td>status</td>
    <td>submit</td>
    <td>taint</td>
    <td>text</td>
  </tr>
  <tr>
    <td>textarea</td>
    <td>top</td>
    <td>unescape</td>
    <td>untaint</td>
  </tr>
  <tr>
    <td>window</td>
  </tr>
</table>
<h1>HTML Event Handlers</h1>
In addition you should avoid using the name of all HTML event handlers.
<div class="w3-responsive notranslate">
<table class="ws-table-all">
  <tr>
    <td>onblur</td>
    <td>onclick</td>
    <td>onerror</td>
    <td>onfocus</td>
  </tr>
  <tr>
    <td>onkeydown</td>
    <td>onkeypress</td>
    <td>onkeyup</td>
    <td>onmouseover</td>
  </tr>
  <tr>
    <td>onload</td>
    <td>onmouseup</td>
    <td>onmousedown</td>
    <td>onsubmit</td>
  </tr>
</table>
