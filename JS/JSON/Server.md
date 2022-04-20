<a href="/JS/JSON/Arrays.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/JSON/PHP.md">Next &gt;</a>
<hr>
A common use of JSON is to exchange data to/from a web server.
<br>
When receiving data from a web server, the data is always a string.
<br>
Parse the data with JSON.parse(), and the data becomes a JavaScript object.
<h1>Sending Data</h1>
If you have data stored in a JavaScript object, you can convert the object into JSON, and send it to a server:
<pre>
const myObj = {name: "John", age: 31, city: "New York"};
const myJSON = JSON.stringify(myObj);
window.location = "demo_json.php?x=" + myJSON;
</pre>
<h1>Receiving Data</h1>
If you receive data in JSON format, you can easily convert it into a JavaScript object:
<pre>
const myJSON = '{"name":"John", "age":31, "city":"New York"}';
const myObj = JSON.parse(myJSON);
document.getElementById("demo").innerHTML = myObj.name;
</pre>
<h1>JSON From a Server</h1>
You can request JSON from the server by using an AJAX request
<br>
As long as the response from the server is written in JSON format, you can parse the string into a JavaScript object.
<br>
Use the XMLHttpRequest to get data from the server:
<pre>
const xmlhttp = new XMLHttpRequest();
xmlhttp.onload = function() {
  const myObj = JSON.parse(this.responseText);
  document.getElementById("demo").innerHTML = myObj.name;
};
xmlhttp.open("GET", "json_demo.txt");
xmlhttp.send();
</pre>
<h1>Array as JSON</h1>
When using the JSON.parse() on JSON derived from an array, the method will return a JavaScript array, instead of a JavaScript object.
<br>
JSON returned from a server as an array:
<pre>
const xmlhttp = new XMLHttpRequest();
xmlhttp.onload = function() {
  const myArr = JSON.parse(this.responseText);
  document.getElementById("demo").innerHTML = myArr[0];
  }
}
xmlhttp.open("GET", "json_demo_array.txt", true);
xmlhttp.send();
</pre>
