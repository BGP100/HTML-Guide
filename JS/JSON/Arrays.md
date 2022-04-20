<a href="/JS/JSON/Objects.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/JSON/Server.md">Next &gt;</a>
<hr>
This is a JSON string:
<pre>'["Ford", "BMW", "Fiat"]'</pre>
Inside the JSON string there is a JSON array literal:
<pre>["Ford", "BMW", "Fiat"]</pre>
Arrays in JSON are almost the same as arrays in JavaScript.
<br>
In JSON, array values must be of type string, number, object, array, boolean or null.
<br>
In JavaScript, array values can be all of the above, plus any other valid JavaScript expression, including functions, dates, and undefined.
<h1>JavaScript Arrays</h1
You can create a JavaScript array from a literal:
<pre>myArray = ["Ford", "BMW", "Fiat"];</pre>
You can create a JavaScript array by parsing a JSON string:
<pre>
myJSON = '["Ford", "BMW", "Fiat"]';
myArray = JSON.Parse(myJSON);
</pre>
<h1>Accessing Array Values</h1>
You access array values by index:
<pre>myArray[0];</pre>
<h1>Arrays in Objects</h1>
Objects can contain arrays:
<pre>
{
"name":"John",
"age":30,
"cars":["Ford", "BMW", "Fiat"]
}
</pre>
You access array values by index:
<pre>myObj.cars[0];</pre>
<h1>Looping Through an Array</h1>
You can access array values by using a <b>for..in</b> loop:
<pre>
for (let i in myObj.cars) {
  x += myObj.cars[i];
}
</pre>
Or you can use a <b>for</b> loop:
<pre>
for (let i = 0; i &lt; myObj.cars.length; i++) {
  x += myObj.cars[i];
}
</pre>
