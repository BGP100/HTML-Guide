In 2015, JavaScript introduced an important new keyword: <b>const</b>.
<br>
It has become a common practice to declare arrays using <b>const</b>:
<pre>const cars = ["Saab", "Volvo", "BMW"];</pre>
<h1>Cannot be Reassigned</h1>
An array declared with <b>const</b> cannot be reassigned:
<pre>
const cars = ["Saab", "Volvo", "BMW"];
cars = ["Toyota", "Volvo", "Audi"]; // ERROR
</pre>
<h1>Arrays are Not Constants</h1>
The keyword <b>const</b> is a little misleading.
<br>
It does NOT define a constant array. It defines a constant reference to an array.
<br>
Because of this, we can still change the elements of a constant array.
<h1>Elements Can be Reassigned</h1>
You can change the elements of a constant array:
<pre>
// You can create a constant array:
const cars = ["Saab", "Volvo", "BMW"];
// You can change an element:
cars[0] = "Toyota";
// You can add an element:
cars.push("Audi");
</pre>
<h1>Assigned when Declared</h1>
JavaScript const variables must be assigned a value when they are declared:
<br>
<b>Meaning:</b> An arrays declared with const must be initialized when it is declared.
<br>
Using const without initializing the array is a syntax error:
<br>
This will NOT work:
<pre>
const cars;
cars = ["Saab", "Volvo", "BMW"];
</pre>
<h1>Redeclaring Arrays
Redeclaring an array declared with var is allowed anywhere in a program:
<pre>
var cars = ["Volvo", "BMW"]; // Allowed
var cars = ["Toyota", "BMW"]; // Allowed
cars = ["Volvo", "Saab"]; // Allowed
</pre>
Redeclaring or reassigning an array to const, in the same scope, or in the same block, is not allowed:
<pre>
var cars = ["Volvo", "BMW"]; // Allowed
const cars = ["Volvo", "BMW"]; // Not allowed
{
  var cars = ["Volvo", "BMW"]; // Allowed
  const cars = ["Volvo", "BMW"]; // Not allowed
}
</pre>
Redeclaring or reassigning an existing const array, in the same scope, or in the same block, is not allowed:
<pre>
const cars = ["Volvo", "BMW"]; // Allowed
const cars = ["Volvo", "BMW"]; // Not allowed
var cars = ["Volvo", "BMW"]; // Not allowed
cars = ["Volvo", "BMW"]; // Not allowed
{
  const cars = ["Volvo", "BMW"]; // Allowed
  const cars = ["Volvo", "BMW"]; // Not allowed
  var cars = ["Volvo", "BMW"]; // Not allowed
  cars = ["Volvo", "BMW"]; // Not allowed
}
</pre>
Redeclaring an array with const, in another scope, or in another block, is allowed:
<pre>
const cars = ["Volvo", "BMW"]; // Allowed
{
  const cars = ["Volvo", "BMW"]; // Allowed
}
{
  const cars = ["Volvo", "BMW"]; // Allowed
}
</pre>
