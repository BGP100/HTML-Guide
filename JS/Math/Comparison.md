Comparison and Logical operators are used to test for <b>true</b> or <b>false</b>.
<hr>
Comparison operators are used in logical statements to determine equality or difference between variables or values.
<br>
Given that <code>x = 5</code>, the table below explains the comparison operators:
<table class="ws-table-all notranslate">
  <tr>
    <th>Operator</th>
    <th>Short Descriptions</th>
  </tr>
  <tr>
    <td><code>==</code></td>
    <td>Equal to.</td>
  </tr>
  <tr>
    <td><code>===</code></td>
    <td>Equal value and equal type.</td>
  </tr>
  <tr>
    <td><code>!=</code></td>
    <td>Not equal to.</td>
  </tr>
  <tr>
    <td><code>!==</code></td>
    <td>Not equal value or not equal type.</td>
  </tr>
  <tr>
    <td><code>&gt;</code></td>
    <td>Greater than.</td>
  </tr>
  <tr>
    <td><code>&lt;</code></td>
    <td>Less than.</td>
  </tr>
  <tr>
    <td><code>&gt;=</code></td>
    <td>Greater than or equal to.</td>
  </tr>
  <tr>
    <td><code>&lt;=</code></td>
    <td>Less than or equal to.</td>
  </tr>
  <tr>
    <td><code>?</code></td>
    <td>Ternary operator.</td>
  </tr>
</table>
More info in the <a href="/JS/Operators/Comparison.md">Comparison Operators</a> chapter.
<h1>How Can it be Used</h1>
Comparison operators can be used in conditional statements to compare values and take action depending on the result:
<pre>if (age < 18) text = "Too young to buy alcohol";</pre>
<h1>Logical Operators</h1>
Logical operators are used to determine the logic between variables or values.
<br>
Given that <code>x = 6</code> and <code>y = 3</code>, the table below explains the logical operators:
<table class="ws-table-all notranslate">
  <tr>
    <th>Operator</th>
    <th>Description</th>
  </tr>
  <tr>
    <td><code>&&</code></td>
    <td>Logical and.</td>
  </tr>
  <tr>
    <td><code>||</code></td>
    <td>Logical or.</td>
  </tr>
  <tr>
    <td><code>!</code></td>
    <td>Logical not.</td>
  </tr>
</table>
More info in the <a href="/JS/Operators/Logical.md">Logical</a> chapter.
<h1>Comparing Different Types</h1>
Comparing data of different types may give unexpected results.
<br>
When comparing a string with a number, JavaScript will convert the string to a number when doing the comparison. An empty string converts to 0. A non-numeric string converts to <b>NaN</b> which is always <b>false</b>.
<br>
When comparing two strings, "2" will be greater than "12", because (alphabetically) 1 is less than 2.
<br>
To secure a proper result, variables should be converted to the proper type before comparison:
<pre>
age = Number(age);
if (isNaN(age)) {
  voteable = "Input is not a number";
} else {
  voteable = (age < 18) ? "Too young" : "Old enough";
}
</pre>
