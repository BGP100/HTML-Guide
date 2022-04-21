<a href="/JS/JSON/HTML.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="https://bledy-guides.repl.co">Next &gt;</a>
<hr>
JSONP is a method for sending JSON data without worrying about cross-domain issues.
<br>
JSONP does not use the <b>XMLHttpRequest</b> object.
<br>
JSONP uses the <b>&lt;script&gt;</b> tag instead.
<h1>Introduction</h1>
JSONP stands for JSON with Padding.
<br>
Requesting a file from another domain can cause problems, due to cross-domain policy.
<br>
Requesting an external script from another domain does not have this problem.
<br>
JSONP uses this advantage, and request files using the script tag instead of the <b>XMLHttpRequest</b> object.
<pre>&lt;script src="demo_jsonp.php"&gt;</pre>
<h1>Server File</h1>
The file on the server wraps the result inside a function call:
<pre>
&lt;?php
$myJSON = '{ "name":"John", "age":30, "city":"New York" }';
echo "myFunc(".$myJSON.");";
?&gt;
</pre>
The result returns a call to a function named "myFunc" with the JSON data as a parameter.
<br>
Make sure that the function exists on the client.
<h1>The JavaScript function</h1>
The function named "myFunc" is located on the client, and ready to handle JSON data:
<pre>
function myFunc(myObj) {
  document.getElementById("demo").innerHTML = myObj.name;
}
</pre>
<h1>Creating a Dynamic Script Tag</h1>
The example above will execute the "myFunc" function when the page is loading, based on where you put the script tag, which is not very satisfying.
<br>
The script tag should only be created when needed:
<pre>
function clickButton() {
  let s = document.createElement("script");
  s.src = "demo_jsonp.php";
  document.body.appendChild(s);
}
</pre>
<h1>Dynamic Result</h1>
The examples above are still very static.
<br>
Make the example dynamic by sending JSON to the php file, and let the php file return a JSON object based on the information it gets.
<pre>
&lt;?php
header("Content-Type: application/json; charset=UTF-8");
$obj = json_decode($_GET["x"], false);
$conn = new mysqli("myServer", "myUser", "myPassword", "Northwind");
$result = $conn-&gt;query("SELECT name FROM ".$obj-&gt;$table." LIMIT ".$obj-&gt;$limit);
$outp = array();
$outp = $result-&gt;fetch_all(MYSQLI_ASSOC);
echo "myFunc('.json_encode($outp).')";
?&gt;
</pre>
<b>Explained:</b>
<ul>
  <li>Convert the request into an object, using the PHP function json_decode().</li>
  <li>Access the database, and fill an array with the requested data.</li>
  <li>Add the array to an object.</li>
  <li>Convert the array into JSON using the json_encode() function.</li>
  <li>Wrap "myFunc()" around the return object.</li>
</ul>
<pre>
const obj = { table: "products", limit: 10 };
let s = document.createElement("script");
s.src = "jsonp_demo_db.php?x=" + JSON.stringify(obj);
document.body.appendChild(s);
function myFunc(myObj) {
  let txt = "";
  for (let x in myObj) {
    txt += myObj[x].name + "&lt;br&gt;";
  }
  document.getElementById("demo").innerHTML = txt;
}
</pre>
<h1>Callback Function</h1>
When you have no control over the server file, how do you get the server file to call the correct function?
<br>
Sometimes the server file offers a callback function as a parameter:
<pre>
let s = document.createElement("script");
s.src = "jsonp_demo_db.php?callback=myDisplayFunction";
document.body.appendChild(s);
</pre>
