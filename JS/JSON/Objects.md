<a href="/JS/JSON/Strings.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/JSON/Arrays.md">Next &gt;</a>
<hr>
This is a JSON string:
<pre>'{"name":"John", "age":30, "car":null}'</pre>
Inside the JSON string there is a JSON object literal:
<pre>{"name":"John", "age":30, "car":null}</pre>
JSON object literals are surrounded by curly braces {}.
<br>
JSON object literals contains key/value pairs.
<br>
Keys and values are separated by a colon.
<br>
Keys must be strings, and values must be a valid JSON data type:
<ul>
  <li>string</li>
  <li>number</li>
  <li>object</li>
  <li>array</li>
  <li>boolean</li>
  <li>null</li>
</ul>
Each key/value pair is separated by a comma.
<h1>JavaScript Objects</h1>
You can create a JavaScript object from a JSON object literal:
<pre>myObj = {"name":"John", "age":30, "car":null};</pre>
Normally, you create a JavaScript object by parsing a JSON string:
<pre>
myJSON = '{"name":"John", "age":30, "car":null}';
myObj = JSON.parse(myJSON);
</pre>
Accessing Object Values
You can access object values by using dot (.) notation:
<pre>
const myJSON = '{"name":"John", "age":30, "car":null}';
const myObj = JSON.parse(myJSON);
x = myObj.name;
</pre>
You can also access object values by using bracket ([]) notation:
<pre>
const myJSON = '{"name":"John", "age":30, "car":null}';
const myObj = JSON.parse(myJSON);
x = myObj["name"];
</pre>
<h1>Looping an Object</h1>
You can loop through object properties with a for-in loop:
<pre>
const myJSON = '{"name":"John", "age":30, "car":null}';
const myObj = JSON.parse(myJSON);
let text = "";
for (const x in myObj) {
  text += x + ", ";
}
</pre>
In a for-in loop, use the bracket notation to access the property values:
<pre>
const myJSON = '{"name":"John", "age":30, "car":null}';
const myObj = JSON.parse(myJSON);
let text = "";
for (const x in myObj) {
  text += myObj[x] + ", ";
}
</pre>
