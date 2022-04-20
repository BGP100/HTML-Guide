<a href="/JS/JSON/Introduction.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/JSON/XML.md">Next &gt;</a>
<hr>
The JSON syntax is a subset of the JavaScript syntax.
<h1>Rules</h1>
JSON syntax is derived from JavaScript object notation syntax:
<ul>
  <li>Data is in name/value pairs</li>
  <li>Data is separated by commas</li>
  <li>Curly braces hold objects</li>
  <li>Square brackets hold arrays</li>
</ul>
<h1>A Name and a Value</h1>
JSON data is written as name/value pairs (aka key/value pairs).
<br>
A name/value pair consists of a field name (in double quotes), followed by a colon, followed by a value:
<pre>"name":"John"</pre>
JSON names require double quotes.
<h1>Evaluates to JavaScript Objects</h1>
The JSON format is almost identical to JavaScript objects.
<br>
In JSON, keys must be strings, written with double quotes:
<pre>{"name":"John"}</pre>
In JavaScript, keys can be strings, numbers, or identifier names:
<pre>{name:"John"}</pre>
<h1>Values</h1>
In JSON, values must be one of the following data types:
<ul>
  <li>a string</li>
  <li>a number</li>
  <li>an object</li>
  <li>an array</li>
  <li>a boolean</li>
  <li>null</li>
</ul>
In JavaScript values can be all of the above, plus any other valid JavaScript expression, including:
<ul>
  <li>a function</li>
  <li>a date</li>
  <li>undefined</li>
</ul>
In JSON, string values must be written with double quotes:
<pre>{"name":"John"}</pre>
In JavaScript, you can write string values with double or single quotes:
<pre>{name:'John'}</pre>
<h1>JavaScript Objects</h1>
Because JSON syntax is derived from JavaScript object notation, very little extra software is needed to work with JSON within JavaScript.
<br>
With JavaScript you can create an object and assign data to it, like this:
<pre>person = {name:"John", age:31, city:"New York"};</pre>
You can access a JavaScript object like this:
<pre>
// returns John
person.name;
</pre>
It can also be accessed like this:
<pre>
// returns John
person["name"];
</pre>
Data can be modified like this:
<pre>person.name = "Gilbert";</pre>
It can also be modified like this:
<pre>person["name"] = "Gilbert";</pre>
You will learn how to convert JavaScript objects into JSON later in this tutorial.
<h1>JavaScript Arrays as JSON</h1>
The same way JavaScript objects can be written as JSON, JavaScript arrays can also be written as JSON.
<br>
You will learn more about objects and arrays later in this tutorial.
<h1>Files</h1>
The file type for JSON files is ".json"
<br>
The MIME type for JSON text is "application/json"
