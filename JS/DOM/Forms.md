<a href="/JS/DOM/HTML.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/DOM/CSS.md">Next &gt;</a>
<hr>
<h1>Form Validation</h1>
HTML form validation can be done by JavaScript.
<br>
If a form field (fname) is empty, this function alerts a message, and returns false, to prevent the form from being submitted:
<pre>
JavaScript Example
function validateForm() {
  let x = document.forms["myForm"]["fname"].value;
  if (x == "") {
    alert("Name must be filled out");
    return false;
  }
}
</pre>
The function can be called when the form is submitted:
<pre>
&lt;form name="myForm" action="/action_page.php" onsubmit="return validateForm()" method="post"&gt;
Name: &lt;input type="text" name="fname"&gt;
&lt;input type="submit" value="Submit"&gt;
&lt;/form&gt;
</pre>
<h1>Automatic Form Validation</h1>
HTML form validation can be performed automatically by the browser:
<br>
If a form field (fname) is empty, the required attribute prevents this form from being submitted:
<pre>
&lt;form action="/action_page.php" method="post"&gt;
  &lt;input type="text" name="fname" required&gt;
  &lt;input type="submit" value="Submit"&gt;
&lt;/form&gt;
</pre>
<h1>Data Validation</h1>
Data validation is the process of ensuring that user input is clean, correct, and useful.
<br>
Typical validation tasks are:
<ul>
  <li>has the user filled in all required fields?</li>
  <li>has the user entered a valid date?</li>
  <li>has the user entered text in a numeric field?</li>
</ul>
Most often, the purpose of data validation is to ensure correct user input.
<br>
Validation can be defined by many different methods, and deployed in many different ways.
<br>
Server side validation is performed by a web server, after input has been sent to the server.
<br>
Client side validation is performed by a web browser, before input is sent to a web server.
<h1>Constraint Validation</h1>
HTML5 introduced a new HTML validation concept called constraint validation.
<br>
HTML constraint validation is based on:
<ul>
  <li>Constraint validation HTML Input Attributes</li>
  <li>Constraint validation CSS Pseudo Selectors</li>
  <li>Constraint validation DOM Properties and Methods</li>
</ul>
<h1>Constraint Validation Input Form Attributes</h1>
<table class="ws-table-all notranslate">
  <tr>
    <th>Attribute</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>disabled</td>
    <td>Specifies that the input element should be disabled</td>
  </tr>
  <tr>
    <td>max</td>
    <td>Specifies the maximum value of an input element</td>
  </tr>
  <tr>
    <td>min</td>
    <td>Specifies the minimum value of an input element</td>
  </tr>
  <tr>
    <td>pattern</td>
    <td>Specifies the value pattern of an input element</td>
  </tr>
  <tr>
    <td>required</td>
    <td>Specifies that the input field requires an element</td>
  </tr>
  <tr>
    <td>type</td>
    <td>Specifies the type of an input element</td>
  </tr>
</table>
For a full list, go to <a href="/HTML/Forms/Input-FormAttributes.md">Input Form Attributes</a>.
<h1>Constraint Validation CSS Pseudo Selectors</h1>
<table class="ws-table-all notranslate">
  <tr>
    <th>Selector</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>:disabled</td>
    <td>Selects input elements with the "disabled" attribute specified</td>
  </tr>
  <tr>
    <td>:invalid</td>
    <td>Selects input elements with invalid values</td>
  </tr>
  <tr>
    <td>:optional</td>
    <td>Selects input elements with no "required" attribute specified</td>
  </tr>
  <tr>
    <td>:required</td>
    <td>Selects input elements with the "required" attribute specified</td>
  </tr>
  <tr>
    <td>:valid</td>
    <td>Selects input elements with valid values</td>
  </tr>
</table>
For a full list, go to <a href="/CSS/Pseudo-Class.md">CSS Pseudo Classes</a>.
