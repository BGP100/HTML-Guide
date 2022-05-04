<a href="https://bledy-guides.repl.co/#json">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/JSON/Introduction.md">Next &gt;</a>
<hr>
JSON is a format for storing and transporting data.
<br>
JSON is often used when data is sent from a server to a web page.
<ul>
  <li>JSON stands for <b>J</b>ava<b>S</b>cript <b>O</b>bject <b>N</b>otation.</li>
  <li>JSON is a lightweight data interchange format.</li>
  <li>JSON is language independent <code>*</code>.</li>
  <li>JSON is "self-describing" and easy to understand.</li>
</ul>
<code>*</code> The JSON syntax is derived from JavaScript object notation syntax, but the JSON format is text only. Code for reading and generating JSON data can be written in any programming language.
<h1>Example</h1>
This JSON syntax defines an employees object: an array of 3 employee records (objects):
<pre>
{
"employees":[
  {"firstName":"John", "lastName":"Doe"},
  {"firstName":"Anna", "lastName":"Smith"},
  {"firstName":"Peter", "lastName":"Jones"}
]
}
</pre>
<h1>JSON Format Evaluates to JavaScript Objects</h1>
The JSON format is syntactically identical to the code for creating JavaScript objects.
<br>
Because of this similarity, a JavaScript program can easily convert JSON data into native JavaScript objects.
<h1>JSON Syntax Rules</h1>
<ul>
  <li>Data is in name/value pairs</li>
  <li>Data is separated by commas</li>
  <li>Curly braces hold objects</li>
  <li>Square brackets hold arrays</li>
</ul>
<h1>A Name and a Value</h1>
JSON data is written as name/value pairs, just like JavaScript object properties.
<br>
A name/value pair consists of a field name (in double quotes), followed by a colon, followed by a value:
<pre>"firstName":"John"</pre>
<h1>Objects</h1>
JSON objects are written inside curly braces.
<br>
Just like in JavaScript, objects can contain multiple name/value pairs:
<pre>{"firstName":"John", "lastName":"Doe"}</pre>
<h1>Arrays</h1>
JSON arrays are written inside square brackets.
<br>
Just like in JavaScript, an array can contain objects:
<pre>
"employees":[
  {"firstName":"John", "lastName":"Doe"},
  {"firstName":"Anna", "lastName":"Smith"},
  {"firstName":"Peter", "lastName":"Jones"}
]
</pre>
In the example above, the object "employees" is an array. It contains three objects.
<br>
Each object is a record of a person (with a first name and a last name).
<h1>Converting a JSON Text to a JavaScript Object</h1>
A common use of JSON is to read data from a web server, and display the data in a web page.
<br>
For simplicity, this can be demonstrated using a string as input.
<br>
First, create a JavaScript string containing JSON syntax:
<pre>
let text = '{ "employees" : [' +
'{ "firstName":"John" , "lastName":"Doe" },' +
'{ "firstName":"Anna" , "lastName":"Smith" },' +
'{ "firstName":"Peter" , "lastName":"Jones" } ]}';
</pre>
Then, use the JavaScript built-in function JSON.parse() to convert the string into a JavaScript object:
<pre>const obj = JSON.parse(text);</pre>
Finally, use the new JavaScript object in your page:
<pre>
&lt;p id="demo"&gt;d&lt;/p&gt;d
&lt;script&gt;d
document.getElementById("demo").innerHTML =
obj.employees[1].firstName + " " + obj.employees[1].lastName;
&lt;/script&gt;
</pre>
