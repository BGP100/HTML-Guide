<a href="/JS/Math/Comparison.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Switch.md">Next &gt;</a>
<hr>
Very often when you write code, you want to perform different actions for different decisions.
<br>
You can use conditional statements in your code to do this.
<br>
In JavaScript we have the following conditional statements:
<ul>
  <li>Use <a href="#if">if</a> to specify a block of code to be executed, if a specified condition is true.</li>
  <li>Use <a href="#else">else</a> to specify a block of code to be executed, if the same condition is false.</li>
  <li>Use <a href="#else-if">else if</a> to specify a new condition to test, if the first condition is false.</li>
  <li>Use <a href="Switch.md">switch</a> to specify many alternative blocks of code to be executed.</li>
</ul>
<h1>if</h1>
Use the if statement to specify a block of JavaScript code to be executed if a condition is true.
<br>
<b>Syntax:</b>
<pre>
if (<i>condition</i>) {
  //  block of code to be executed if the condition is true
}
</pre>
<b><i>Note:</i></b> if keyword <b>if</b> is in lowercase letters. Uppercase letters (If, iF, or IF) will generate a JavaScript error.
<br>
The result would write "Good Day" only if is 17:59 or less:
<pre>
if (hour &lt; 18) {
  greeting = "Good Day";
}
</pre>
<h1>else</h1>
Use the else statement to specify a block of code to be executed if the condition is false.
<br>
<b>Syntax:</b>
<pre>
if (<i>condition</i>) {
  //  block of code to be executed if the condition is true
} else {
  //  block of code to be executed if the condition is false
}
</pre>
The result would write "Good Day" only if is 17:59 or less, and if its 18:00 or more it will write "Good Evening":
<pre>
if (hour &lt; 18) {
  greeting = "Good Day";
} else {
  greeting = "Good Evening";
}
</pre>
<h1>else if</h1>
Use the else if statement to specify a new condition if the first condition is false.
<br>
<b>Syntax:</b>
<pre>
if (<i>condition1</i>) {
  //  block of code to be executed if condition1 is true
} else if (<i>condition2</i>) {
  //  block of code to be executed if the condition1 is false and condition2 is true
} else {
  //  block of code to be executed if the condition1 is false and condition2 is false
}
</pre>
The result would write "Good Morning" only if is 17:59 or less, and if its 18:00 or less it will write "Good Day", and if any of the previous <b>if</b> don't match it will write "Good Evening":
<pre>
if (time &lt; 10) {
  greeting = "Good Morning";
} else if (time &lt; 20) {
  greeting = "Good Day";
} else {
  greeting = "Good Evening";
}
</pre>
