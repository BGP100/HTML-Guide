<a href="/JS/Functions/Main.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Functions/Parameter.md">Next &gt;</a>
<hr>
JavaScript functions are defined with the <b>function</b> keyword.
<br>
You can use a function declaration or a function expression.
<h1>Declarations</h1>
Earlier in this tutorial, you learned that functions are declared with the following syntax:
<pre>
function functionName(parameters) {
  // code to be executed
}
</pre>
Declared functions are not executed immediately. They are "saved for later use", and will be executed later, when they are invoked (called upon).
<pre>
function myFunction(a, b) {
  return a * b;
}
</pre>
<h1>Expressions</h1>
A JavaScript function can also be defined using an expression.
<br>
A function expression can be stored in a variable:
<pre>const x = function (a, b) {return a * b};</pre>
After a function expression has been stored in a variable, the variable can be used as a function:
<pre>
const x = function (a, b) {return a * b};
let z = x(4, 3);
</pre>
The function above is actually an anonymous function (a function without a name).
<br>
Functions stored in variables do not need function names. They are always invoked (called) using the variable name.
<h1>Function()</h1>
As you have seen in the previous examples, JavaScript functions are defined with the function keyword.
<br>
Functions can also be defined with a built-in JavaScript function constructor called Function().
<pre>
const myFunction = new Function("a", "b", "return a * b");
let x = myFunction(4, 3);
</pre>
You actually don't have to use the function constructor. The example above is the same as writing:
<pre>
const myFunction = function (a, b) {return a * b};
let x = myFunction(4, 3);
</pre>
<h1>Hoisting</h1>
Earlier in this tutorial, you learned about "hoisting" (JavaScript Hoisting).
<br>
Hoisting is JavaScript's default behavior of moving declarations to the top of the current scope.
<br>
Hoisting applies to variable declarations and to function declarations.
<br>
Because of this, JavaScript functions can be called before they are declared:
<pre>
myFunction(5);
function myFunction(y) {
  return y * y;
}
</pre>
Functions defined using an expression are not hoisted.
<h1>Self-Invoking Functions</h1>
Function expressions can be made "self-invoking".
<br>
A self-invoking expression is invoked (started) automatically, without being called.
<br>
Function expressions will execute automatically if the expression is followed by ().
<br>
You cannot self-invoke a function declaration.
<br>
You have to add parentheses around the function to indicate that it is a function expression:
<pre>
(function () {
  let x = "Hello!!";  // I will invoke myself
})();
</pre>
The function above is actually an anonymous self-invoking function (function without name).
<h1>Functions Can Be Used as Values</h1>
JavaScript functions can be used as values:
<pre>
function myFunction(a, b) {
  return a * b;
}
let x = myFunction(4, 3);
</pre>
JavaScript functions can be used in expressions:
<pre>
function myFunction(a, b) {
  return a * b;
}
let x = myFunction(4, 3) * 2;
</pre>
<h1>Functions are Objects</h1>
The typeof operator in JavaScript returns "function" for functions.
<br>
But, JavaScript functions can best be described as objects.
<br>
JavaScript functions have both properties and methods.
<br>
The arguments.length property returns the number of arguments received when the function was invoked:
<pre>
function myFunction(a, b) {
  return arguments.length;
}
</pre>
The toString() method returns the function as a string:
<pre>
function myFunction(a, b) {
  return a * b;
}
let text = myFunction.toString();
</pre>
<h1>Arrow Functions</h1>
Arrow functions allows a short syntax for writing function expressions.
<br>
You don't need the function keyword, the return keyword, and the curly brackets.
<pre>
// ES5
var x = function(x, y) {
  return x * y;
}
</pre>
<pre>
// ES6
const x = (x, y) => x * y;
</pre>
Arrow functions do not have their own this. They are not well suited for defining object methods.
<br>
Arrow functions are not hoisted. They must be defined before they are used.
<br>
Using const is safer than using var, because a function expression is always constant value.
<br>
You can only omit the return keyword and the curly brackets if the function is a single statement. Because of this, it might be a good habit to always keep them:
<pre>const x = (x, y) => { return x * y };</pre>
