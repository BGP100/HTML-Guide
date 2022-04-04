4 Ways to Declare a JavaScript Variable:
<ul>
  <li>Using <b>var</b></li>
  <li>Using <b>let</b></li>
  <li>Using <b>const</b></li>
  <li>Using nothing</li>
</ul>
<h1>What are Them?</h1>
Variables are containers for storing data (storing data values).
<br>
In this example, <b>x</b>, <b>y</b>, and <b>z</b>, are variables, declared with the <b>var</b> keyword:
<pre>
var x = 5;
var y = 6;
var z = x + y;
</pre>
In this example, <b>x</b>, <b>y</b>, and <b>z</b>, are variables, declared with the <b>let</b> keyword:
<pre>
let x = 5;
let y = 6;
let z = x + y;
</pre>
In this example, <b>x</b>, <b>y</b>, and <b>z</b>, are undeclared variables:
<pre>
x = 5;
y = 6;
z = x + y;
</pre>
From all the examples above, you can guess:
<ul>
  <li>x stores the value 5</li>
  <li>y stores the value 6</li>
  <li>z stores the value 11</li>
</ul>
<h1>When to Use var?</h1>
Always declare JavaScript variables with <b>var</b>, <b>let</b>, or <b>const</b>.
<br>
The <b>var</b> keyword is used in all JavaScript code from 1995 to 2015.
<br>
The <b>let</b> and <b>const</b> keywords were added to JavaScript in 2015.
<br>
If you want your code to run in older browser, you must use <b>var</b>.
<h1>When to Use const?</h1>
If you want a general rule: always declare variables with <b>const</b>.
<br>
If you think the value of the variable can change, use <b>let</b>.
<br>
In this example, <b>price1</b>, <b>price2</b>, and <b>total</b>, are variables:
<pre>
const price1 = 5;
const price2 = 6;
let total = price1 + price2;
</pre>
The two variables <b>price1</b> and <b>price2</b> are declared with the <b>const</b> keyword.
<br>
These are constant values and cannot be changed.
<br>
The variable <b>total</b> is declared with the <b>let</b> keyword.
<br>
This is a value that can be changed.
<h1>Just Like Algebra</h1>
Just like in algebra, variables hold values:
<pre>
let x = 5;
let y = 6;
</pre>
Just like in algebra, variables are used in expressions:
<pre>let z = x + y;</pre>
From the example above, you can guess that the total is calculated to be 11.
<h1>Identifiers</h1>
All JavaScript variables must be identified with unique names.
<br>
These unique names are called identifiers.
<br>
Identifiers can be short names (like x and y) or more descriptive names (age, sum, totalVolume).
<br>
The general rules for constructing names for variables (unique identifiers) are:
<ul>
  <li>Names can contain letters, digits, underscores, and dollar signs.
  <li>Names must begin with a letter
  <li>Names can also begin with <code>$</code> and <code>_</code> (but we I not use it in this tutorial)
  <li>Names are case sensitive (y and Y are different variables)
  <li>Reserved words (like JavaScript keywords) cannot be used as names
</ul>
<h1>The Assignment Operator</h1>
In JavaScript, the equal sign (<code>=</code>) is an "assignment" operator, not an "equal to" operator.
<br>
This is different from algebra. The following does not make sense in algebra:
<pre>x = x + 5</pre>
In JavaScript, however, it makes perfect sense: it assigns the value of x + 5 to x.
<br>
(It calculates the value of x + 5 and puts the result into x. The value of x is incremented by 5.)
<br>
<b>Note:</b> The "equal to" operator is written like <code>==</code> in JavaScript.
<h1>Data Types</h1>
JavaScript variables can hold numbers like 100 and text values like "John Doe".
<br>
In programming, text values are called text strings.
<br>
JavaScript can handle many types of data, but for now, just think of numbers and strings.
<br>
Strings are written inside double or single quotes. Numbers are written without quotes.
<br>
If you put a number in quotes, it will be treated as a text string.
<pre>
const pi = 3.14;
let person = "John Doe";
let answer = 'Yes I am!';
</pre>
<h1>Declaring a Variable</h1>
Creating a variable in JavaScript is called "declaring" a variable.
<br>
You declare a JavaScript variable with the <b>var</b> or the <b>let</b> keyword:
<pre>var carName;</pre>
or:
<pre>let carName;</pre>
After the declaration, the variable has no value (technically it is undefined).
<br>
To assign a value to the variable, use the equal sign:
<pre>carName = "Volvo";</pre>
You can also assign a value to the variable when you declare it:
<pre>let carName = "Volvo";</pre>
In the example below, we create a variable called <b>carName</b> and assign the value "Volvo" to it.
<br>
Then we "output" the value inside an HTML paragraph with id="demo":
<pre>
&lt;p id="demo"&gt;&lt;/p&gt;
&lt;script&gt;
let carName = "Volvo";
document.getElementById("demo").innerHTML = carName; 
&lt;/script&gt;
</pre>
<h1>One Statement, Many Variables</h1>
You can declare many variables in one statement.
<br>
Start the statement with let and separate the variables by comma:
<pre>let person = "John Doe", carName = "Volvo", price = 200;</pre>
A declaration can span multiple lines:
<pre>
let person = "John Doe",
carName = "Volvo",
price = 200;
</pre>
<h1>Value = undefined</h1>
In computer programs, variables are often declared without a value. The value can be something that has to be calculated, or something that will be provided later, like user input.
<br>
A variable declared without a value will have the value undefined.
<br>
The variable carName will have the value undefined after the execution of this statement:
<pre>let carName;</pre>
<h1>Re-Declaring Variables</h1>
If you re-declare a JavaScript variable declared with var, it will not lose its value.
<br>
The variable carName will still have the value "Volvo" after the execution of these statements:
<pre>
var carName = "Volvo";
var carName;
</pre>
<b>Note:</b> You cannot re-declare a variable declared with let or const.
<br>
This will not work:
<pre>
let carName = "Volvo";
let carName;
</pre>
<h1>Arithmetic</h1>
As with algebra, you can do arithmetic with JavaScript variables, using operators like = and +:
<pre>let x = 5 + 2 + 3;</pre>
You can also add strings, but strings will be concatenated:
<pre>let x = "John" + " " + "Doe";</pre>
Also try this:
<pre>let x = "5" + 2 + 3;</pre>
<b>Note:</b> If you put a number in quotes, the rest of the numbers will be treated as strings, and concatenated.
<br>
Now try this:
<pre>let x = 2 + 3 + "5";</pre>
<h1>Dollar Sign</h1>
Since JavaScript treats a dollar sign as a letter, identifiers containing <code>$</code> are valid variable names:
<pre>
let $ = "Hello World";
let $$$ = 2;
let $myMoney = 5;
</pre>
Using the dollar sign is not very common in JavaScript, but professional programmers often use it as an alias for the main function in a JavaScript library.
<br>
In the JavaScript library jQuery, for instance, the main function <code>$</code> is used to select HTML elements. In jQuery $("p"); means "select all p elements".
<h1>Underscore</h1>
Since JavaScript treats underscore as a letter, identifiers containing <code>_</code> are valid variable names:
<pre>
let _lastName = "Johnson";
let _x = 2;
let _100 = 5;
</pre>
Using the underscore is not very common in JavaScript, but a convention among professional programmers is to use it as an alias for "private (hidden)" variables.
