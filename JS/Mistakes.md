<a href="/JS/Practices.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Performance.md">Next &gt;</a>
<hr>
<h1>Accidentally Using the Assignment Operator</h1>
JavaScript programs may generate unexpected results if a programmer accidentally uses an assignment operator (<code>=</code>), instead of a comparison operator (<code>==</code>) in an if statement.
<br>
This <b>if</b> statement returns <b>false</b> (as expected) because x is not equal to 10:
<pre>
let x = 0;
if (x == 10)
</pre>
This <b>if</b> statement returns <b>true</b> (maybe not as expected), because 10 is true:
<pre>
let x = 0;
if (x = 10)
</pre>
This <b>if</b> statement returns <b>false</b> (maybe not as expected), because 0 is false:
<pre>
let x = 0;
if (x = 0)
</pre>
<h1>Expecting Loose Comparison</h1>
In regular comparison, data type does not matter. This <b>if</b> statement returns true:
<pre>
let x = 10;
let y = "10";
if (x == y)
</pre>
In strict comparison, data type does matter. This <b>if</b> statement returns false:
<pre>
let x = 10;
let y = "10";
if (x === y)
</pre>
It is a common mistake to forget that <b>switch</b> statements use strict comparison:
<br>
This <b>case switch</b> will display an alert:
<pre>
let x = 10;
switch(x) {
  case 10: alert("Hello");
}
</pre>
This <b>case switch</b> will not display an alert:
<pre>
let x = 10;
switch(x) {
  case "10": alert("Hello");
}
</pre>
<h1>Confusing Addition & Concatenation</h1>
Addition is about adding numbers.
<br>
Concatenation is about adding strings.
<br>
In JavaScript both operations use the same + operator.
<br>
Because of this, adding a number as a number will produce a different result from adding a number as a string:
<pre>
let x = 10;
x = 10 + 5;       // Now x is 15
let y = 10;
y += "5";        // Now y is "105"
</pre>
When adding two variables, it can be difficult to anticipate the result:
<pre>
let x = 10;
let y = 5;
let z = x + y;     // Now z is 15
let x = 10;
let y = "5";
let z = x + y;     // Now z is "105"
</pre>
<h1>Misunderstanding Floats</h1>
All numbers in JavaScript are stored as 64-bits Floating point numbers (Floats).
<br>
All programming languages, including JavaScript, have difficulties with precise floating point values:
<pre>
let x = 0.1;
let y = 0.2;
let z = x + y // the result in z will not be 0.3
</pre>
To solve the problem above, it helps to multiply and divide:
<pre>let z = (x * 10 + y * 10) / 10; // z will be 0.3</pre>
<h1>Breaking a JavaScript String</h1>
JavaScript will allow you to break a statement into two lines:
<pre>let x ="Hello World!";</pre>
<h1>Misplacing Semicolon</h1>
Because of a misplaced semicolon, this code block will execute regardless of the value of x:
<pre>
if (x == 19);
{
  // code block 
}
</pre>
<h1>Breaking a Return Statement</h1>
It is a default JavaScript behavior to close a statement automatically at the end of a line.
<br>
Because of this, these two examples will return the same result:
<pre>
function myFunction(a) {
  let power = 10 
  return a * power
}
</pre>
<h1>Explanation</h1>
If a statement is incomplete like:
<pre>let</pre>
JavaScript will try to complete the statement by reading the next line:
<pre>power = 10;</pre>
But since this statement is complete:
<pre>return</pre>
JavaScript will automatically close it like this:
<pre>return;</pre>
This happens because closing (ending) statements with semicolon is optional in JavaScript.
<br>
JavaScript will close the return statement at the end of the line, because it is a complete statement.
<h1>Accessing Arrays with Named Indexes</h1>
Many programming languages support arrays with named indexes.
<br>
Arrays with named indexes are called associative arrays (or hashes).
<br>
JavaScript does not support arrays with named indexes.
<br>
In JavaScript, arrays use numbered indexes:  
<pre>
const person = [];
person[0] = "John";
person[1] = "Doe";
person[2] = 46;
person.length; // person.length will return 3
person[0]; // person[0] will return "John"
</pre>
In JavaScript, objects use named indexes.
<br>
If you use a named index, when accessing an array, JavaScript will redefine the array to a standard object.
<br>
After the automatic redefinition, array methods and properties will produce undefined or incorrect results:
<pre>
const person = [];
person["firstName"] = "John";
person["lastName"] = "Doe";
person["age"] = 46;
person.length; // person.length will return 0
person[0]; // person[0] will return undefined
</pre>
<h1>Ending Definitions with a Comma</h1>
Trailing commas in object and array definition are legal in ECMAScript 5.
<pre>person = {firstName:"John", lastName:"Doe", age:46,}</pre>
<pre>points = [40, 100, 1, 5, 25, 10,];</pre>
<b>WARNING!!!</b>
<br>
Internet Explorer 8 will crash.
<br>
JSON does not allow trailing commas.
<h1>Undefined is Not Null</h1>
JavaScript objects, variables, properties, and methods can be undefined.
<br>
In addition, empty JavaScript objects can have the value null.
<br>
This can make it a little bit difficult to test if an object is empty.
<br>
You can test if an object exists by testing if the type is undefined:
<pre>if (typeof myObj === "undefined") // Correct</pre>
But you cannot test if an object is null, because this will throw an error if the object is undefined:
<pre>if (myObj === null) // Incorrect</pre>
