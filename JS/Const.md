<a href="/JS/Let.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Operators/Main.md">Next &gt;</a>
<hr>
The <b>const</b> keyword was introduced in ES6 (2015).
<br>
Variables defined with <b>const</b> cannot be Redeclared.
<br>
Variables defined with <b>const</b> cannot be Reassigned.
<br>
Variables defined with <b>const</b> have Block Scope.
<h1>Browser Support</h1>
The <b>const</b> keyword is not supported in Internet Explorer 10 or earlier.
<br>
The following table defines the first browser versions with full support for the <b>const</b> keyword:
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
    <td>11.0</td>
    <td>36.0</td>
    <td>10.0</td>
    <td>36.0</td>
  </tr>
  <tr>
    <td>Date</td>
    <td>Mar, 2016</td>
    <td>Oct, 2013</td>
    <td>Feb, 2015</td>
    <td>Sep, 2016</td>
    <td>Mar, 2016</td>
  </tr>
</table>
Chrome 49	IE 11 / Edge	Firefox 36	Safari 10	Opera 36
Mar, 2016	Oct, 2013	Feb, 2015	Sep, 2016	Mar, 2016
<h1>Cannot be Reassigned</h1>
A <b>const</b> variable cannot be reassigned:
<pre>
const PI = 3.141592653589793;
PI = 3.14; // This will give an error
PI = PI + 10; // This will also give an error
</pre>
<h1>Must be Assigned</h1>
JavaScript <b>const</b> variables must be assigned a value when they are declared:
<br>
<b>Correct:</b>
<pre>const PI = 3.14159265359;</pre>
<b>Incorrect:</b>
<pre>
const PI;
PI = 3.14159265359;
</pre>
<h1>When to use const?</h1>
As a general rule, always declare a variable with <b>const</b> unless you know that the value will change.
<br>
Use <b>const</b> when you declare:
<ul>
  <li>A new Array</li>
  <li>A new Object</li>
  <li>A new Function</li>
  <li>A new RegExp</li>
</ul>
Constant Objects and Arrays
The keyword const is a little misleading.
<br>
It does not define a constant value. It defines a constant reference to a value.
<ul>
  <li>Because of this you can NOT:
  <ul>
    <li>Reassign a constant value</li>
    <li>Reassign a constant array</li>
    <li>Reassign a constant object</li>
  </ul>
  <li>But you CAN:
  <ul>
    <li>Change the elements of constant array</li>
    <li>Change the properties of constant object</li>
    <li>Constant Arrays</li>
  </ul>
</ul>
You can change the elements of a constant array:
<pre>
// You can create a constant array:
const cars = ["Saab", "Volvo", "BMW"];
// You can change an element:
cars[0] = "Toyota";
// You can add an element:
cars.push("Audi");
</pre>
But you can NOT reassign the array:
<pre>
const cars = ["Saab", "Volvo", "BMW"];
cars = ["Toyota", "Volvo", "Audi"]; // ERROR
</pre>
<h1>Constant Objects</h1>
You can change the properties of a constant object:
<pre>
// You can create a const object:
const car = {type:"Fiat", model:"500", color:"white"};
// You can change a property:
car.color = "red";
// You can add a property:
car.owner = "Johnson";
</pre>
But you can NOT reassign the object:
<pre>
const car = {type:"Fiat", model:"500", color:"white"};
car = {type:"Volvo", model:"EX60", color:"red"}; // ERROR
</pre>
<h1>Block Scope</h1>
Declaring a variable with const is similar to let when it comes to Block Scope.
<br>
The x declared in the block, in this example, is not the same as the x declared outside the block:
<pre>
const x = 10;
// Here x is 10
{ 
const x = 2;
// Here x is 2
}
// Here x is 10
</pre>
You can learn more about block scope in the chapter JavaScript Scope.
<h1>Redeclaring</h1>
Redeclaring a JavaScript var variable is allowed anywhere in a program:
<pre>
var x = 2; // Allowed
var x = 3; // Allowed
x = 4; // Allowed
</pre>
Redeclaring an existing var or let variable to const, in the same scope, is not allowed:
<pre>
var x = 2; // Allowed
const x = 2; // Not allowed
{
let x = 2; // Allowed
const x = 2; // Not allowed
}
{
const x = 2; // Allowed
const x = 2; // Not allowed
}
</pre>
Reassigning an existing const variable, in the same scope, is not allowed:
<pre>
const x = 2; // Allowed
x = 2; // Not allowed
var x = 2; // Not allowed
let x = 2; // Not allowed
const x = 2; // Not allowed
{
  const x = 2; // Allowed
  x = 2; // Not allowed
  var x = 2; // Not allowed
  let x = 2; // Not allowed
  const x = 2; // Not allowed
}
</pre>
Redeclaring a variable with const, in another scope, or in another block, is allowed:
<pre>
const x = 2; // Allowed
{
  const x = 3; // Allowed
}
{
  const x = 4; // Allowed
}
</pre>
<h1>Const Hoisting</h1>
Variables defined with var are hoisted to the top and can be initialized at any time.
<br>
<b>Meaning:</b> You can use the variable before it is declared:
<br>
This is OK:
<pre>
carName = "Volvo";
var carName;
</pre>
If you want to learn more about hoisting, study the chapter JavaScript Hoisting.
<br>
Variables defined with const are also hoisted to the top, but not initialized.
<br>
<b>Meaning:</b> Using a const variable before it is declared will result in a ReferenceError:
<pre>
alert (carName);
const carName = "Volvo";
</pre>
