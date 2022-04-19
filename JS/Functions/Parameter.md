<a href="/JS/Functions/Definition.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Functions/Invocation.md">Next &gt;</a>
<hr>
A JavaScript function does not perform any checking on parameter values (arguments).
<h1>Parameters and Arguments</h1>
Earlier in this tutorial, you learned that functions can have parameters:
<pre>
function functionName(parameter1, parameter2, parameter3) {
  // code to be executed
}
</pre>
Function parameters are the names listed in the function definition.
<br>
Function arguments are the real values passed to (and received by) the function.
<h1>Parameter Rules</h1>
JavaScript function definitions do not specify data types for parameters.
<br>
JavaScript functions do not perform type checking on the passed arguments.
<br>
JavaScript functions do not check the number of arguments received.
<h1>Default Parameters</h1>
If a function is called with missing arguments (less than declared), the missing values are set to undefined.
<br>
Sometimes this is acceptable, but sometimes it is better to assign a default value to the parameter:
<pre>
function myFunction(x, y) {
  if (y === undefined) {
    y = 2;
  }
}
</pre>
ECMAScript 2015 allows default parameter values in the function declaration:
<pre>
function myFunction(x, y = 2) {
  // function code
}
</pre>
<h1>The Arguments Object</h1>
JavaScript functions have a built-in object called the arguments object.
<br>
The argument object contains an array of the arguments used when the function was called (invoked).
<br>
This way you can simply use a function to find (for instance) the highest value in a list of numbers:
<pre>
x = findMax(1, 123, 500, 115, 44, 88);
function findMax() {
  let max = -Infinity;
  for (let i = 0; i < arguments.length; i++) {
    if (arguments[i] > max) {
      max = arguments[i];
    }
  }
  return max;
}
</pre>
Or create a function to sum all input values:
<pre>
x = sumAll(1, 123, 500, 115, 44, 88);
function sumAll() {
  let sum = 0;
  for (let i = 0; i < arguments.length; i++) {
    sum += arguments[i];
  }
  return sum;
}
</pre>
If a function is called with too many arguments (more than declared), these arguments can be reached using the arguments object.
<h1>Arguments are Passed by Value</h1>
The parameters, in a function call, are the function's arguments.
<br>
JavaScript arguments are passed by value: The function only gets to know the values, not the argument's locations.
<br>
If a function changes an argument's value, it does not change the parameter's original value.
<br>
Changes to arguments are not visible (reflected) outside the function.
<h1>Objects are Passed by Reference</h1>
In JavaScript, object references are values.
<br>
Because of this, objects will behave like they are passed by reference:
<br>
If a function changes an object property, it changes the original value.
<br>
Changes to object properties are visible (reflected) outside the function.
