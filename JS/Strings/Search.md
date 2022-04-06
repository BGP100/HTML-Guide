String Search Methods:
<ul>
  <li><a href="#indexOf">String indexOf()</a></li>
  <li><a href="#lastIndexOf">String lastIndexOf()</a></li>
  <li><a href="#startsWith">String startsWith()</a></li>
  <li><a href="#endsWith">String endsWith()</a></li>
  <li><a href="#search">String search()</a></li>
  <li><a href="#match">String match()</a></li>
  <li><a href="#includes">String includes()</a></li>
</ul>
<h1>indexOf()</h1>
The <b>indexOf()</b> method returns the index of (the position of) the first occurrence of a specified text in a string:
<pre>
let str = "Please locate where 'locate' occurs!";
str.indexOf("locate");
</pre>
<h1>lastIndexOf()</h1>
The <b>lastIndexOf()</b> method returns the index of the last occurrence of a specified text in a string:
<pre>
let str = "Please locate where 'locate' occurs!";
str.lastIndexOf("locate");
</pre>
Both <b>indexOf()</b>, and <b>lastIndexOf()</b> return -1 if the text is not found:
<pre>
let str = "Please locate where 'locate' occurs!";
str.lastIndexOf("John");
</pre>
Both methods accept a second parameter as the starting position for the search:
<pre>
let str = "Please locate where 'locate' occurs!";
str.indexOf("locate", 15);
</pre>
The <b>lastIndexOf()</b> methods searches backwards (from the end to the beginning), meaning: if the second parameter is 15, the search starts at position 15, and searches to the beginning of the string.
<pre>
let str = "Please locate where 'locate' occurs!";
str.lastIndexOf("locate", 15);
</pre>
<h1>startsWith()</h1>
The <b>startsWith()</b> method returns true if a string begins with a specified value, otherwise false:
<pre>
let text = "Hello world, welcome to the universe.";
text.startsWith("Hello");
</pre>
<h1>endsWith()</h1>
The endsWith() method returns true if a string ends with a specified value, otherwise false:
<pre>
let text = "John Doe";
text.endsWith("Doe");
</pre>
<h1>search()</h1>
The <b>search()</b> method searches a string for a specified value and returns the position of the match:
<pre>
let str = "Please locate where 'locate' occurs!";
str.search("locate");
</pre>
<h2>Did You Notice?</h2>
The two methods, <b>indexOf()</b> and <b>search()</b>, are equal?
<br>
They accept the same arguments (parameters), and return the same value?
<br>
The two methods are NOT equal. These are the differences:
<ul>
  <li>The search() method cannot take a second start position argument.</li>
  <li>The indexOf() method cannot take powerful search values. (regular expressions)</li>
</ul>
<h1>match()</h1>
The match() method searches a string for a match against a regular expression, and returns the matches, as an Array object.
<br>
Search a string for "ain":
<pre>
let text = "The rain in SPAIN stays mainly in the plain"; 
text.match(/ain/g);
</pre>
<h1>includes()</h1>
The <b>includes()</b> method returns true if a string contains a specified value.
<pre>
let text = "Hello world, welcome to the universe.";
text.includes("world");
</pre>
