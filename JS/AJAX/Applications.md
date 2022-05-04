<a href="/JS/AJAX/Database.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="https://bledy-guides.repl.co/#ajax">Next &gt;</a>
<hr>
This chapter demonstrates some HTML applications using XML, HTTP, DOM, and JavaScript.
<h1>The XML Document Used</h1>
In this chapter we will use the XML file called <a href="https://codepen.io/BGP100/pen/GRyePxw">"cd_catalog.xml"</a>.
<h1>Display XML Data in an HTML Table</h1>
This example loops through each &lt;CD&gt; element, and displays the values of the &lt;ARTIST&gt; and the &lt;TITLE&gt; elements in an HTML table:
<pre>
&lt;table id="demo"&gt;&lt;/table&gt;
&lt;script&gt;
function loadXMLDoc() {
  const xhttp = new XMLHttpRequest();
  xhttp.onload = function() {
    const xmlDoc = xhttp.responseXML;
    const cd = xmlDoc.getElementsByTagName("CD");
    myFunction(cd);
  }
  xhttp.open("GET", "cd_catalog.xml");
  xhttp.send();
}
function myFunction(cd) {
  let table="&lt;tr&gt;&lt;th&gt;Artist&lt;/th&gt;&lt;th&gt;Title&lt;/th&gt;&lt;/tr&gt;";
  for (let i = 0; i &lt; cd.length; i++) {
    table += "&lt;tr&gt;&lt;td&gt;" + cd[i].getElementsByTagName("ARTIST")[0].childNodes[0].nodeValue + "&lt;/td&gt;&lt;td&gt;" + cd[i].getElementsByTagName("TITLE")[0].childNodes[0].nodeValue + "&lt;/td&gt;&lt;/tr&gt;";
  }
  document.getElementById("demo").innerHTML = table;
}
&lt;/script&gt;
</pre>
<h1>Display the First CD in an HTML div Element</h1>
This example uses a function to display the first CD element in an HTML element with id="showCD":
<pre>
const xhttp = new XMLHttpRequest();
xhttp.onload = function() {
  const xmlDoc = xhttp.responseXML;
  const cd = xmlDoc.getElementsByTagName("CD");
  myFunction(cd, 0);
}
xhttp.open("GET", "cd_catalog.xml");
xhttp.send();
function myFunction(cd, i) {
  document.getElementById("showCD").innerHTML = "Artist: " + cd[i].getElementsByTagName("ARTIST")[0].childNodes[0].nodeValue + "&lt;br&gt;Title: " + cd[i].getElementsByTagName("TITLE")[0].childNodes[0].nodeValue + "&lt;br&gt;Year: " + cd[i].getElementsByTagName("YEAR")[0].childNodes[0].nodeValue;
}
</pre>
<h1>Navigate Between the CDs</h1>
To navigate between the CDs in the example above, create a next() and previous() function:
<pre>
function next() {
  // display the next CD, unless you are on the last CD
  if (i &lt; len-1) {
    i++;
    displayCD(i);
  }
}
function previous() {
  // display the previous CD, unless you are on the first CD
  if (i &gt; 0) {
    i--;
    displayCD(i);
  }
}
</pre>
<h1>Show Album Information When Clicking On a CD</h1>
The last example shows how you can show album information when the user clicks on a CD:
<pre>
function displayCD(i) {
  document.getElementById("showCD").innerHTML = "Artist: " + cd[i].getElementsByTagName("ARTIST")[0].childNodes[0].nodeValue + "&lt;br&gt;Title: " + cd[i].getElementsByTagName("TITLE")[0].childNodes[0].nodeValue + "&lt;br&gt;Year: " + cd[i].getElementsByTagName("YEAR")[0].childNodes[0].nodeValue;
}
</pre>
