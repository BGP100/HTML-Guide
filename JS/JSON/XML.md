Both JSON and XML can be used to receive data from a web server.
<br>
The following JSON and XML examples both define an employees object, with an array of 3 employees:
<br>
<b>JSON:</b>
<pre>
{"employees":[
  { "firstName":"John", "lastName":"Doe" },
  { "firstName":"Will", "lastName":"Smith" },
  { "firstName":"Peter", "lastName":"Jones" }
]}
</pre>
<b>XML:</b>
<pre>
&lt;employees&gt;
  &lt;employee&gt;
    &lt;firstName&gt;John&lt;/firstName> &lt;lastName&gt;Doe&lt;/lastName&gt;
  &lt;/employee&gt;
  &lt;employee&gt;
    &lt;firstName&gt;Will&lt;/firstName> &lt;lastName&gt;Smith&lt;/lastName&gt;
  &lt;/employee&gt;
  &lt;employee&gt;
    &lt;firstName&gt;Peter&lt;/firstName> &lt;lastName&gt;Jones&lt;/lastName&gt;
  &lt;/employee&gt;
&lt;/employees&gt;
</pre>
<h1>JSON is Like XML Because</h1>
<ul>
  <li>Both JSON and XML are "self describing" (human readable)</li>
  <li>Both JSON and XML are hierarchical (values within values)</li>
  <li>Both JSON and XML can be parsed and used by lots of programming languages</li>
  <li>Both JSON and XML can be fetched with an XMLHttpRequest</li>
</ul>
<h1>JSON is Unlike XML Because</h1>
<ul>
  <li>JSON doesn't use end tag</li>
  <li>JSON is shorter</li>
  <li>JSON is quicker to read and write</li>
  <li>JSON can use arrays</li>
</ul>
The biggest difference is:
<br>
XML has to be parsed with an XML parser. JSON can be parsed by a standard JavaScript function.
<h1>Why JSON is better than XML</h1>
For AJAX applications, JSON is faster and easier than XML:
<br>
<b>Using XML</b>
<ul>
  <li>Fetch an XML document</li>
  <li>Use the XML DOM to loop through the document</li>
  <li>Extract values and store in variables</li>
</ul>
<b>Using JSON</b>
<ul>
  <li>Fetch a JSON string</li>
  <li>JSON.Parse the JSON string</li>
</ul>
