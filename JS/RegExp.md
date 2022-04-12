<a href="/JS/Type-Conversion.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Errors.md">Next &gt;</a>
<hr>
A regular expression is a sequence of characters that forms a search pattern.
<br>
The search pattern can be used for text search and text replace operations.
<h1>What is it?</h1>
A regular expression is a sequence of characters that forms a search pattern.
<br>
When you search for data in a text, you can use this search pattern to describe what you are searching for.
<br>
A regular expression can be a single character, or a more complicated pattern.
<br>
Regular expressions can be used to perform all types of text search and text replace operations.
<br>
<b>Syntax:</b>
<pre>/pattern/modifiers;</pre>
<hr>
<pre>/bledygames/i;</pre>
Explained:
<br>
<b>/bledygames/i</b>  is a regular expression.
<br>
<b>bledygames</b>  is a pattern (to be used in a search).
<br>
<b>i</b>  is a modifier (modifies the search to be case-insensitive).
<h1>Using String Methods</h1>
In JavaScript, regular expressions are often used with the two string methods: <b>search()</b> and <b>replace()</b>.
<br>
The <b>search()</b> method uses an expression to search for a match, and returns the position of the match.
<br>
The <b>replace()</b> method returns a modified string where the pattern is replaced.
<h1>Using String search() With a String</h1>
The search() method searches a string for a specified value and returns the position of the match:
<br>
Use a string to do a search for "BledyGames" in a string:
<pre>
let text = "Visit BledyGames!";
let n = text.search("BledyGames");
</pre>
<h1>Using String search() With a Regular Expression</h1>
Use a regular expression to do a case-insensitive search for "BledyGames" in a string:
<pre>
let text = "Visit BledyGames";
let n = text.search(/BledyGames/i);
</pre>
<h1>Using String replace() With a String</h1>
The replace() method replaces a specified value with another value in a string:
<pre>
let text = "Visit Microsoft!";
let result = text.replace("Microsoft", "W3Schools");
</pre>
<h1>Use String replace() With a Regular Expression</h1>
Use a case insensitive regular expression to replace Microsoft with BledyGames in a string:
let text = "Visit Microsoft!";
let result = text.replace(/microsoft/i, "BledyGames");
</pre>
<h1>Using the RegExp Object</h1>
In JavaScript, the RegExp object is a regular expression object with predefined properties and methods.
