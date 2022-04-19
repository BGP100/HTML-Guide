<a href="/JS/Functions/Parameter.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Functions/Method/Call.md">Next &gt;</a>
<hr>
The code inside a JavaScript function will execute when "something" invokes it.
<h1>Invoking a JavaScript Function</h1>
The code inside a function is not executed when the function is defined.
<br>
The code inside a function is executed when the function is invoked.
<br>
It is common to use the term "call a function" instead of "invoke a function".
<br>
It is also common to say "call upon a function", "start a function", or "execute a function".
<br>
In this tutorial, we will use invoke, because a JavaScript function can be invoked without being called.
<h1>Invoking a Function as a Function</h1>
<pre>
function myFunction(a, b) {
  return a * b;
}
myFunction(10, 2); // Will return 20
</pre>
The function above does not belong to any object. But in JavaScript there is always a default global object.
<br>
In HTML the default global object is the HTML page itself, so the function above "belongs" to the HTML page.
<br>
In a browser the page object is the browser window. The function above automatically becomes a window function.
<br>
myFunction() and window.myFunction() is the same function:
<pre>
function myFunction(a, b) {
  return a * b;
}
window.myFunction(10, 2); // Will also return 20
</pre>
<h1>What is the this Keyword?</h1>
In JavaScript, the <b>this</b> keyword refers to an object.
<br>
Which object depends on how <b>this</b> is being invoked (used or called).
<br>
The <b>this</b> keyword refers to different objects depending on how it is used:
<ul>
  <li>In an object method, <b>this</b> refers to the object.</li>
  <li>Alone, <b>this</b> refers to the global object.</li>
  <li>In a function, <b>this</b> refers to the global object.</li>
  <li>In a function, in strict mode, <b>this</b> is undefined.</li>
  <li>In an event, <b>this</b> refers to the element that received the event.</li>
  <li>Methods like <b>call()</b>, <b>apply()</b>, and <b>bind()</b> can refer <b>this</b> to any object.</li>
</ul>
<h1>The Global Object</h1>
When a function is called without an owner object, the value of this becomes the global object.
<br>
In a web browser the global object is the browser window.
<br>
This example returns the window object as the value of this:
<pre>
let x = myFunction(); // x will be the window object
function myFunction() {
  return this;
}
</pre>
<h1>Invoking a Function as a Method</h1>
In JavaScript you can define functions as object methods.
<br>
The following example creates an object (myObject), with two properties (firstName and lastName), and a method (fullName):
<pre>
const myObject = {
  firstName:"John",
  lastName: "Doe",
  fullName: function () {
    return this.firstName + " " + this.lastName;
  }
}
myObject.fullName(); // Will return "John Doe"
</pre>
The fullName method is a function. The function belongs to the object. myObject is the owner of the function.
<br>
The thing called this, is the object that "owns" the JavaScript code. In this case the value of this is myObject.
<br>
Test it! Change the fullName method to return the value of this:
<pre>
const myObject = {
  firstName:"John",
  lastName: "Doe",
  fullName: function () {
    return this;
  }
}
// This will return [object Object] (the owner object)
myObject.fullName();
</pre>
Invoking a function as an object method, causes the value of this to be the object itself.
<h1>Invoking a Function with a Function Constructor</h1>
If a function invocation is preceded with the new keyword, it is a constructor invocation.
<br>
It looks like you create a new function, but since JavaScript functions are objects you actually create a new object:
<pre>
// This is a function constructor:
function myFunction(arg1, arg2) {
  this.firstName = arg1;
  this.lastName  = arg2;
}
// This creates a new object
const myObj = new myFunction("John", "Doe");
// This will return "John"
myObj.firstName;
</pre>
A constructor invocation creates a new object. The new object inherits the properties and methods from its constructor.
