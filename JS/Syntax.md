<a href="/JS/Statements.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Comments.md">Next &gt;</a>
<hr>
The JavaScript syntax defines two types of values:
<ul>
  <li>Fixed values</li>
  <li>Variable values</li>
  <li>Fixed values are called Literals.</li>
</ul>
Variable values are called Variables.
<h1>Literals</h1>
The two most important syntax rules for fixed values are:
<br>
1. Numbers are written with or without decimals:
<pre>
10.50
1001
</pre>
2. Strings are text, written within double or single quotes:
<pre>
"John Doe"
'John Doe'
</pre>
<h1>Variables</h1>
In a programming language, variables are used to store data values.
<br>
JavaScript uses the keywords <b>var</b>, <b>let</b> and <b>const</b> to declare variables.
<br>
An equal sign is used to assign values to variables.
<br>
In this example, x is defined as a variable. Then, x is assigned (given) the value 6:
<pre>
let x;
x = 6;
</pre>
<h1>Operators</h1>
JavaScript uses arithmetic operators ( + - * / ) to compute values:
<pre>(5 + 6) * 10</pre>
JavaScript uses an assignment operator ( = ) to assign values to variables:
<pre>
let x, y;
x = 5;
y = 6;
</pre>
<h1>Expressions</h1>
An expression is a combination of values, variables, and operators, which computes to a value.
<br>
The computation is called an evaluation.
<br>
For example, 5 * 10 evaluates to 50:
<pre>5 * 10</pre>
Expressions can also contain variable values:
<pre>x * 10</pre>
The values can be of various types, such as numbers and strings.
<br>
For example, "John" + " " + "Doe", evaluates to "John Doe":
<pre>"John" + " " + "Doe"</pre>
<h1>Keywords</h1>
JavaScript keywords are used to identify actions to be performed.
<br>
The <b>let</b> keyword tells the browser to create variables:
<pre>
let x, y;
x = 5 + 6;
y = x * 10;
</pre>
The <b>var</b> keyword also tells the browser to create variables:
<pre>
var x, y;
x = 5 + 6;
y = x * 10;
</pre>
<h1>Comment</h1>
Not all JavaScript statements are "executed".
<br>
Code after double slashes <code>//</code> or between <code>/*</code> and <code>*/</code> is treated as a comment.
<br>
Comments are ignored, and will not be executed:
<pre>
let x = 5; // I will be executed
// x = 6; I will NOT be executed
</pre>
<h1>Identifiers</h1>
Identifiers are JavaScript names.
<br>
Identifiers are used to name variables and keywords, and functions.
<br>
The rules for legal names are the same in most programming languages.
<br>
A JavaScript name must begin with:
<ul>
  <li>A letter (<code>A-Z</code> or <code>a-z</code>)</li>
  <li>A dollar sign (<code>$</code>)</li>
  <li>Or an underscore (<code>_</code>)</li>
</ul>
Subsequent characters may be letters, digits, underscores, or dollar signs.
<h1>Case Sensitive</h1>
All JavaScript identifiers are case sensitive. 
<br>
The variables <b>lastName</b> and <b>lastname</b>, are two different variables:
<pre>
let lastname, lastName;
lastName = "Doe";
lastname = "Peterson";
</pre>
JavaScript does not interpret LET or Let as the keyword let.
<h1>Camel Case</h1>
Historically, programmers have used different ways of joining multiple words into one variable name:
<br>
<b>Hyphens:</b>
<br>
first-name, last-name, master-card, inter-city.
<br>
Hyphens are not allowed in JavaScript. They are reserved for subtractions.
<br>
<b>Underscore:</b>
<br>
first_name, last_name, master_card, inter_city.
<br>
<b>Upper Camel Case (Pascal Case):</b>
<br>
FirstName, LastName, MasterCard, InterCity.
<br>
<b>Lower Camel Case:</b>
<br>
JavaScript programmers tend to use camel case that starts with a lowercase letter:
<br>
firstName, lastName, masterCard, interCity.
<h1>Character Set</h1>
JavaScript uses the Unicode character set.
<br>
Unicode covers (almost) all the characters, punctuations, and symbols in the world.
