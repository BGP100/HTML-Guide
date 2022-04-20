<a href="/JS/JSON/Parse.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/JSON/Objects.md">Next &gt;</a>
<hr>
A common use of JSON is to exchange data to/from a web server.
<br>
When sending data to a web server, the data has to be a string.
<br>
Convert a JavaScript object into a string with JSON.stringify().
<h1>Stringify a JavaScript Object</h1>
Imagine we have this object in JavaScript:
<pre>const obj = {name: "John", age: 30, city: "New York"};</pre>
Use the JavaScript function JSON.stringify() to convert it into a string.
<pre>const myJSON = JSON.stringify(obj);</pre>
myJSON is now a string, and ready to be sent to a server:
<pre>
const obj = {name: "John", age: 30, city: "New York"};
const myJSON = JSON.stringify(obj);
</pre>
You will learn how to send JSON to a server in the next chapters.
<h1>Stringify a JavaScript Array</h1>
It is also possible to stringify JavaScript arrays:
<br>
Imagine we have this array in JavaScript:
<pre>const arr = ["John", "Peter", "Sally", "Jane"];</pre>
Use the JavaScript function JSON.stringify() to convert it into a string.
<pre>const myJSON = JSON.stringify(arr);</pre>
<h1>Storing Data</h1>
When storing data, the data has to be a certain format, and regardless of where you choose to store it, text is always one of the legal formats.
<br>
JSON makes it possible to store JavaScript objects as text.
<pre>
// Storing data:
const myObj = {name: "John", age: 31, city: "New York"};
const myJSON = JSON.stringify(myObj);
localStorage.setItem("testJSON", myJSON);
// Retrieving data:
let text = localStorage.getItem("testJSON");
let obj = JSON.parse(text);
document.getElementById("demo").innerHTML = obj.name;
</pre>
<h1>Stringify Dates</h1>
In JSON, date objects are not allowed. The JSON.stringify() function will convert any dates into strings.
<pre>
const obj = {name: "John", today: new Date(), city : "New York"};
const myJSON = JSON.stringify(obj);
</pre>
You can convert the string back into a date object at the receiver.
<h1>Stringify Functions</h1>
In JSON, functions are not allowed as object values.
<br>
The JSON.stringify() function will remove any functions from a JavaScript object, both the key and the value:
<pre>
const obj = {name: "John", age: function () {return 30;}, city: "New York"};
const myJSON = JSON.stringify(obj);
</pre>
This can be omitted if you convert your functions into strings before running the JSON.stringify() function.
<pre>
const obj = {name: "John", age: function () {return 30;}, city: "New York"};
obj.age = obj.age.toString();
const myJSON = JSON.stringify(obj);
</pre>
If you send functions using JSON, the functions will lose their scope, and the receiver would have to use eval() to convert them back into functions.
