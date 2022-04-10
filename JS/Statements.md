<a href="/JS/Output.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Syntax.md">Next &gt;</a>
<hr>
A computer program is a list of "instructions" to be "executed" by a computer.
<br>
In a programming language, these programming instructions are called statements.
<br>
A JavaScript program is a list of programming statements.
<pre>
let x, y, z; // Statement 1
x = 5; // Statement 2
y = 6; // Statement 3
z = x + y; // Statement 4
</pre>
JavaScript statements are composed of:
<br>
Values, Operators, Expressions, Keywords, and Comments.
<br>
This statement tells the browser to write "Hello Dolly." inside an HTML element with id="demo":
<pre>document.getElementById("demo").innerHTML = "Hello Dolly.";</pre>
Most JavaScript programs contain many JavaScript statements.
<br>
The statements are executed, one by one, in the same order as they are written.
<h1>Semicolons</h1>
Semicolons separate JavaScript statements.
<br>
Add a semicolon at the end of each executable statement:
<pre>
let a, b, c; // Declare 3 variables
a = 5; // Assign the value 5 to a
b = 6; // Assign the value 6 to b
c = a + b; // Assign the sum of a and b to c
</pre>
When separated by semicolons, multiple statements on one line are allowed:
<pre>a = 5; b = 6; c = a + b;</pre>
<h1>White Space</h1>
JavaScript ignores multiple spaces. You can add white space to your script to make it more readable.
<br>
The following lines are equivalent:
<pre>
let person = "Hege";
let person="Hege";
</pre>
A good practice is to put spaces around operators ( = + - * / ):
<pre>let x = y + z;</pre>
<h1>Line Length &amp; Line Breaks</h1>
For best readability, programmers often like to avoid code lines longer than 80 characters.
<br>
If a JavaScript statement does not fit on one line, the best place to break it is after an operator:
<pre>document.getElementById("demo").innerHTML =<br>"Hello Dolly!";</pre>
<h1>Code Breaks</h1>
JavaScript statements can be grouped together in code blocks, inside curly brackets {...}.
<br>
The purpose of code blocks is to define statements to be executed together.
<br>
One place you will find statements grouped together in blocks, is in JavaScript functions:
<pre>
function myFunction() {
  document.getElementById("demo1").innerHTML = "Hello Dolly!";
  document.getElementById("demo2").innerHTML = "How are you?";
}
</pre>
<h1>JavaScript Keywords</h1>
<table class="ws-table-all" style="width: 100%">
  <tr>
    <th>Keyword</th>
    <th>Description</th>
  </tr>
  <tr>
    <td class="notranslate">var</td>
    <td>Declares a variable</td>
  </tr>
  <tr>
    <td class="notranslate">let</td>
    <td>Declares a block variable</td>
  </tr>
  <tr>
    <td class="notranslate">const</td>
    <td>Declares a block constant</td>
  </tr>
  <tr>
    <td class="notranslate">if</td>
    <td>Marks a block of statements to be executed on a condition</td>
  </tr>
  <tr>
    <td class="notranslate">switch</td>
    <td>Marks a block of statements to be executed in different cases</td>
  </tr>
  <tr>
    <td class="notranslate">for</td>
    <td>Marks a block of statements to be executed in a loop</td>
  </tr>
  <tr>
    <td class="notranslate">function</td>
    <td>Declares a function</td>
  </tr>
  <tr>
    <td class="notranslate">return</td>
    <td>Exits a function</td>
  </tr>
  <tr>
    <td class="notranslate">try</td>
    <td>Implements error handling to a block of statements</td>
  </tr>
</table>
