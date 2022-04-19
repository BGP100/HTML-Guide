<a href="/JS/This.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Modules.md">Next &gt;</a>
<hr>
Arrow functions were introduced in ES6.
<br>
Arrow functions allow us to write shorter function syntax:
<pre>let myFunction = (a, b) => a * b;</pre>
<hr>
Before:
<pre>
hello = function() {
  return "Hello World!";
}
</pre>
With Arrow Function:
<pre>
hello = () => {
  return "Hello World!";
}
</pre>
It gets shorter! If the function has only one statement, and the statement returns a value, you can remove the brackets and the return keyword:
<pre>hello = () => "Hello World!";</pre>
<h1>What About <b>this</b> Keyword?</h1>
The handling of this is also different in arrow functions compared to regular functions.
<br>
In short, with arrow functions there are no binding of this.
<br>
In regular functions the this keyword represented the object that called the function, which could be the window, the document, a button or whatever.
<br>
With arrow functions the this keyword always represents the object that defined the arrow function.
<br>
Let us take a look at two examples to understand the difference.
<br>
Both examples call a method twice, first when the page loads, and once again when the user clicks a button.
<br>
The first example uses a regular function, and the second example uses an arrow function.
<br>
The result shows that the first example returns two different objects (window and button), and the second example returns the window object twice, because the window object is the "owner" of the function.
<br>
With a regular function this represents the object that calls the function:
<pre>
// Regular Function:
hello = function() {
  document.getElementById("demo").innerHTML += this;
}
// The window object calls the function:
window.addEventListener("load", hello);
// A button object calls the function:
document.getElementById("btn").addEventListener("click", hello);
</pre>
With an arrow function this represents the owner of the function:
<pre>
// Arrow Function:
hello = () => {
  document.getElementById("demo").innerHTML += this;
}
// The window object calls the function:
window.addEventListener("load", hello);
// A button object calls the function:
document.getElementById("btn").addEventListener("click", hello);
</pre>
Remember these differences when you are working with functions. Sometimes the behavior of regular functions is what you want, if not, use arrow functions.
<h1>Browser Support</h1>
The following table defines the first browser versions with full support for Arrow Functions in JavaScript:
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
    <td>45.0</td>
    <td>12.0</td>
    <td>22.0</td>
    <td>10.0</td>
    <td>32.0</td>
  </tr>
</table>
