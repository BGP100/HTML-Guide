<a href="/JS/APIs/Introduction.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/APIs/History.md">Next &gt;</a>
<hr>
<h1>Constraint Validation DOM Methods</h1>
If an input field contains invalid data, display a message:
<pre>
&lt;input id="id1" type="number" min="100" max="300" required&gt;
&lt;button onclick="myFunction()">OK&lt;/button&gt;
&lt;p id="demo"&gt;&lt;/p&gt;
&lt;script&gt;
function myFunction() {
  const inpObj = document.getElementById("id1");
  if (!inpObj.checkValidity()) {
    document.getElementById("demo").innerHTML = inpObj.validationMessage;
  }
}
&lt;/script&gt;
</pre>
<h1>Constraint Validation DOM Properties</h1>
<table class="ws-table-all notranslate">
  <tr>
<th>Property</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>validity</td>
    <td>Contains boolean properties related to the validity of an input element.</td>
  </tr>
  <tr>
    <td>validationMessage</td>
    <td>Contains the message a browser will display when the validity is false.</td>
  </tr>
  <tr>
    <td>willValidate</td>
    <td>Indicates if an input element will be validated.</td>
  </tr>
</table>
    <h1>Validity Properties</h1>
The <b>validity property</b> of an input element contains a number 
of properties related to the validity of data:
<table class="ws-table-all notranslate">
  <tr>
<th>Property</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>customError</td>
    <td>Set to true, if a custom validity message is set.</td>
  </tr>
  <tr>
    <td>patternMismatch</td>
    <td>Set to true, if an element's value does not match its pattern attribute.</td>
  </tr>
  <tr>
    <td>rangeOverflow</td>
    <td>Set to true, if an element's value is greater than its max attribute.</td>
  </tr>
  <tr>
    <td>rangeUnderflow</td>
    <td>Set to true, if an element's value is less than its min attribute.</td>
  </tr>
  <tr>
    <td>stepMismatch</td>
    <td>Set to true, if an element's value is invalid per its step attribute.</td>
  </tr>
  <tr>
    <td>tooLong</td>
    <td>Set to true, if an element's value exceeds its maxLength attribute.</td>
  </tr>
  <tr>
    <td>typeMismatch</td>
    <td>Set to true, if an element's value is invalid per its type attribute.</td>
  </tr>
  <tr>
    <td>valueMissing</td>
    <td>Set to true, if an element (with a required attribute) has no value.</td>
  </tr>
  <tr>
    <td>valid</td>
    <td>Set to true, if an element's value is valid.</td>
  </tr>
</table>
<h1>Examples</h1>
If the number in an input field is greater than 100 (the input's <b>max</b> attribute), display a message:
<pre>
&lt;input id="id1" type="number" max="100"&gt;
&lt;button onclick="myFunction()">OK&lt;/button&gt;
&lt;p id="demo"&gt;&lt;/p&gt;
&lt;script&gt;
function myFunction() {
  let text = "Value OK";
  if (document.getElementById("id1").validity.rangeOverflow) {
    text = "Value too large";
  }
}
&lt;/script&gt;
</pre>
If the number in an input field is less than 100 (the input's <b>min</b> attribute), display a message:
<pre>
&lt;input id="id1" type="number" min="100"&gt;
&lt;button onclick="myFunction()">OK&lt;/button&gt;
&lt;p id="demo"&gt;&lt;/p&gt;
&lt;script&gt;
function myFunction() {
  let text = = "Value OK";
  if (document.getElementById("id1").validity.rangeOverflow) {
    text = "Value too small";
  }
}
&lt;/script&gt;
</pre>
