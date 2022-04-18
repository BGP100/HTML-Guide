<a href="/JS/Operators/Bitwise.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Events.md">Next &gt;</a>
<hr>
In programming, data types is an important concept.
<br>
To be able to operate on variables, it is important to know something about the type.
<br>
Without data types, a computer cannot safely solve this:
<pre>let x = 16 + "Volvo";</pre>
Does it make any sense to add "Volvo" to sixteen? Will it produce an error or will it produce a result?
<br>
JavaScript will treat the example above as:
<pre>let x = "16" + "Volvo";</pre>
When adding a number and a string, JavaScript will treat the number as a string.
<pre>let x = 16 + "Volvo";</pre>
<pre>let x = "Volvo" + 16;</pre>
JavaScript evaluates expressions from left to right. Different sequences can produce different results:
<pre>let x = 16 + 4 + "Volvo";</pre>
Result: <code>20Volvo</code>
<pre>let x = "Volvo" + 16 + 4;</pre>
Result: <code>Volvo164</code>
<p></p>
In the first example, JavaScript treats 16 and 4 as numbers, until it reaches "Volvo".
<br>
In the second example, since the first operand is a string, all operands are treated as strings.
<h1>Dynamic</h1>
JavaScript has dynamic types. This means that the same variable can be used to hold different data types:
<pre>
let x; // Now x is undefined
x = 5; // Now x is a Number
x = "John"; // Now x is a String
</pre>
<h1>Strings</h1>
A string (or a text string) is a series of characters like "John Doe".
<br>
Strings are written with quotes. You can use single or double quotes:
<pre>
let carName1 = "Volvo XC60"; // Using double quotes
let carName2 = 'Volvo XC60'; // Using single quotes
</pre>
You can use quotes inside a string, as long as they don't match the quotes surrounding the string:
<pre>
let answer1 = "It's alright"; // Single quote inside double quotes
let answer2 = "He is called 'Johnny'"; // Single quotes inside double quotes
let answer3 = 'He is called "Johnny"'; // Double quotes inside single quotes
</pre>
You will learn more about strings later in this tutorial.
<h1>Numbers</h1>
JavaScript has only one type of numbers.
<br>
Numbers can be written with, or without decimals:
<pre>
let x1 = 34.00; // Written with decimals
let x2 = 34; // Written without decimals
</pre>
Extra large or extra small numbers can be written with scientific (exponential) notation:
<pre>
let y = 123e5; // 12300000
let z = 123e-5; // 0.00123
</pre>
You will learn more about numbers later in this tutorial.
<h1>Booleans</h1>
Booleans can only have two values: <b>true</b> or <b>false</b>.
<pre>
let x = 5;
let y = 5;
let z = 6;
(x == y) // Returns true
(x == z) // Returns false
</pre>
Booleans are often used in conditional testing.
<br>
You will learn more about conditional testing later in this tutorial.
<h1>Arrays</h1>
JavaScript arrays are written with square brackets.
<br>
Array items are separated by commas.
<br>
The following code declares (creates) an array called cars, containing three items (car names):
<pre>const cars = ["Saab", "Volvo", "BMW"];</pre>
Array indexes are zero-based, which means the first item is <code>[0]</code>, second is <code>[1]</code>, and so on.
<br>
You will learn more about arrays later in this tutorial.
<h1>Objects</h1>
JavaScript objects are written with curly braces { }.
<br>
Object properties are written as name:value pairs, separated by commas.
<pre>const person = {firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"};</pre>
The object (person) in the example above has 4 properties: firstName, lastName, age, and eyeColor.
<h1>Undefined</h1>
In JavaScript, a variable without a value, has the value undefined. The type is also undefined.
<pre>let car; // Value is undefined, type is undefined</pre>
Any variable can be emptied, by setting the value to undefined. The type will also be undefined.
<pre>car = undefined; // Value is undefined, type is undefined</pre>
<h1>Empty Values</h1>
An empty value has nothing to do with undefined.
<br>
An empty string has both a legal value and a type.
<pre>let car = ""; // The value is "", the typeof is "string"</pre>
