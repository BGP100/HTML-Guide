<code>"use strict";</code> Defines that JavaScript code should be executed in "strict mode".
<hr>
The <code>"use strict"</code> directive was new in ECMAScript version 5.
<br>
It is not a statement, but a literal expression, ignored by earlier versions of JavaScript.
<br>
The purpose of <code>"use strict"</code> is to indicate that the code should be executed in "strict mode".
<br>
With strict mode, you can not, for example, use undeclared variables.
<h1>Browser Support</h1>
All modern browsers support "use strict" except Internet Explorer 9 and lower:
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
    <td>13.0</td>
    <td>10.0</td>
    <td>4.0</td>
    <td>6.0</td>
    <td>12.1</td>
  </tr>
</table>
The numbers in the table specify the first browser version that fully supports the directive.
<h1>Declaring It</h1>
Strict mode is declared by adding "use strict"; to the beginning of a script or a function.
<br>
Declared at the beginning of a script, it has global scope (all code in the script will execute in strict mode):
<pre>
"use strict";
x = 3.14; // This will cause an error because x is not declared
</pre>
<pre>
"use strict";
myFunction();
function myFunction() {
  y = 3.14; // This will also cause an error because y is not declared
}
</pre>
Declared inside a function, it has local scope (only the code inside the function is in strict mode):
<pre>
x = 3.14; // This will not cause an error.
myFunction();
function myFunction() {
  "use strict";
  y = 3.14; // This will cause an error
}
</pre>
<h1>Syntax</h1>
The syntax, for declaring strict mode, was designed to be compatible with older versions of JavaScript.
<br>
Compiling a numeric literal (4 + 5;) or a string literal ("John Doe";) in a JavaScript program has no side effects. It simply compiles to a non existing variable and dies.
<br>
So "use strict"; only matters to new compilers that "understand" the meaning of it.
<h1>Why Strict Mode?</h1>
Strict mode makes it easier to write "secure" JavaScript.
<br>
Strict mode changes previously accepted "bad syntax" into real errors.
<br>
As an example, in normal JavaScript, mistyping a variable name creates a new global variable. In strict mode, this will throw an error, making it impossible to accidentally create a global variable.
<br>
In normal JavaScript, a developer will not receive any error feedback assigning values to non-writable properties.
<br>
In strict mode, any assignment to a non-writable property, a getter-only property, a non-existing property, a non-existing variable, or a non-existing object, will throw an error.
<h1>Not Allowed in Strict Mode</h1>
Using a variable, without declaring it, is not allowed:
<pre>
"use strict";
x = 3.14; // This will cause an error
</pre>
<b>Note:</b> Objects are variables too.
<br>
Using an object, without declaring it, is not allowed:
<pre>
"use strict";
x = {p1:10, p2:20}; // This will cause an error
</pre>
Deleting a variable (or object) is not allowed.
<pre>
"use strict";
let x = 3.14;
delete x; // This will cause an error
</pre>
Deleting a function is not allowed.
<pre>
"use strict";
function x(p1, p2) {};
delete x; // This will cause an error 
</pre>
Duplicating a parameter name is not allowed:
<pre>
"use strict";
function x(p1, p1) {}; // This will cause an error
</pre>
Octal numeric literals are not allowed:
<pre>
"use strict";
let x = 010; // This will cause an error
</pre>
Octal escape characters are not allowed:
<pre>
"use strict";
let x = "\010"; // This will cause an error
</pre>
Writing to a read-only property is not allowed:
<pre>
"use strict";
const obj = {};
Object.defineProperty(obj, "x", {value:0, writable:false});
obj.x = 3.14; // This will cause an error
</pre>
Writing to a get-only property is not allowed:
<pre>
"use strict";
const obj = {get x() {return 0} };
obj.x = 3.14; // This will cause an error
</pre>
Deleting an undeletable property is not allowed:
<pre>
"use strict";
delete Object.prototype; // This will cause an error
</pre>
The word eval cannot be used as a variable:
<pre>
"use strict";
let eval = 3.14; // This will cause an error
</pre>
The word arguments cannot be used as a variable:
<pre>
"use strict";
let arguments = 3.14; // This will cause an error
</pre>
The with statement is not allowed:
<pre>
"use strict";
with (Math){x = cos(2)}; // This will cause an error
</pre>
For security reasons, eval() is not allowed to create variables in the scope from which it was called:
<pre>
"use strict";
eval ("let x = 2");
alert (x); // This will cause an error
</pre>
The <b>this</b> keyword in functions behaves differently in strict mode.
<br>
The <b>this</b> keyword refers to the object that called the function.
<br>
If the object is not specified, functions in strict mode will return <b>undefined</b> and functions in normal mode will return the global object (window):
<pre>
"use strict";
function myFunction() {
  alert(this); // will alert "undefined"
}
myFunction();
</pre>
<h1>Future Proof!</h1>
Keywords reserved for future JavaScript versions can NOT be used as variable names in strict mode.
<br>
These are:
<ul>
  <li><code>implements</code></li>
  <li><code>interface</code></li>
  <li><code>let</code></li>
  <li><code>package</code></li>
  <li><code>private</code></li>
  <li><code>protected</code></li>
  <li><code>public</code></li>
  <li><code>static</code></li>
  <li><code>yield</code></li>
  <li><code>"use strict";</code></li>
  <li><code>let public = 1500; // This will cause an error</code></li>
</ul>
<h1>Watch Out!</h1>
The "use strict" directive is only recognized at the beginning of a script or a function.
