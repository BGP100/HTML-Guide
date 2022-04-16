<a href="/JS/Debugging.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Practices.md">Next &gt;</a>
<hr>
Always use the same coding conventions for all your JavaScript projects.
<h1>Coding Conventions</h1>
Coding conventions are style guidelines for programming. They typically cover:
<ul>
Naming and declaration rules for variables and functions.
Rules for the use of white space, indentation, and comments.
Programming practices and principles
</ul>
Coding conventions secure quality:
<ul>
Improves code readability
Make code maintenance easier
</ul>
Coding conventions can be documented rules for teams to follow, or just be your individual coding practice.
<h1>Variable Names</h1>
At W3schools we use camelCase for identifier names (variables and functions).
<br>
All names start with a letter.
<br>
At the bottom of this page, you will find a wider discussion about naming rules.
<pre>
firstName = "John";
lastName = "Doe";
price = 19.90;
tax = 0.20;
fullPrice = price + (price * tax);
</pre>
<h1>Spaces Around Operators</h1>
Always put spaces around operators (<code>= + - * /</code>), and after commas:
<pre>
let x = y + z;
const myArray = ["Volvo", "Saab", "Fiat"];
</pre>
<h1>Code Indentation</h1>
Always use 2 spaces for indentation of code blocks:
<pre>
function toCelsius(fahrenheit) {
  return (5 / 9) * (fahrenheit - 32);
}
</pre>
<h1>Statement Rules</h1>
General rules for simple statements:
<br>
Always end a simple statement with a semicolon.
<pre>
const cars = ["Volvo", "Saab", "Fiat"];
const person = {
  firstName: "John",
  lastName: "Doe",
  age: 50,
  eyeColor: "blue"
};
</pre>
General rules for complex (compound) statements:
<ul>
  <li>Put the opening bracket at the end of the first line.</li>
  <li>Use one space before the opening bracket.</li>
  <li>Put the closing bracket on a new line, without leading spaces.</li>
  <li>Do not end a complex statement with a semicolon.</li>
</ul>
Functions:
<pre>
function toCelsius(fahrenheit) {
  return (5 / 9) * (fahrenheit - 32);
}
</pre>
Loops:
<pre>
for (let i = 0; i < 5; i++) {
  x += i;
}
</pre>
Conditionals:
<pre>
if (time < 20) {
  greeting = "Good day";
} else {
  greeting = "Good evening";
}
</pre>
<h1>Object Rules</h1>
General rules for object definitions:
<ul>
  <li>Place the opening bracket on the same line as the object name.</li>
  <li>Use colon plus one space between each property and its value.</li>
  <li>Use quotes around string values, not around numeric values.</li>
  <li>Do not add a comma after the last property-value pair.</li>
  <li>Place the closing bracket on a new line, without leading spaces.</li>
  <li>Always end an object definition with a semicolon.</li>
</ul>
<pre>
const person = {
  firstName: "John",
  lastName: "Doe",
  age: 50,
  eyeColor: "blue"
};
</pre>
Short objects can be written compressed, on one line, using spaces only between properties, like this:
<pre>const person = {firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"};</pre>
<h1>Line Length &lt; 80</h1>
For readability, avoid lines longer than 80 characters.
<br>
If a JavaScript statement does not fit on one line, the best place to break it, is after an operator or a comma.
<pre>document.getElementById("demo").innerHTML = "Hello Dolly.";</pre>
<h1>Naming Conventions</h1>
Always use the same naming convention for all your code. For example:
<ul>
  <li>Variable and function names written as camelCase</li>
  <li>Global variables written in UPPERCASE (We don't, but it's quite common)</li>
  <li>Constants (like PI) written in UPPERCASE</li>
</ul>
Should you use hyp-hens, camelCase, or under_scores in variable names?
<br>
This is a question programmers often discuss. The answer depends on who you ask:
<br>
<b>Hyphens in HTML and CSS:</b>
<br>
HTML5 attributes can start with data- (data-quantity, data-price).
<br>
CSS uses hyphens in property-names (font-size).
<br>
<b>Note:</b> Hyphens can be mistaken as subtraction attempts. Hyphens are not allowed in JavaScript names.
<br>
<b>Underscores:</b>
<br>
Many programmers prefer to use underscores (date_of_birth), especially in SQL databases.
<br>
Underscores are often used in PHP documentation.
<br>
<b>PascalCase:</b>
<br>
PascalCase is often preferred by C programmers.
<br>
<b>camelCase:</b>
<br>
camelCase is used by JavaScript itself, by jQuery, and other JavaScript libraries.
<br>
<b>Note:</b> Do not start names with a <code>$</code> sign. It will put you in conflict with many JavaScript library names.
<h1>Loading JavaScript in HTML</h1>
Use simple syntax for loading external scripts (the type attribute is not necessary):
<pre>&lt;script src="myScript.js"&gt;&lt;/script&gt;</pre>
<h1>Accessing HTML Elements</h1>
A consequence of using "untidy" HTML styles, might result in JavaScript errors.
<br>
These two JavaScript statements will produce different results:
<pre>
const obj = getElementById("Demo")
const obj = getElementById("demo")
</pre>
Or classes:
<pre>const obj = getElementByClass("example")</pre>
Or even the element itself:
<pre>const obj = getElementByElement("p")</pre>
If possible, use the same naming convention (as JavaScript) in HTML.
<h1>File Extensions</h1>
HTML files should have a <b>.html</b> extension (<b>.htm</b> is also allowed).
<br>
CSS files should have a <b>.css</b> extension.
<br>
JavaScript files should have a <b>.js</b> extension.
<h1>Use Lower Case File Names</h1>
Most web servers (Apache, Unix) are case sensitive about file names:
<br>
london.jpg cannot be accessed as London.jpg.
<br>
Other web servers (Microsoft, IIS) are not case sensitive:
<br>
london.jpg can be accessed as London.jpg or london.jpg.
<br>
If you use a mix of upper and lower case, you have to be extremely consistent.
<br>
If you move from a case insensitive, to a case sensitive server, even small errors can break your web site.
<br>
To avoid these problems, always use lower case file names (if possible).
<h1>Performance</h1>
Coding conventions are not used by computers. Most rules have little impact on the execution of programs.
<br>
Indentation and extra spaces are not significant in small scripts.
<br>
For code in development, readability should be preferred. Larger production scripts should be minified.
