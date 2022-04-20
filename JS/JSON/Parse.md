<a href="/JS/JSON/Data-Types.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/JSON/Strings.md">Next &gt;</a>
<hr>
A common use of JSON is to exchange data to/from a web server.
<br>
When receiving data from a web server, the data is always a string.
<br>
Parse the data with <b>JSON.parse()</b>, and the data becomes a JavaScript object.
<h1>Examples</h1>
Imagine we received this text from a web server:
<pre>'{"name":"John", "age":30, "city":"New York"}'</pre>
Use the JavaScript function <b>JSON.parse()</b> to convert text into a JavaScript object:
<pre>const obj = JSON.parse('{"name":"John", "age":30, "city":"New York"}');</pre>
Use the JavaScript object in your page:
<pre>
&lt;p id="demo"&gt;&lt;/p&gt;
&lt;script&gt;document.getElementById("demo").innerHTML = obj.name;&lt;/script&gt;
</pre>
<h1>Array as JSON</h1>
When using the JSON.parse() on a JSON derived from an array, the method will return a JavaScript array, instead of a JavaScript object.
<pre>
const text = '["Ford", "BMW", "Audi", "Fiat"]';
const myArr = JSON.parse(text);
</pre>
<h1>Parsing Dates</h1>
Date objects are not allowed in JSON.
<br>
If you need to include a date, write it as a string.
<br>
You can convert it back into a date object later:
<pre>
const text = '{"name":"John", "birth":"1986-12-14", "city":"New York"}';
const obj = JSON.parse(text);
obj.birth = new Date(obj.birth);
document.getElementById("demo").innerHTML = obj.name + ", " + obj.birth;
</pre>
Or, you can use the second parameter, of the JSON.parse() function, called reviver.
<br>
The reviver parameter is a function that checks each property, before returning the value.
<pre>
const text = '{"name":"John", "birth":"1986-12-14", "city":"New York"}';
const obj = JSON.parse(text, function (key, value) {
  if (key == "birth") {
    return new Date(value);
  } else {
    return value;
  }
});
document.getElementById("demo").innerHTML = obj.name + ", " + obj.birth;
</pre>
<h1>Parsing Functions</h1>
Functions are not allowed in JSON.
<br>
If you need to include a function, write it as a string.
<br>
You can convert it back into a function later:
<pre>
const text = '{"name":"John", "age":"function () {return 30;}", "city":"New York"}';
const obj = JSON.parse(text);
obj.age = eval("(" + obj.age + ")");
document.getElementById("demo").innerHTML = obj.name + ", " + obj.age();
</pre>
