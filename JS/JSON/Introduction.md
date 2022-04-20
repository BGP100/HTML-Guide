<a href="/JS/JSON/Main.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/JSON/Syntax.md">Next &gt;</a>
<hr>
JSON stands for <b>J</b>ava<b>S</b>cript <b>O</b>bject <b>N</b>otation
<br>
JSON is a text format for storing and transporting data
<br>
JSON is "self-describing" and easy to understand
<h1>Example</h1>
This example is a JSON string:
<pre>'{"name":"John", "age":30, "car":null}'</pre>
It defines an object with 3 properties:
<ul>
  <li>name</li>
  <li>age</li>
  <li>car</li>
</ul>
Each property has a value.
<br>
If you parse the JSON string with a JavaScript program, you can access the data as an object:
<pre>
let personName = obj.name;
let personAge = obj.age;
</pre>
<h1>What is JSON?</h1>
<ul>
  <li>JSON stands for JavaScript Object Notation</li>
  <li>JSON is a lightweight data-interchange format</li>
  <li>JSON is plain text written in JavaScript object notation</li>
  <li>JSON is used to send data between computers</li>
  <li>JSON is language independent <code>*</code></li>
</ul>
<code>*</code> The JSON syntax is derived from JavaScript object notation, but the JSON format is text only.
<br>
<code>*</code> Code for reading and generating JSON exists in many programming languages.
<br>
The JSON format was originally specified by Douglas Crockford.
<h1>Why Use JSON?</h1>
The JSON format is syntactically similar to the code for creating JavaScript objects. Because of this, a JavaScript program can easily convert JSON data into JavaScript objects.
<br>
Since the format is text only, JSON data can easily be sent between computers, and used by any programming language.
<br>
JavaScript has a built in function for converting JSON strings into JavaScript objects:
<br>
<b>JSON.parse()</b>
<br>
JavaScript also has a built in function for converting an object into a JSON string:
<br>
<b>JSON.stringify()</b>
<h1>Storing Data</h1>
When storing data, the data has to be a certain format, and regardless of where you choose to store it, text is always one of the legal formats.
<br>
JSON makes it possible to store JavaScript objects as text.
