<a href="/JS/JSON/PHP.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/JSON/JSONP.md">Next &gt;</a>
<p></p>
<a href="/HTML/Home.md">HTML Guide.</a>
<hr>
JSON can very easily be translated into JavaScript.
<br>
JavaScript can be used to make HTML in your web pages.
<h1>Table</h1>
Make an HTML table with data received as JSON:
<pre>
const dbParam = JSON.stringify({table:"customers",limit:20});
const xmlhttp = new XMLHttpRequest();
xmlhttp.onload = function() {
  myObj = JSON.parse(this.responseText);
  let text = &lt;table border='1'>&gt;"
  for (let x in myObj) {
    text += "&lt;tr>&gt;&lt;td>&gt;" + myObj[x].name + "&lt;/td>&gt;&lt;/tr>&gt;";
  }
  text += "&lt;/table>&gt;"
  document.getElementById("demo").innerHTML = text;
}
xmlhttp.open("POST", "json_demo_html_table.php");
xmlhttp.setRequestHeader("Content-type", "application/x-www-form-urlencoded");
xmlhttp.send("x=" + dbParam);
</pre>
<h1>Dynamic Table</h1>
Make the HTML table based on the value of a drop down menu.
<pre>
&lt;select id="myselect" onchange="change_myselect(this.value)"&gt;
  &lt;option value=""&gt;Choose an option:&lt;/option&gt;
  &lt;option value="customers"&gt;Customers&lt;/option&gt;
  &lt;option value="products"&gt;Products&lt;/option&gt;
  &lt;option value="suppliers"&gt;Suppliers&lt;/option&gt;
&lt;/select&gt;
&lt;script&gt;
function change_myselect(sel) {
  const dbParam = JSON.stringify({table:sel,limit:20});
  const xmlhttp = new XMLHttpRequest();
  xmlhttp.onload = function() {
    const myObj = JSON.parse(this.responseText);
    let text = "&lt;table border='1'&gt;"
    for (let x in myObj) {
      text += "&lt;tr&gt;&lt;td&gt;" + myObj[x].name + "&lt;/td&gt;&lt;/tr&gt;";
    }
    text += "&lt;/table&gt;"
    document.getElementById("demo").innerHTML = text;
  }
  xmlhttp.open("POST", "json_demo_html_table.php");
  xmlhttp.setRequestHeader("Content-type", "application/x-www-form-urlencoded");
  xmlhttp.send("x=" + dbParam);
}
&lt;/script&gt;
</pre>
<h1>Drop Down List</h1>
Make an HTML drop down list with data received as JSON:
<pre>
const dbParam = JSON.stringify({table:"customers",limit:20});
const xmlhttp = new XMLHttpRequest();
xmlhttp.onload = function() {
  const myObj = JSON.parse(this.responseText);
  let text = "&lt;select&gt;"
  for (let x in myObj) {
    text += "&lt;option&gt;" + myObj[x].name + "&lt;/option&gt;";
  }
  text += "&lt;/select&gt;"
  document.getElementById("demo").innerHTML = text;
  }
}
xmlhttp.open("POST", "json_demo_html_table.php", true);
xmlhttp.setRequestHeader("Content-type", "application/x-www-form-urlencoded");
xmlhttp.send("x=" + dbParam);
</pre>
