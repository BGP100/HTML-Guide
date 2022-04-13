<a href="/JS/Errors.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Hoisting.md">Next &gt;</a>
<hr>
Scope determines the accessibility (visibility) of variables.
<br>
JavaScript has 3 types of scope:
<ul>
  <li>Block scope</li>
  <li>Function scope</li>
  <li>Global scope</li>
</ul>
<h1>Block Scope</h1>
Before ES6 (2015), JavaScript had only Global Scope and Function Scope.
<br>
ES6 introduced two important new JavaScript keywords: <b>let</b> and <b>const</b>.
<br>
These two keywords provide Block Scope in JavaScript.
<br>
Variables declared inside a { } block cannot be accessed from outside the block:
<pre>
{
  let x = 2;
}
// x can NOT be used here
</pre>
Variables declared with the <b>var</b> keyword can NOT have block scope.
<br>
Variables declared inside a { } block can be accessed from outside the block.
<pre>
{
  var x = 2;
}
// x CAN be used here
</pre>
<h1>Local Scope</pre>
Variables declared within a JavaScript function, become LOCAL to the function.
<pre>
// code here can NOT use carName

function myFunction() {
  let carName = "Volvo";
  // code here CAN use carName
}
// code here can NOT use carName
</pre>
Since local variables are only recognized inside their functions, variables with the same name can be used in different functions.
<br>
Local variables are created when a function starts, and deleted when the function is completed.
<h1>Function Scope</h1>
JavaScript has function scope: Each function creates a new scope.
<br>
Variables defined inside a function are not accessible (visible) from outside the function.
<br>
Variables declared with var, let and const are quite similar when declared inside a function.
<br>
They all have Function Scope:
<pre>
function myFunction() {
  var carName = "Volvo";   // Function Scope
}
</pre>
<pre>
function myFunction() {
  let carName = "Volvo";   // Function Scope
}
</pre>
<pre>
function myFunction() {
  const carName = "Volvo";   // Function Scope
}
</pre>
<h1>Global Variables</h1>
A variable declared outside a function, becomes GLOBAL.
<pre>
let carName = "Volvo";
// code here can use carName
function myFunction() {
// code here can also use carName
}
</pre>
<h1>Global Scope</h1>
Variables declared Globally (outside any function) have Global Scope.
<br>
Global variables can be accessed from anywhere in a JavaScript program.
<br>
Variables declared with var, let and const are quite similar when declared outside a block.
<br>
They all have Global Scope:
<pre>
var x = 2;       // Global scope
let x = 2;       // Global scope
const x = 2;       // Global scope
</pre>
<h1>Automatic Global</h1>
If you assign a value to a variable that has not been declared, it will automatically become a GLOBAL variable.
<br>
This code example will declare a global variable carName, even if the value is assigned inside a function.
<pre>
myFunction();
// code here can use carName
function myFunction() {
  carName = "Volvo";
}
</pre>
<h1>Global Variables</h1>
With JavaScript, the global scope is the JavaScript environment.
<br>
In HTML, the global scope is the window object.
<br>
Global variables defined with the <b>var</b> keyword belong to the window object:
<pre>
var carName = "Volvo";
// code here can use window.carName
</pre>
Global variables defined with the let keyword do not belong to the window object:
<pre>
let carName = "Volvo";
// code here can use window.carName
</pre>
<h1>The Lifetime of Variables</h1>
The lifetime of a JavaScript variable starts when it is declared.
<br>
Function (local) variables are deleted when the function is completed.
<br>
In a web browser, global variables are deleted when you close the browser window (or tab).
