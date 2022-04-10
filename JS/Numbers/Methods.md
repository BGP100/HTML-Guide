<a href="/JS/Numbers/Main.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Arrays/Main.md">Next &gt;</a>
<hr>
Primitive values (like 3.14 or 2014), cannot have properties and methods (because they are not objects).
<br>
But with JavaScript, methods and properties are also available to primitive values, because JavaScript treats primitive values as objects when executing methods and properties.
<h1>toString()</h1>
The <b>toString()</b> method returns a number as a string.
<br>
All number methods can be used on any type of numbers (literals, variables, or expressions):
<pre>
let x = 123;
x.toString();
(123).toString();
(100 + 23).toString();
</pre>
<h1>toExponential()</h1>
<b>toExponential()</b> returns a string, with a number rounded and written using exponential notation.
<br>
A parameter defines the number of characters behind the decimal point:
<pre>
let x = 9.656;
x.toExponential(2);
x.toExponential(4);
x.toExponential(6);
</pre>
The parameter is optional. If you don't specify it, JavaScript will not round the number.
<h1>The toFixed() Method</h1>
<b>toFixed()</b> returns a string, with the number written with a specified number of decimals:
<pre>
let x = 9.656;
x.toFixed(0);
x.toFixed(2);
x.toFixed(4);
x.toFixed(6);
</pre>
<b>toFixed(2)</b> is perfect for working with money.
<h1>toPrecision()</h1>
<b>toPrecision()</b> returns a string, with a number written with a specified length:
<pre>
let x = 9.656;
x.toPrecision();
x.toPrecision(2);
x.toPrecision(4);
x.toPrecision(6);
</pre>
<h1>valueOf()</h1>
<b>valueOf()</b> returns a number as a number.
<pre>
let x = 123;
x.valueOf();
(123).valueOf();
(100 + 23).valueOf();
</pre>
In JavaScript, a number can be a primitive value (typeof = number) or an object (typeof = object).
<br>
The valueOf() method is used internally in JavaScript to convert Number objects to primitive values.
<br>
There is no reason to use it in your code.
<h1>Converting Variables to Numbers</h1>
There are 3 JavaScript methods that can be used to convert variables to numbers:
<ul>
  <li>The Number() method</li>
  <li>The parseInt() method</li>
  <li>The parseFloat() method</li>
</ul>
These methods are not number methods, but global JavaScript methods.
<h1>Number()</h1>
<b>Number()</b> can be used to convert JavaScript variables to numbers:
<pre>
Number(true);
Number(false);
Number("10");
Number("  10");
Number("10  ");
Number(" 10  ");
Number("10.33");
Number("10,33");
Number("10 33");
Number("John");
</pre>
If the number cannot be converted, NaN (Not a Number) is returned.
<h2>Number() Used on Dates</h2>
Number() can also convert a date to a number.
<pre>Number(new Date("1970-01-01"))</pre>
The <b>Number()</b> method returns the number of milliseconds since 1.1.1970.
<br>
The number of milliseconds between 1970-01-02 and 1970-01-01 is 86400000:
<pre>Number(new Date("1970-01-02"))</pre>
<pre>Number(new Date("2017-09-30"))</pre>
<h1>parseInt()</h1>
<b>parseInt()</b> parses a string and returns a whole number. Spaces are allowed. Only the first number is returned:
<pre>
parseInt("-10");
parseInt("-10.33");
parseInt("10");
parseInt("10.33");
parseInt("10 20 30");
parseInt("10 years");
parseInt("years 10");
</pre>
If the number cannot be converted, NaN (Not a Number) is returned.
<h1>parseFloat()</h1>
<b>parseFloat()</b> parses a string and returns a number. Spaces are allowed. Only the first number is returned:
<pre>
parseFloat("10");
parseFloat("10.33");
parseFloat("10 20 30");
parseFloat("10 years");
parseFloat("years 10");
</pre>
If the number cannot be converted, NaN (Not a Number) is returned.
Number Properties
<h1>MIN_VALUE &amp; MAX_VALUE</h1>
<b>MAX_VALUE</b> returns the largest possible number in JavaScript.
<pre>let x = Number.MAX_VALUE;</pre>
<b>MIN_VALUE</b> returns the lowest possible number in JavaScript.
<pre>let x = Number.MIN_VALUE;</pre>
<h1>POSITIVE_INFINITY</h1>
<pre>let x = Number.POSITIVE_INFINITY;</pre>
<b>POSITIVE_INFINITY</b> is returned on overflow:
<pre>let x = 1 / 0;</pre>
<h1>NEGATIVE_INFINITY</h1>
<pre>let x = Number.NEGATIVE_INFINITY;</pre>
<b>NEGATIVE_INFINITY</b> is returned on overflow:
<pre>let x = -1 / 0;</pre>
