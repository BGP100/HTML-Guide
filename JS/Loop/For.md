<a href="/JS/Crash.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Loop/For-In.md">Next &gt;</a>
<hr>
Loops can execute a block of code a number of times.
<br>
Loops are handy, if you want to run the same code over and over again, each time with a different value.
<br>
Often this is the case when working with arrays:
<br>
Instead of writing:
<pre>
text += cars[0] + "&lt;br&gt;";
text += cars[1] + "&lt;br&gt;";
text += cars[2] + "&lt;br&gt;";
text += cars[3] + "&lt;br&gt;";
text += cars[4] + "&lt;br&gt;";
text += cars[5] + "&lt;br&gt;";
</pre>
You can write:
<pre>
for (let i = 0; i < cars.length; i++) {
  text += cars[i] + "<br>";
}
</pre>
<h1>Different Kinds of Loops</h1>
JavaScript supports different kinds of loops:
<ul>
  <li><b>for</b> - loops through a block of code a number of times.</li>
  <li><b>for/in</b> - loops through the properties of an object.</li>
  <li><b>for/of</b> - loops through the values of an iterable object.</li>
  <li><b>while</b> - loops through a block of code while a specified condition is true.</li>
  <li><b>do/while</b> - also loops through a block of code while a specified condition is true.</li>
</ul>
<h1>Syntax</h1>
The for loop has the following syntax:
<pre>
for (statement 1; statement 2; statement 3) {
  // code block to be executed
}
</pre>
Statement 1 is executed (one time) before the execution of the code block.
<br>
Statement 2 defines the condition for executing the code block.
<br>
Statement 3 is executed (every time) after the code block has been executed.
<pre>
for (let i = 0; i < 5; i++) {
  text += "The number is " + i + "<br>";
}
</pre>
From the example above, you can read:
<br>
Statement 1 sets a variable before the loop starts (let i = 0).
<br>
Statement 2 defines the condition for the loop to run (i must be less than 5).
<br>
Statement 3 increases a value (i++) each time the code block in the loop has been executed.
<h2>Statement 1</h2>
Normally you will use statement 1 to initialize the variable used in the loop (let i = 0).
<br>
This is not always the case, JavaScript doesn't care. Statement 1 is optional.
<br>
You can initiate many values in statement 1 (separated by comma):
<pre>
for (let i = 0, len = cars.length, text = ""; i < len; i++) {
  text += cars[i] + "<br>";
}
</pre>
And you can omit statement 1 (like when your values are set before the loop starts):
<pre>
let i = 2;
let len = cars.length;
let text = "";
for (; i < len; i++) {
  text += cars[i] + "<br>";
}
</pre>
<h2>Statement 2</h2>
Often statement 2 is used to evaluate the condition of the initial variable.
<br>
This is not always the case, JavaScript doesn't care. Statement 2 is also optional.
<br>
If statement 2 returns true, the loop will start over again, if it returns false, the loop will end.
<h2>Statement 3</h2>
Often statement 3 increments the value of the initial variable.
<br>
This is not always the case, JavaScript doesn't care, and statement 3 is optional.
<br>
Statement 3 can do anything like negative increment (i--), positive increment (i = i + 15), or anything else.
<br>
Statement 3 can also be omitted (like when you increment your values inside the loop):
<pre>
let i = 0;
let len = cars.length;
let text = "";
for (; i < len; ) {
  text += cars[i] + "<br>";
  i++;
}
</pre>
<h1>Loop Scope</h1>
Using var in a loop:
<pre>
var i = 5;
for (var i = 0; i < 10; i++) {
  // some code
}
// Here i is 10
</pre>
Using let in a loop:
<pre>
let i = 5;
for (let i = 0; i < 10; i++) {
  // some code
}
// Here i is 5
</pre>
In the first example, using var, the variable declared in the loop redeclares the variable outside the loop.
<br>
In the second example, using let, the variable declared in the loop does not redeclare the variable outside the loop.
<br>
When let is used to declare the i variable in a loop, the i variable will only be visible within the loop.
