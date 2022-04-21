<a href="/JS/JSON/Server.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/JSON/HTML.md">Next &gt;</a>
<hr>
A common use of JSON is to read data from a web server, and display the data in a web page.
<br>
This chapter will teach you how to exchange JSON data between the client and a PHP server.
<h1>The PHP File</h1>
PHP has some built-in functions to handle JSON.
<br>
Objects in PHP can be converted into JSON by using the PHP function json_encode():
<pre>
&lt;?php
$myObj-&gt;name = "John";
$myObj-&gt;age = 30;
$myObj-&gt;city = "New York";
$myJSON = json_encode($myObj);
echo $myJSON;
?&gt;
</pre>
<h1>The Client JavaScript</h1>
Here is a JavaScript on the client, using an AJAX call to request the PHP file from the example above:
<br>
Use JSON.parse() to convert the result into a JavaScript object:
<pre>
const xmlhttp = new XMLHttpRequest();
xmlhttp.onload = function() {
  const myObj = JSON.parse(this.responseText);
  document.getElementById("demo").innerHTML = myObj.name;
}
xmlhttp.open("GET", "demo_file.php");
xmlhttp.send();
</pre>
<h1>Array</h1>
Arrays in PHP will also be converted into JSON when using the PHP function json_encode():
<pre>
&lt;?php
$myArr = array("John", "Mary", "Peter", "Sally");
$myJSON = json_encode($myArr);
echo $myJSON;
?&gt;
</pre>
<h1>The Client JavaScript</h1>
Here is a JavaScript on the client, using an AJAX call to request the PHP file from the array example above:
<pre>
var xmlhttp = new XMLHttpRequest();
xmlhttp.onload = function() {
  const myObj = JSON.parse(this.responseText);
  document.getElementById("demo").innerHTML = myObj[2];
}
xmlhttp.open("GET", "demo_file_array.php", true);
xmlhttp.send();
</pre>
<h1>Database</h1>
PHP is a server side programming language, and can be used to access a database.
<br>
Imagine you have a database on your server, and you want to send a request to it from the client where you ask for the 10 first rows in a table called "customers".
<br>
On the client, make a JSON object that describes the numbers of rows you want to return.
<br>
Before you send the request to the server, convert the JSON object into a string and send it as a parameter to the url of the PHP page:
<pre>
const limit = {"limit":10};
const dbParam = JSON.stringify(limit);
xmlhttp = new XMLHttpRequest();
xmlhttp.onload = function() {
  document.getElementById("demo").innerHTML = this.responseText;
}
xmlhttp.open("GET","json_demo_db.php?x=" + dbParam);
xmlhttp.send();
</pre>
<b>Explained:</b>
<ul>
  <li>Define an object containing a "limit" property and value.</li>
  <li>Convert the object into a JSON string.</li>
  <li>Send a request to the PHP file, with the JSON string as a parameter.</li>
  <li>Wait until the request returns with the result (as JSON)</li>
  <li>Display the result received from the PHP file.</li>
</ul>
Take a look at the PHP file:
<pre>
&lt;?php
header("Content-Type: application/json; charset=UTF-8");
$obj = json_decode($_GET["x"], false);
$conn = new mysqli("myServer", "myUser", "myPassword", "Northwind");
$stmt = $conn->prepare("SELECT name FROM customers LIMIT ?");
$stmt->bind_param("s", $obj->limit);
$stmt->execute();
$result = $stmt->get_result();
$outp = $result->fetch_all(MYSQLI_ASSOC);
echo json_encode($outp);
?&gt;
</pre>
<b>Explained:</b>
<ul>
  <li>Convert the request into an object, using the PHP function <b>json_decode()</b>.</li>
  <li>Access the database, and fill an array with the requested data.</li>
  <li>Add the array to an object, and return the object as JSON using the <b>json_encode()</b> function.</li>
</ul>
<h1>Use the Data</h1>
<pre>
xmlhttp.onload = function() {
  const myObj = JSON.parse(this.responseText);
  let text = "";
  for (let x in myObj) {
    text += myObj[x].name + "&lt;br&gt;";
  }
  document.getElementById("demo").innerHTML = text;
}
</pre>
<h1>Method = POST</h1>
When sending data to the server, it is often best to use the HTTP POST method.
<br>
To send AJAX requests using the POST method, specify the method, and the correct header.
<br>
The data sent to the server must now be an argument to the send() method:
<pre>
const dbParam = JSON.stringify({"limit":10});
const xmlhttp = new XMLHttpRequest();
xmlhttp.onload = function() {
  const myObj = JSON.parse(this.responseText);
  let text ="";
  for (let x in myObj) {
    text += myObj[x].name + "&lt;br&gt;";
  }
  document.getElementById("demo").innerHTML = text;
}
xmlhttp.open("POST", "json_demo_db_post.php");
xmlhttp.setRequestHeader("Content-type", "application/x-www-form-urlencoded");
xmlhttp.send("x=" + dbParam);
</pre>
The only difference in the PHP file is the method for getting the transferred data.
<pre>
&lt;?php
header("Content-Type: application/json; charset=UTF-8");
$obj = json_decode($_POST["x"], false);
$conn = new mysqli("myServer", "myUser", "myPassword", "Northwind");
$stmt = $conn->prepare("SELECT name FROM customers LIMIT ?");
$stmt->bind_param("s", $obj->limit);
$stmt->execute();
$result = $stmt->get_result();
$outp = $result->fetch_all(MYSQLI_ASSOC);
echo json_encode($outp);
?&gt;
</pre>
