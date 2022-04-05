A JavaScript function is a block of code designed to perform a particular task.
<br>
A JavaScript function is executed when "something" invokes it (calls it).
<pre>
function myFunction(p1, p2) {
  return p1 * p2; // The function returns the product of p1 and p2
}
</pre>
<h1>Syntax</h1>
A JavaScript function is defined with the <b>function</b> keyword, followed by a name, followed by parentheses ().
<br>
Function names can contain letters, digits, underscores, and dollar signs (same rules as variables).
<br>
The parentheses may include parameter names separated by commas:
<br>
<b>(parameter1, parameter2, ...)</b>
<br>
The code to be executed, by the function, is placed inside curly brackets: { }
<pre>
function name(parameter1, parameter2, parameter3) {
  // code to be executed
}
</pre>
Function parameters are listed inside the parentheses () in the function definition.
<br>
Function arguments are the values received by the function when it is invoked.
<br>
Inside the function, the arguments (the parameters) behave as local variables.
<h1>Invocation</h1>
The code inside the function will execute when "something" invokes (calls) the function:
<ul>
  <li>When an event occurs (when a user clicks a button)</li>
  <li>When it is invoked (called) from JavaScript code</li>
  <li>Automatically (self invoked)</li>
  <li>You will learn a lot more about function invocation later in this tutorial.</li>
</ul>
<h1>Return</h1>
When JavaScript reaches a return statement, the function will stop executing.
<br>
If the function was invoked from a statement, JavaScript will "return" to execute the code after the invoking statement.
<br>
Functions often compute a return value. The return value is "returned" back to the "caller":
<pre>let x = myFunction(4, 3); // Function is called, return value will end up in x</pre>
<pre>
function myFunction(a, b) {
  return a * b; // Function returns the product of a and b
}
</pre>
The result in x will be: <code>12</code>
<h1>Why 'Function'?</h1>
You can reuse code: Define the code once, and use it many times.
<br>
You can use the same code many times with different arguments, to produce different results.
<pre>
function toCelsius(fahrenheit) {
  return (5/9) * (fahrenheit-32);
}
document.getElementById("demo").innerHTML = toCelsius(77);
</pre>
<h1>The () Operator</h1>
Using the example above, <b>toCelsius</b> refers to the function object, and <b>toCelsius()</b> refers to the function result.
<br>
Accessing a function without () will return the function object instead of the function result.
<pre>
function toCelsius(fahrenheit) {
  return (5/9) * (fahrenheit-32);
}
document.getElementById("demo").innerHTML = toCelsius;
</pre>
<h1>Functions Used as Variable Values</h1>
Functions can be used the same way as you use variables, in all types of formulas, assignments, and calculations.
<pre>
let x = toCelsius(77);
let text = "The temperature is " + x + " Celsius";
You can use the function directly, as a variable value:
let text = "The temperature is " + toCelsius(77) + " Celsius";
</pre>
<h1>Local Variables</h1>
Local Variables
Variables declared within a JavaScript function, become LOCAL to the function.
<br>
Local variables can only be accessed from within the function.
<pre>
// code here can NOT use carName=
function myFunction() {
  let carName = "Volvo";
  // code here CAN use carName
}
// code here can NOT use carName
</pre>
Since local variables are only recognized inside their functions, variables with the same name can be used in different functions.
<br>
Local variables are created when a function starts, and deleted when the function is completed.
