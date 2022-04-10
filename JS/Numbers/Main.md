<a href="/JS/Strings/Templates.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Numbers/Methods.md">Next &gt;</a>
<hr>
JavaScript has only one type of number. Numbers can be written with or without decimals.
<hr>
<pre>
let x = 3.14; // A number with decimals
let y = 3; // A number without decimals
</pre>
Extra large or extra small numbers can be written with scientific (exponent) notation:
<pre>
let x = 123e5; // 12300000
let y = 123e-5; // 0.00123
</pre>
<h1>Numbers are Always 64-bit Floating Point</h1>
Unlike many other programming languages, JavaScript does not define different types of numbers, like integers, short, long, floating-point etc.
<br>
JavaScript numbers are always stored as double precision floating point numbers, following the international IEEE 754 standard. 
<br>
This format stores numbers in 64 bits, where the number (the fraction) is stored in bits 0 to 51, the exponent in bits 52 to 62, and the sign in bit 63:
<p></p>
<b>Value (aka Fraction/Mantissa):</b> 0 - 52 bits
<br>
<b>Exponent:</b> 52 - 62 bits
<b>Sign:</b> 63 bits
<h1>Integer Precision</h1>
Integers (numbers without a period or exponent notation) are accurate up to 15 digits.
<pre>
let x = "tel:999999999999999">999999999999999; // x will be 999999999999999
let y = "tel:9999999999999999">9999999999999999; // y will be 10000000000000000
</pre>
The maximum number of decimals is 17.
<h1>Floating Precision</h1>
Floating point arithmetic is not always 100% accurate:
<pre>let x = 0.2 + 0.1;</pre>
To solve the problem above, it helps to multiply and divide:
<pre>let x = (0.2 * 10 + 0.1 * 10) / 10;</pre>
<h1>Adding Numbers and Strings</h1>
<b>WARNING!!</b>
<br>
JavaScript uses the + operator for both addition and concatenation.
<br>
Numbers are added. Strings are concatenated.
<br>
If you add two numbers, the result will be a number:
<pre>
let x = 10;
let y = 20;
let z = x + y;
</pre>
If you add two strings, the result will be a string concatenation:
<pre>
let x = "10";
let y = "20";
let z = x + y;
</pre>
If you add a number and a string, the result will be a string concatenation:
<pre>
let x = 10;
let y = "20";
let z = x + y;
</pre>
If you add a string and a number, the result will be a string concatenation:
<pre>
let x = "10";
let y = 20;
let z = x + y;
</pre>
A common mistake is to expect this result to be 30:
<pre>
let x = 10;
let y = 20;
let z = "The result is: " + x + y;
</pre>
A common mistake is to expect this result to be 102030:
<pre>
let x = 10;
let y = 20;
let z = "30";
let result = x + y + z;
</pre>
<h1>NaN</h1>
NaN is a JavaScript reserved word indicating that a number is not a legal number.
<br>
Trying to do arithmetic with a non-numeric string will result in NaN (Not a Number):
<pre>let x = 100 / "Apple";</pre>
However, if the string contains a numeric value , the result will be a number:
<pre>let x = 100 / "10";</pre>
You can use the global JavaScript function isNaN() to find out if a value is a not a number:
<pre>
let x = 100 / "Apple";
isNaN(x);
</pre>
Watch out for NaN. If you use NaN in a mathematical operation, the result will also be NaN:
<pre>
let x = NaN;
let y = 5;
let z = x + y;
</pre>
Or the result might be a concatenation like NaN5:
<pre>
let x = NaN;
let y = "5";
let z = x + y;
</pre>
NaN is a number: typeof NaN returns number:
<pre>typeof NaN;</pre>
<h1>Infinity</h1>
Infinity (or -Infinity) is the value JavaScript will return if you calculate a number outside the largest possible number.

Example
let myNumber = 2;
// Execute until Infinity
while (myNumber != Infinity) {
  myNumber = myNumber * myNumber;
}
Try it Yourself »
Division by 0 (zero) also generates Infinity
<pre>
let x = 2 / 0;
let y = -2 / 0;
</pre>
Infinity is a number: typeof Infinity returns number.
<pre>typeof Infinity;</pre>
