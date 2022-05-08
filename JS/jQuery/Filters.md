<a href="/JS/jQuery/NoConflict.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="https://bledy-guides.repl.co">Next &gt;</a>
<hr>
Use jQuery to filter/search for specific elements.
<h1>Filter Tables</h1>
Perform a case-insensitive search for items in a table:
<pre>
&lt;head&gt;
&lt;script&gt;
$(document).ready(function(){
  $("#myInput").on("keyup", function() {
    var value = $(this).val().toLowerCase();
    $("#myTable tr").filter(function() {
      $(this).toggle($(this).text().toLowerCase().indexOf(value) &gt; -1)
    });
  });
});
&lt;/script&gt;
&lt;script src="https://ajax.googleapis.com/ajax/libs/jquery/3.6.0/jquery.min.js"&gt;&lt;/script&gt;
&lt;/head&gt;
&lt;style&gt;
table {
  font-family: arial, sans-serif;
  border-collapse: collapse;
  width: 100%;
}
td, th {
  border: 1px solid #dddddd;
  text-align: left;
  padding: 8px;
}
tr:nth-child(even) {
  background-color: #dddddd;
}
&lt;/style&gt;
&lt;input id="myInput" type="text" placeholder="Search.."&gt;
&lt;br&gt;&lt;br&gt;
&lt;table&gt;
  &lt;thead&gt;
  &lt;tr&gt;
    &lt;th&gt;Firstname&lt;/th&gt;
    &lt;th&gt;Lastname&lt;/th&gt;
    &lt;th&gt;Email&lt;/th&gt;
  &lt;/tr&gt;
  &lt;/thead&gt;
  &lt;tbody id="myTable"&gt;
  &lt;tr&gt;
    &lt;td&gt;John&lt;/td&gt;
    &lt;td&gt;Doe&lt;/td&gt;
    &lt;td&gt;john@example.com&lt;/td&gt;
  &lt;/tr&gt;
  &lt;tr&gt;
    &lt;td&gt;Mary&lt;/td&gt;
    &lt;td&gt;Moe&lt;/td&gt;
    &lt;td&gt;mary@mail.com&lt;/td&gt;
  &lt;/tr&gt;
  &lt;tr&gt;
    &lt;td&gt;July&lt;/td&gt;
    &lt;td&gt;Dooley&lt;/td&gt;
    &lt;td&gt;july@greatstuff.com&lt;/td&gt;
  &lt;/tr&gt;
  &lt;tr&gt;
    &lt;td&gt;Anja&lt;/td&gt;
    &lt;td&gt;Ravendale&lt;/td&gt;
    &lt;td&gt;a_r@test.com&lt;/td&gt;
  &lt;/tr&gt;
  &lt;/tbody&gt;
&lt;/table&gt;
</pre>
<b>Explained:</b>
<br>
We use jQuery to loop through each table rows to check if there are any text values that matches the value of the input field. The <b>toggle()</b> method hides the row (<b>display:none</b>) that does not match the search. We use the <b>toLowerCase()</b> DOM method to convert the text to lower case, which makes the search case insensitive (allows "john", "John", and even "JOHN" on search).
<h1>Filter Lists</h1>
Perform a case-insensitive search for items in a list:
<pre>
&lt;head&gt;
&lt;script&gt;
$(document).ready(function(){
  $("#myInput").on("keyup", function() {
    var value = $(this).val().toLowerCase();
    $("#myTable tr").filter(function() {
      $(this).toggle($(this).text().toLowerCase().indexOf(value) &gt; -1)
    });
  });
});
&lt;/script&gt;
&lt;script src="https://ajax.googleapis.com/ajax/libs/jquery/3.6.0/jquery.min.js"&gt;&lt;/script&gt;
&lt;/head&gt;
&lt;input id="myInput" type="text" placeholder="Search.."&gt;
&lt;br&gt;
&lt;ul id="myList"&gt;
  &lt;li&gt;First item&lt;/li&gt;
  &lt;li&gt;Second item&lt;/li&gt;
  &lt;li&gt;Third item&lt;/li&gt;
  &lt;li&gt;Fourth&lt;/li&gt;
&lt;/ul&gt;
</pre>
<h1>Filter Anything</h1>
Perform a case-insensitive search for text inside a div element:
<pre>
&lt;head&gt;
&lt;script&gt;
$(document).ready(function(){
  $("#myInput").on("keyup", function() {
    var value = $(this).val().toLowerCase();
    $("#myTable tr").filter(function() {
      $(this).toggle($(this).text().toLowerCase().indexOf(value) &gt; -1)
    });
  });
});
&lt;/script&gt;
&lt;script src="https://ajax.googleapis.com/ajax/libs/jquery/3.6.0/jquery.min.js"&gt;&lt;/script&gt;
&lt;/head&gt;
&lt;input id="myInput" type="text" placeholder="Search.."&gt;
&lt;div id="myDIV"&gt;
  &lt;p&gt;I am a paragraph.&lt;/p&gt;
  &lt;div&gt;I am a div element inside div.&lt;/div&gt;
  &lt;br&gt;
  &lt;button&gt;I am a button&lt;/button&gt;
  &lt;button&gt;Another button&lt;/button&gt;
  &lt;p&gt;Another paragraph.&lt;/p&gt;
&lt;/div&gt;
</pre>
