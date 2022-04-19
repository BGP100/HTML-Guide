<a href="/JS/Functions/Method/Bind.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Classes/Main.md">Next &gt;</a>
<hr>
JavaScript variables can belong to the local or global scope.
<br>
Global variables can be made local (private) with closures.
<h1>Global Variables</h1>
A function can access all variables defined inside the function, like this:
<pre>
function myFunction() {
  let a = 4;
  return a * a;
}
</pre>
But a function can also access variables defined outside the function, like this:

Example
let a = 4;
function myFunction() {
  return a * a;
}
In the last example, a is a global variable.
<br>
In a web page, global variables belong to the window object.
<br>
Global variables can be used (and changed) by all scripts in the page (and in the window).
<br>
In the first example, a is a local variable.
<br>
A local variable can only be used inside the function where it is defined. It is hidden from other functions and other scripting code.
<br>
Global and local variables with the same name are different variables. Modifying one, does not modify the other.
<b>Note:</b> Variables created without a declaration keyword (<b>var</b>, <b>let</b>, or <b>const</b>) are always global, even if they are created inside a function:
<pre>
function myFunction() {
  a = 4;
}
</pre>
<h1>Variable Lifetime</h1>
Global variables live until the page is discarded, like when you navigate to another page or close the window.
<br>
Local variables have short lives. They are created when the function is invoked, and deleted when the function is finished.
<h1>A Counter Dilemma</h1>
Suppose you want to use a variable for counting something, and you want this counter to be available to all functions.
<br>
You could use a global variable, and a function to increase the counter:
<pre>
// Initiate counter
let counter = 0;
// Function to increment counter
function add() {
  counter += 1;
}
// Call add() 3 times
add();
add();
add();
// The counter should now be 3
</pre>
There is a problem with the solution above: Any code on the page can change the counter, without calling add().
<br>
The counter should be local to the add() function, to prevent other code from changing it:
<pre>
// Initiate counter
let counter = 0;
// Function to increment counter
function add() {
  let counter = 0;
  counter += 1;
}
// Call add() 3 times
add();
add();
add();
// The counter should now be 3. But it is 0
</pre>
It did not work because we display the global counter instead of the local counter.
<br>
We can remove the global counter and access the local counter by letting the function return it:
<pre>
// Function to increment counter
function add() {
  let counter = 0;
  counter += 1;
  return counter;
}
// Call add() 3 times
add();
add();
add();
//The counter should now be 3. But it is 1.
</pre>
It did not work because we reset the local counter every time we call the function.
<br>
A JavaScript inner function can solve this.
<h1>Nested Functions</h1>
All functions have access to the global scope.  
<br>
In fact, in JavaScript, all functions have access to the scope "above" them.
<br>
JavaScript supports nested functions. Nested functions have access to the scope "above" them.
<br>
In this example, the inner function plus() has access to the counter variable in the parent function:
<pre>
function add() {
  let counter = 0;
  function plus() {counter += 1;}
  plus();   
  return counter;
}
</pre>
This could have solved the counter dilemma, if we could reach the plus() function from the outside.
<br>
We also need to find a way to execute counter = 0 only once.
<br>
We need a closure.
<h1>Example</h1>
Remember self-invoking functions? What does this function do?
<pre>
const add = (function () {
  let counter = 0;
  return function () {counter += 1; return counter}
})();
add();
add();
add();
// the counter is now 3
</pre>
<b>Explained:</b>
<br>
The variable add is assigned to the return value of a self-invoking function.
<br>
The self-invoking function only runs once. It sets the counter to zero (0), and returns a function expression.
<br>
This way add becomes a function. The "wonderful" part is that it can access the counter in the parent scope.
<br>
This is called a JavaScript closure. It makes it possible for a function to have "private" variables.
<br>
The counter is protected by the scope of the anonymous function, and can only be changed using the add function.
