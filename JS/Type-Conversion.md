<a href="/JS/Typeof.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/RegExp.md">Next &gt;</a>
<hr>
<ul>
  <li>Converting Strings to Numbers</li>
  <li>Converting Numbers to Strings</li>
  <li>Converting Dates to Numbers</li>
  <li>Converting Numbers to Dates</li>
  <li>Converting Booleans to Numbers</li>
  <li>Converting Numbers to Booleans</li>
</ul>
<h1>Converting Strings to Numbers</h1>
The global method Number() can convert strings to numbers.
<br>
Strings containing numbers (like "3.14") convert to numbers (like 3.14).
<br>
Empty strings convert to 0.
<br>
Anything else converts to NaN (Not a Number).
<pre>
Number("3.14") // returns 3.14
Number(" ") // returns 0
Number("") // returns 0
Number("99 88") // returns NaN
</pre>
<h1>Unary + Operator</h1>
The <b>unary + operator</b> can be used to convert a variable to a number:
<pre>
let y = "5"; // y is a string
let x = + y; // x is a number
</pre>
If the variable cannot be converted, it will still become a number, but with the value NaN (Not a Number):
<pre>
let y = "John"; // y is a string
let x = + y; // x is a number (NaN)
</pre>
<h1>Converting Numbers to Strings</h1>
The global method String() can convert numbers to strings.
<br>
It can be used on any type of numbers, literals, variables, or expressions:
<pre>
String(x) // returns a string from a number variable x
String(123) // returns a string from a number literal 123
String(100 + 23) // returns a string from a number from an expression
</pre>
The Number method toString() does the same.
<pre>
x.toString()
(123).toString()
(100 + 23).toString()
</pre>
<h1>Converting Dates to Numbers</h1>
The global method Number() can be used to convert dates to numbers.
<pre>
d = new Date();
Number(d) // returns 1404568027739
</pre>
The date method getTime() does the same.
<pre>
d = new Date();
d.getTime() // returns 1404568027739
</pre>
<h1>Converting Dates to Strings</h1>
The global method String() can convert dates to strings.
<pre>String(Date()) // returns "Thu Jul 17 2014 15:38:19 GMT+0200 (W. Europe Daylight Time)"</pre>
The Date method toString() does the same.
<pre>Date().toString() // returns "Thu Jul 17 2014 15:38:19 GMT+0200 (W. Europe Daylight Time)"</pre>
<h1>Converting Booleans to Numbers</h1>
The global method Number() can also convert booleans to numbers.
<pre>
Number(false) // returns 0
Number(true) // returns 1
</pre>
<h1>Converting Booleans to Strings</h1>
The global method String() can convert booleans to strings.
<pre>
String(false) // returns "false"
String(true) // returns "true"
</pre>
<h1>Automatic Type Conversion</h1>
When JavaScript tries to operate on a "wrong" data type, it will try to convert the value to a "right" type.

The result is not always what you expect:

5 + null    // returns 5         because null is converted to 0
"5" + null  // returns "5null"   because null is converted to "null"
"5" + 2     // returns "52"      because 2 is converted to "2"
"5" - 2     // returns 3         because "5" is converted to 5
"5" * "2"   // returns 10        because "5" and "2" are converted to 5 and 2
<h1>Automatic String Conversion</h1>
JavaScript automatically calls the variable's toString() function when you try to "output" an object or a variable:
<pre>
document.getElementById("demo").innerHTML = myVar;
// if myVar = {name:"Fjohn"} // toString converts to "[object Object]"
// if myVar = [1,2,3,4] // toString converts to "1,2,3,4"
// if myVar = new Date() // toString converts to "Fri Jul 18 2014 09:08:55 GMT+0200"
</pre>
Numbers and booleans are also converted, but this is not very visible:
<pre>
// if myVar = 123 // toString converts to "123"
// if myVar = true // toString converts to "true"
// if myVar = false // toString converts to "false"
</pre>
