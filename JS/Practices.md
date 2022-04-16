<a href="/JS/BeginnerGuide.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Mistakes.md">Next &gt;</a>
<hr>
Avoid global variables, avoid <code>new</code>, avoid <code>==</code>, avoid <code>eval()</code>.
<h1>Avoid Global Variables</h1>
Minimize the use of global variables.
<br>
This includes all data types, objects, and functions.
<br>
Global variables and functions can be overwritten by other scripts.
<h1>Always Declare Local Variables</h1>
All variables used in a function should be declared as local variables.
<br>
Local variables must be declared with the var keyword or the let keyword,or the const keyword, otherwise they will become global variables.
<h1>Declarations on Top</h1>
It is a good coding practice to put all declarations at the top of each script or function.
<br>
This will:
<ul>
  <li>Give cleaner code</li>
  <li>Provide a single place to look for local variables</li>
  <li>Make it easier to avoid unwanted (implied) global variables</li>
  <li>Reduce the possibility of unwanted re-declarations</li>
</ul>
<pre>
// Declare at the beginning
let firstName, lastName, price, discount, fullPrice;
// Use later
firstName = "John";
lastName = "Doe";
price = 19.90;
discount = 0.10;
fullPrice = price - discount;
</pre>
This also goes for loop variables:
<pre>for (let i = 0; i < 5; i++) {</pre>
<h1>Initialize Variables</h1>
It is a good coding practice to initialize variables when you declare them.
<br>
This will:
<ul>
  <li>Give cleaner code</li>
  <li>Provide a single place to initialize variables</li>
  <li>Avoid undefined values</li>
</ul>
<pre>
// Declare and initiate at the beginning
let firstName = "",
let lastName = "",
let price = 0,
let discount = 0,
let fullPrice = 0,
const myArray = [],
const myObject = {};
</pre>
<h1>Declare Objects with const</h1>
Declaring objects with const will prevent any accidental change of type:
<pre>
let car = {type:"Fiat", model:"500", color:"white"};
car = "Fiat"; // Changes object to string
</pre>
<pre>
const car = {type:"Fiat", model:"500", color:"white"};
car = "Fiat"; // Not possible
</pre>
<h1>Declare Arrays with const</h1>
Declaring arrays with const will prevent any accidential change of type:
<pre>
let cars = ["Saab", "Volvo", "BMW"];
cars = 3; // Changes array to number
</pre>
<pre>
const cars = ["Saab", "Volvo", "BMW"];
cars = 3; // Not possible
</pre>
<h1>Don't Use new Object()</h1>
<ul>
  <li>Use <code>""</code> instead of <code>new String()</code></li>
  <li>Use <code>0</code> instead of <code>new Number()</code></li>
  <li>Use <code>false</code> instead of <code>new Boolean()</code></li>
  <li>Use <code>{}</code> instead of <code>new Object()</code></li>
  <li>Use <code>[]</code> instead of <code>new Array()</code></li>
  <li>Use <code>/()/</code> instead of new <code>RegExp()</code></li>
  <li>Use <code>function (){}</code> instead of <code>new Function()</code></li>
</ul>
<pre>
let x1 = ""; // new primitive string
let x2 = 0; // new primitive number
let x3 = false; // new primitive boolean
const x4 = {}; // new object
const x5 = []; // new array object
const x6 = /()/; // new regexp object
const x7 = function(){}; // new function object
</pre>
<h1>Beware of Automatic Type Conversions</h1>
JavaScript is loosely typed.
<br>
A variable can contain all data types.
<br>
A variable can change its data type:
<pre>
let x = "Hello"; // typeof x is a string
x = 5; // changes typeof x to a number
</pre>
Beware that numbers can accidentally be converted to strings or NaN (Not a Number).
<br>
When doing mathematical operations, JavaScript can convert numbers to strings:
<pre>
let x = 5 + 7; // x.valueOf() is 12,  typeof x is a number
let x = 5 + "7"; // x.valueOf() is 57,  typeof x is a string
let x = "5" + 7; // x.valueOf() is 57,  typeof x is a string
let x = 5 - 7; // x.valueOf() is -2,  typeof x is a number
let x = 5 - "7"; // x.valueOf() is -2,  typeof x is a number
let x = "5" - 7; // x.valueOf() is -2,  typeof x is a number
let x = 5 - "x"; // x.valueOf() is NaN, typeof x is a number
</pre>
Subtracting a string from a string, does not generate an error but returns NaN (Not a Number):
<pre>"Hello" - "Dolly" // returns NaN</pre>
<h1>Use <code>===</code> Comparison</h1>
The <code>==</code> comparison operator always converts (to matching types) before comparison.
<br>
The <code>===</code> operator forces comparison of values and type:
<pre>
0 == ""; // true
1 == "1"; // true
1 == true; // true
</pre>
<pre>
0 === ""; // false
1 === "1"; // false
1 === true; // false
</pre>
<h1>Use Parameter Defaults</h1>
If a function is called with a missing argument, the value of the missing argument is set to undefined.
<br>
Undefined values can break your code. It is a good habit to assign default values to arguments.
<pre>
function myFunction(x, y) {
  if (y === undefined) {
    y = 0;
  }
}
</pre>
<pre>function (a=1, b=1) {/*function code*/}</pre>
<h1>End Your Switches with Defaults</h1>
Always end your switch statements with a default. Even if you think there is no need for it.
<pre>
switch (new Date().getDay()) {
  case 0:
    day = "Sunday";
    break;
  case 1:
    day = "Monday";
    break;
  case 2:
    day = "Tuesday";
    break;
  case 3:
    day = "Wednesday";
    break;
  case 4:
    day = "Thursday";
    break;
  case 5:
    day = "Friday";
    break;
  case 6:
    day = "Saturday";
    break;
  default:
    day = "Unknown";
}
</pre>
<h1>Avoid Number, String, and Boolean as Objects</h1>
Always treat numbers, strings, or booleans as primitive values. Not as objects.
<br>
Declaring these types as objects, slows down execution speed, and produces nasty side effects:
<pre>
let x = "John";             
let y = new String("John");
(x === y) // is false because x is a string and y is an object.
</pre>
Or even worse:
<pre>
let x = new String("John");             
let y = new String("John");
(x == y) // is false because you cannot compare objects.
</pre>
<h1>Avoid Using eval()</h1>
The <b>eval()</b> function is used to run text as code. In almost all cases, it should not be necessary to use it.
<br>
Because it allows arbitrary code to be run, it also represents a security problem.
