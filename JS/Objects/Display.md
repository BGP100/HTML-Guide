<a href="/JS/Objects/Methods.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Objects/Accessors.md">Next &gt;</a>
<hr>
Displaying a JavaScript object will output <code>[object Object]</code>.
<pre>
const person = {
  name: "John",
  age: 30,
  city: "New York"
};
document.getElementById("demo").innerHTML = person;
</pre>
Some common solutions to display JavaScript objects are:
<ul>
  <li>Displaying the Object Properties by name</li>
  <li>Displaying the Object Properties in a Loop</li>
  <li>Displaying the Object using Object.values()</li>
  <li>Displaying the Object using JSON.stringify()</li>
</ul>
<h1>Displaying Object Properties</h1>
The properties of an object can be displayed as a string:
<pre>
const person = {
  name: "John",
  age: 30,
  city: "New York"
};
document.getElementById("demo").innerHTML =
person.name + "," + person.age + "," + person.city;
</pre>
<h1>Displaying the Object in a Loop</h1>
The properties of an object can be collected in a loop:
<pre>
const person = {
  name: "John",
  age: 30,
  city: "New York"
};
let txt = "";
for (let x in person) {
txt += person[x] + " ";
};
document.getElementById("demo").innerHTML = txt;
</pre>
You must use person[x] in the loop.
<br>
person.x will not work (Because x is a variable).
<h1>Using Object.values()</h1>
Any JavaScript object can be converted to an array using Object.values():
<pre>
const person = {
  name: "John",
  age: 30,
  city: "New York"
};
const myArray = Object.values(person);
</pre>
myArray is now a JavaScript array, ready to be displayed:
<pre>
const person = {
  name: "John",
  age: 30,
  city: "New York"
};
const myArray = Object.values(person);
document.getElementById("demo").innerHTML = myArray;
</pre>
<h1>Using JSON.stringify()</h1>
Any JavaScript object can be stringified (converted to a string) with the JavaScript function JSON.stringify():
<pre>
const person = {
  name: "John",
  age: 30,
  city: "New York"
};
let myString = JSON.stringify(person);
</pre>
myString is now a JavaScript string, ready to be displayed:
<pre>
const person = {
  name: "John",
  age: 30,
  city: "New York"
};
let myString = JSON.stringify(person);
document.getElementById("demo").innerHTML = myString;
</pre>
<h1>Stringify Dates</h1>
JSON.stringify converts dates into strings:
<pre>
const person = {
  name: "John",
  today: new Date()
};
let myString = JSON.stringify(person);
document.getElementById("demo").innerHTML = myString;
</pre>
<h1>Stringify Functions</h1>
JSON.stringify will not stringify functions:
<pre>
const person = {
  name: "John",
  age: function () {return 30;}
};
let myString = JSON.stringify(person);
document.getElementById("demo").innerHTML = myString;
</pre>
This can be "fixed" if you convert the functions into strings before stringifying.
<pre>
const person = {
  name: "John",
  age: function () {return 30;}
};
person.age = person.age.toString();
let myString = JSON.stringify(person);
document.getElementById("demo").innerHTML = myString;
</pre>
<h1>Stringify Arrays</h1>
It is also possible to stringify JavaScript arrays:
<pre>
const arr = ["John", "Peter", "Sally", "Jane"];
let myString = JSON.stringify(arr);
document.getElementById("demo").innerHTML = myString;
</pre>
