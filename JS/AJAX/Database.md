<a href="/JS/AJAX/ASP.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/AJAX/Applications.md">Next &gt;</a>
<hr>
<h1>Example</h1>
The following example will demonstrate how a web page can fetch information from a database with AJAX:
<pre>Sorry, but GitHub can't display these type of stuff.</pre>
<h1>Explained</h1>
When a user selects a customer in the dropdown list above, a function called showCustomer() is executed. The function is triggered by the onchange event:
<pre>
function showCustomer(str) {
  if (str == "") {
    document.getElementById("txtHint").innerHTML = "";
    return;
  }
  const xhttp = new XMLHttpRequest();
  xhttp.onload = function() {
    document.getElementById("txtHint").innerHTML = this.responseText;
  }
  xhttp.open("GET", "getcustomer.php?q="+str);
  xhttp.send();
}
</pre>
The showCustomer() function does the following:
<ul>
  <li>Check if a customer is selected</li>
  <li>Create an XMLHttpRequest object</li>
  <li>Create the function to be executed when the server response is ready</li>
  <li>Send the request off to a file on the server</li>
  <li>Notice that a parameter (q) is added to the URL (with the content of the dropdown list)</li>
</ul>
<h1>getcustomer.php</h1>
The page on the server called by the JavaScript above is a PHP file called "getcustomer.php".
<br>
The source code in "getcustomer.php" runs a query against a database, and returns the result in an HTML table:
<pre>
&lt;?php
$mysqli = new mysqli("servername", "username", "password", "dbname");
if($mysqli-&gt;connect_error) {
  exit('Could not connect');
}
$sql = "SELECT customerid, companyname, contactname, address, city, postalcode, country
FROM customers WHERE customerid = ?";
$stmt = $mysqli-&gt;prepare($sql);
$stmt-&gt;bind_param("s", $_GET['q']);
$stmt-&gt;execute();
$stmt-&gt;store_result();
$stmt-&gt;bind_result($cid, $cname, $name, $adr, $city, $pcode, $country);
$stmt-&gt;fetch();
$stmt-&gt;close();
echo "&lt;table&gt;";
echo "&lt;tr&gt;";
echo "&lt;th>CustomerID&lt;/th&gt;";
echo "&lt;td&gt;" . $cid . "&lt;/td&gt;";
echo "&lt;th&gt;CompanyName&lt;/th&gt;";
echo "&lt;td&gt;" . $cname . "&lt;/td&gt;";
echo "&lt;th&gt;ContactName&lt;/th&gt;";
echo "&lt;td&gt;" . $name . "&lt;/td&gt;";
echo "&lt;th&gt;Address&lt;/th&gt;";
echo "&lt;td&gt;" . $adr . "&lt;/td&gt;";
echo "&lt;th&gt;City&lt;/th&gt;";
echo "&lt;td&gt;" . $city . "&lt;/td&gt;";
echo "&lt;th&gt;PostalCode&lt;/th&gt;";
echo "&lt;td&gt;" . $pcode . "&lt;/td&gt;";
echo "&lt;th&gt;Country&lt;/th&gt;";
echo "&lt;td&gt;" . $country . "&lt;/td&gt;";
echo "&lt;/tr&gt;";
echo "&lt;/table&gt;";
?&gt;
</pre>
