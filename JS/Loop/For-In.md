The JavaScript <b>for in</b> statement loops through the properties of an Object:
<br>
<b>Syntax:</b>
<pre>
for (key in object) {
  // code block to be executed
}
</pre>
<pre>
const person = {fname:"John", lname:"Doe", age:25};
let text = "";
for (let x in person) {
  text += person[x];
}
</pre>
Example Explained:
<ul>
  <li>The for in loop iterates over a person object</li>
  <li>Each iteration returns a key (x)</li>
  <li>The key is used to access the value of the key</li>
  <li>The value of the key is person[x]</li>
</ul>
<h1>For In Over Arrays</h1>
The JavaScript for in statement can also loop over the properties of an Array:
<pre>
for (variable in array) {
  code
}
</pre>
<pre>
const numbers = [45, 4, 9, 16, 25];
let txt = "";
for (let x in numbers) {
  txt += numbers[x];
}
</pre>
<h1>Array.forEach()</h1>
The <b>forEach()</b> method calls a function (a callback function) once for each array element.
<pre>
const numbers = [45, 4, 9, 16, 25];
let txt = "";
numbers.forEach(myFunction);
function myFunction(value, index, array) {
  txt += value;
}
</pre>
Note that the function takes 3 arguments:
<ul>
  <li>The item value</li>
  <li>The item index</li>
  <li>The array itself</li>
</ul>
The example above uses only the value parameter. It can be rewritten to:
<pre>
const numbers = [45, 4, 9, 16, 25];
let txt = "";
numbers.forEach(myFunction);
function myFunction(value) {
  txt += value;
}
</pre>
