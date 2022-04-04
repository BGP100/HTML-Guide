The let keyword was introduced in ES6 (2015).
<br>
Variables defined with let cannot be Redeclared.
<br>
Variables defined with let must be Declared before use.
<br>
Variables defined with let have Block Scope.
<h1>Browser Support</h1>
The <b>let</b> keyword is not fully supported in Internet Explorer 11 or earlier.
<br>
The following table defines the first browser versions with full support for the <b>let</b> keyword:
<table class="ws-table-all notranslate">
  <tr>
    <th>Browser</th>
    <th>Chrome</th>
    <th>Edge</th>
    <th>Firefox</th>
    <th>Safari</th>
    <th>Opera</th>
  </tr>
  <tr>
    <td>Version</td>
    <td>49.0</td>
    <td>12.0</td>
    <td>44.0</td>
    <td>11.0</td>
    <td>36.0</td>
  </tr>
  <tr>
    <td>Date</td>
    <td>Mar, 2016</td>
    <td>Jul, 2015</td>
    <td>Jan, 2015</td>
    <td>Sep, 2017</td>
    <td>Mar, 2016</td>
  </tr>
</table>
<h1>Cannot be Redeclared</h1>
Variables defined with <b>let</b> cannot be redeclared.
<br>
You cannot accidentally redeclare a variable.
<br>
With <b>let</b> you can not do this:
<pre>
let x = "John Doe";
let x = 0;
// SyntaxError: 'x' has already been declared
</pre>
With <b>var</b> you can:
<pre>
var x = "John Doe";
var x = 0;
</pre>
<h1>Block Scope</h1>
Before ES6 (2015), JavaScript had only Global Scope and Function Scope.
<br>
ES6 introduced two important new JavaScript keywords: <b>let</b> and <b>const</b>.
<br>
These two keywords provide Block Scope in JavaScript.
<br>
Variables declared inside a <code>{</code> <code>}</code> block cannot be accessed from outside the block:
<pre>
{ 
  let x = 2;
}
// x CANT be used here
</pre>
Variables declared with the var keyword can NOT have block scope.
<br>
Variables declared inside a <code>{</code> <code>}</code> block can be accessed from outside the block.
<pre>
{ 
  var x = 2; 
}
// x CAN be used here
</pre>
<h1>Redeclaring Variables</h1>
Redeclaring a variable using the <b>var</b> keyword can impose problems.
<br>
Redeclaring a variable inside a block will also redeclare the variable outside the block:
<pre>
var x = 10;
// Here x is 10
{ 
var x = 2;
// Here x is 2
}
// Here x is 2
</pre>
Redeclaring a variable using the <b>let</b> keyword can solve this problem.
<br>
Redeclaring a variable inside a block will not redeclare the variable outside the block:
<pre>
let x = 10;
// Here x is 10
{
let x = 2;
// Here x is 2
}
// Here x is 10
</pre>
<h1>Redeclaring</h1>
Redeclaring a JavaScript variable with <b>var</b> is allowed anywhere in a program:
<pre>
var x = 2;
// Now x is 2
var x = 3;
// Now x is 3
</pre>
With <b>let</b>, redeclaring a variable in the same block is NOT allowed:
<pre>
var x = 2; // Allowed
let x = 3; // Not allowed
{
let x = 2; // Allowed
let x = 3 // Not allowed
}
{
let x = 2; // Allowed
var x = 3 // Not allowed
}
</pre>
Redeclaring a variable with <b>let</b>, in another block, IS allowed:
<pre>
let x = 2; // Allowed
{
let x = 3; // Allowed
}
{
let x = 4; // Allowed
}
</pre>
<h1>Let Hoisting</h1>
Variables defined with <b>var</b> are hoisted to the top and can be initialized at any time.
<br>
<b>Meaning:</b> You can use the variable before it is declared:
<pre>
// This is OK:
carName = "Volvo";
var carName;
</pre>
If you want to learn more about hoisting, study the chapter JavaScript Hoisting.
<br>
Variables defined with <b>let</b> are also hoisted to the top of the block, but not initialized.
<br>
<b>Meaning:</b> Using a <b>let</b> variable before it is declared will result in a <b>ReferenceError</b>:
<pre>
carName = "Saab";
let carName = "Volvo";
</pre>
