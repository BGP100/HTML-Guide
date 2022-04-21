<a href="/JS/AJAX/XML.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/AJAX/ASP.md">Next &gt;</a>
<hr>
<h1>Example</h1>
The following example demonstrates how a web page can communicate with a web server while a user types characters in an input field:
<pre>Sorry, but GitHub can't display these type of stuff.</pre>
<h1>Explained</h1>
In the example above, when a user types a character in the input field, a function called showHint() is executed.
<br>
The function is triggered by the onkeyup event.
<br>
Here is the code:
<pre>
&lt;p&gt;Start typing a name in the input field below:&lt;/p&gt;
&lt;p&gt;Suggestions: &lt;span id="txtHint"&gt;&lt;/span&gt;&lt;/p&gt;
&lt;form&gt;
First name: &lt;input type="text" onkeyup="showHint(this.value)"&gt;
&lt;/form&gt;
&lt;script&gt;
function showHint(str) {
  if (str.length == 0) {
    document.getElementById("txtHint").innerHTML = "";
    return;
  } else {
    const xmlhttp = new XMLHttpRequest();
    xmlhttp.onload = function() {
      document.getElementById("txtHint").innerHTML = this.responseText;
    }
  xmlhttp.open("GET", "gethint.php?q=" + str);
  xmlhttp.send();
  }
}
&lt;/script&gt;
</pre>
<b>Code explanation:</b>
<br>
First, check if the input field is empty (<code>str.length == 0</code>). If it is, clear the content of the txtHint placeholder and exit the function.
<br>
However, if the input field is not empty, do the following:
<ul>
  <li>Create an XMLHttpRequest object</li>
  <li>Create the function to be executed when the server response is ready</li>
  <li>Send the request off to a PHP file (gethint.php) on the server</li>
  <li>Notice that q parameter is added <code>gethint.php?q="+str</code></li>
  <li>The str variable holds the content of the input field</li>
</ul>
<h1>"gethint.php"</h1>
The PHP file checks an array of names, and returns the corresponding name(s) to the browser:
<pre>
&lt;?php
// Array with names
$a[] = "Anna";
$a[] = "Brittany";
$a[] = "Cinderella";
$a[] = "Diana";
$a[] = "Eva";
$a[] = "Fiona";
$a[] = "Gunda";
$a[] = "Hege";
$a[] = "Inga";
$a[] = "Johanna";
$a[] = "Kitty";
$a[] = "Linda";
$a[] = "Nina";
$a[] = "Ophelia";
$a[] = "Petunia";
$a[] = "Amanda";
$a[] = "Raquel";
$a[] = "Cindy";
$a[] = "Doris";
$a[] = "Eve";
$a[] = "Evita";
$a[] = "Sunniva";
$a[] = "Tove";
$a[] = "Unni";
$a[] = "Violet";
$a[] = "Liza";
$a[] = "Elizabeth";
$a[] = "Ellen";
$a[] = "Wenche";
$a[] = "Vicky";
// get the q parameter from URL
$q = $_REQUEST["q"];
$hint = "";
// lookup all hints from array if $q is different from ""
if ($q !== "") {
  $q = strtolower($q);
  $len=strlen($q);
  foreach($a as $name) {
    if (stristr($q, substr($name, 0, $len))) {
      if ($hint === "") {
        $hint = $name;
      } else {
        $hint .= ", $name";
      }
    }
  }
}
// Output "no suggestion" if no hint was found or output correct values
echo $hint === "" ? "no suggestion" : $hint;
?&gt;
</pre>
