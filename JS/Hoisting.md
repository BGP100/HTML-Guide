Hoisting is JavaScript's default behavior of moving declarations to the top.
<h1>Declarations are Hoisted</h1>
In JavaScript, a variable can be declared after it has been used.
<br>
In other words; a variable can be used before it has been declared.
<br>
Example 1 gives the same result as Example 2:
<pre>
x = 5; // Assign 5 to x
elem = document.getElementById("demo"); // Find an element
elem.innerHTML = x; // Display x in the element
var x; // Declare x
</pre>
<pre>
var x; // Declare x
x = 5; // Assign 5 to x
elem = document.getElementById("demo"); // Find an element
elem.innerHTML = x; // Display x in the element
</pre>
To understand this, you have to understand the term "hoisting".
<br>
Hoisting is JavaScript's default behavior of moving all declarations to the top of the current scope (to the top of the current script or the current function).
<h1>let & const</h1>
Variables defined with <b>let</b> and <b>const</b> are hoisted to the top of the block, but not initialized.
<br>
<b>Meaning:</b> The block of code is aware of the variable, but it cannot be used until it has been declared.
<br>
Using a <b>let</b> variable before it is declared will result in a <b>ReferenceError</b>.
<br>
The variable is in a "temporal dead zone" from the start of the block until it is declared:
<pre>
carName = "Volvo";
let carName;
</pre>
Using a const variable before it is declared, is a syntax errror, so the code will simply not run.
<pre>
carName = "Volvo";
const carName;
</pre>
<h1>Initializations are Not Hoisted</h1>
JavaScript only hoists declarations, not initializations.
<br>
Example 1 does not give the same result as Example 2:
<pre>
var x = 5; // Initialize x
var y = 7; // Initialize y
elem = document.getElementById("demo"); // Find an element
elem.innerHTML = x + " " + y; // Display x and y
</pre>
<pre>
var x = 5; // Initialize x
elem = document.getElementById("demo"); // Find an element
elem.innerHTML = x + " " + y; // Display x and y
var y = 7; // Initialize y
</pre>
Does it make sense that y is undefined in the last example?
<br>
This is because only the declaration (<code>var y</code>), not the initialization (<code>=7</code>) is hoisted to the top.
<br>
Because of hoisting, y has been declared before it is used, but because initializations are not hoisted, the value of y is undefined.
<br>
Example 2 is the same as writing:
<pre>
var x = 5; // Initialize x
var y; // Declare y
elem = document.getElementById("demo"); // Find an element
elem.innerHTML = x + " " + y; // Display x and y
y = 7; // Assign 7 to y
</pre>
<h1>Declare Your Variables At the Top !</h1>
Hoisting is (to many developers) an unknown or overlooked behavior of JavaScript.
<br>
If a developer doesn't understand hoisting, programs may contain bugs (errors).
<br>
To avoid bugs, always declare all variables at the beginning of every scope.
<br>
Since this is how JavaScript interprets the code, it is always a good rule.
