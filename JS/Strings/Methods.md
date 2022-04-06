String methods help you to work with strings.
<br>
Primitive values, like "John Doe", cannot have properties or methods (because they are not objects).
<br>
But with JavaScript, methods and properties are also available to primitive values, because JavaScript treats primitive values as objects when executing methods and properties.
<h1>String Parts</h1>
There are 3 methods for extracting a part of a string:
<ul>
  <li><a href="#slice">slice(start, end)</a></li>
  <li><a href="#substring">substring(start, end)</a></li>
  <li><a href="#substr">substr(start, length)</a></li>
</ul>
<h2>slice()</h2>
<b>slice()</b> extracts a part of a string and returns the extracted part in a new string.
<br>
The method takes 2 parameters: the start position, and the end position (end not included).
<br>
This example slices out a portion of a string from position 7 to position 12 (13-1):
<pre>
let str = "Apple, Banana, Kiwi";
let part = str.slice(7, 13);
</pre>
If a parameter is negative, the position is counted from the end of the string.
<br>
This example slices out a portion of a string from position -12 to position -6:
<pre>
let str = "Apple, Banana, Kiwi";
let part = str.slice(-12, -6);
</pre>
If you omit the second parameter, the method will slice out the rest of the string:
<pre>let part = str.slice(7);</pre>
or, counting from the end:
<pre>let part = str.slice(-12);</pre>
<h2>substring()</h2>
<b>substring()</b> is similar to <b>slice()</b>.
<br>
The difference is that <b>substring()</b> cannot accept negative indexes.
<pre>
let str = "Apple, Banana, Kiwi";
let part = str.substring(7, 13);
</pre>
If you omit the second parameter, <b>substring()</b> will slice out the rest of the string.
<h2>substr()</h2>
<b>substr()</b> is similar to <b>slice()</b>.
<br>
The difference is that the second parameter specifies the length of the extracted part.
<pre>
let str = "Apple, Banana, Kiwi";
let part = str.substr(7, 6);
</pre>
If you omit the second parameter, <b>substr()</b> will slice out the rest of the string.
<pre>
let str = "Apple, Banana, Kiwi";
let part = str.substr(7);
</pre>
If the first parameter is negative, the position counts from the end of the string.
<pre>
let str = "Apple, Banana, Kiwi";
let part = str.substr(-4);
</pre>
