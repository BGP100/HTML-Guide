<a href="/JS/AJAX/PHP.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/AJAX/Database.md">Next &gt;</a>
<hr>
<h1>Example</h1>
The following example demonstrates how a web page can communicate with a web server while a user type characters in an input field:
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
  xmlhttp.open("GET", "gethint.asp?q=" + str);
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
  <li>Notice that q parameter is added <code>gethint.asp?q="+str</code></li>
  <li>The str variable holds the content of the input field</li>
</ul>
<h1>"gethint.asp"</h1>
The ASP file checks an array of names, and returns the corresponding name(s) to the browser:
<pre>
&lt;%
response.expires = -1
dim a(30)
'Fill up array with names
a(1) = "Anna"
a(2) = "Brittany"
a(3) = "Cinderella"
a(4) = "Diana"
a(5) = "Eva"
a(6) = "Fiona"
a(7) = "Gunda"
a(8) = "Hege"
a(9) = "Inga"
a(10) = "Johanna"
a(11) = "Kitty"
a(12) = "Linda"
a(13) = "Nina"
a(14) = "Ophelia"
a(15) = "Petunia"
a(16) = "Amanda"
a(17) = "Raquel"
a(18) = "Cindy"
a(19) = "Doris"
a(20) = "Eve"
a(21) = "Evita"
a(22) = "Sunniva"
a(23) = "Tove"
a(24) = "Unni"
a(25) = "Violet"
a(26) = "Liza"
a(27) = "Elizabeth"
a(28) = "Ellen"
a(29) = "Wenche"
a(30) = "Vicky"
'get the q parameter from URL
q = ucase(request.querystring("q"))
'lookup all hints from array if length of q &gt; 0
if len(q) &gt; 0 then
  hint = ""
  for i = 1 to 30
    if q = ucase(mid(a(i),1,len(q))) then
      if hint = "" then
        hint = a(i)
      else
        hint = hint & ", " & a(i)
      end if
    end if
  next
end if
'Output "no suggestion" if no hint were found
'or output the correct values
if hint = "" then
  response.write("no suggestion")
else
  response.write(hint)
end if
%&gt;
</pre>
