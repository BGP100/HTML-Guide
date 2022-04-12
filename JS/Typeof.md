<a href="/JS/Maps.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Type-Conversion.md">Next &gt;</a>
<hr>
In JavaScript there are 5 different data types that can contain values:
<ul>
  <li><b>string</b></li>
  <li><b>number</b></li>
  <li><b>boolean</b></li>
  <li><b>object</b></li>
  <li><b>function</b></li>
</ul>
There are 6 types of objects:
<ul>
  <li><b>Object</b></li>
  <li><b>Date</b></li>
  <li><b>Array</b></li>
  <li><b>String</b></li>
  <li><b>Number</b></li>
  <li><b>Boolean</b></li>
</ul>
And 2 data types that cannot contain values:
<ul>
  <li><b>null</b></li>
  <li><b>undefined</b></li>
</ul>
<h1>Operator</h1>
You can use the typeof operator to find the data type of a JavaScript variable.
<pre>
typeof "John" // Returns "string"
typeof 3.14 // Returns "number"
typeof NaN // Returns "number"
typeof false // Returns "boolean"
typeof [1,2,3,4] // Returns "object"
typeof {name:'John', age:34} // Returns "object"
typeof new Date() // Returns "object"
typeof function () {} // Returns "function"
typeof myCar // Returns "undefined *"
typeof null // Returns "object"
</pre>
Please observe:
<ul>
  <li>The data type of NaN is <code>number</code></li>
  <li>The data type of an array is <code>object</code></li>
  <li>The data type of a date is <code>object</code></li>
  <li>The data type of null is <code>object</code></li>
  <li>The data type of an undefined variable is <code>undefined *</code></li>
  <li>The data type of a variable that has not been assigned a value is also <code>undefined *</code></li>
</ul>
<h1>Primitive Data</h1>
A primitive data value is a single simple data value with no additional properties and methods.
<pre>
typeof "John" // Returns "string"
typeof 3.14 // Returns "number"
typeof true // Returns "boolean"
typeof false // Returns "boolean"
typeof x // Returns "undefined" (if x has no value)
</pre>
<h1>Complex Data</h1>
The <b>typeof</b> operator can return one of two complex types:
<ul>
  <li>function</li>
  <li>object</li>
</ul>
The <b>typeof</b> operator returns "object" for objects, arrays, and null.
<br>
The <b>typeof</b> operator does not return "object" for functions.
<pre>
typeof {name:'John', age:34} // Returns "object"
typeof [1,2,3,4] // Returns "object" (not "array", see note below)
typeof null // Returns "object"
typeof function myFunc(){} // Returns "function"
</pre>
<h1>Data Type of typeof</h1>
The <b>typeof</b> operator is not a variable. It is an operator. Operators (<code>+ - * /</code>) do not have any data type.
<br>
But, the <b>typeof</b> operator always returns a string (containing the type of the operand).
<h1>constructor</h1>
The <b>constructor</b> property returns the constructor function for all JavaScript variables.
<pre>
"John".constructor                // Returns function String()  {[native code]}
(3.14).constructor                // Returns function Number()  {[native code]}
false.constructor                 // Returns function Boolean() {[native code]}
[1,2,3,4].constructor             // Returns function Array()   {[native code]}
{name:'John',age:34}.constructor  // Returns function Object()  {[native code]}
new Date().constructor            // Returns function Date()    {[native code]}
function () {}.constructor        // Returns function Function(){[native code]}
</pre>
You can check the constructor property to find out if an object is an Array (contains the word "Array"):
<pre>
function isArray(myArray) {
  return myArray.constructor.toString().indexOf("Array") > -1;
}
</pre>
Or even simpler, you can check if the object is an Array function:
<pre>
function isArray(myArray) {
  return myArray.constructor === Array;
}
</pre>
You can check the constructor property to find out if an object is a Date (contains the word "Date"):
<pre>
function isDate(myDate) {
  return myDate.constructor.toString().indexOf("Date") > -1;
}
</pre>
Or even simpler, you can check if the object is a Date function:
<pre>
function isDate(myDate) {
  return myDate.constructor === Date;
}
</pre>
<h1>Undefined</h1>
In JavaScript, a variable without a value, has the value undefined. The type is also undefined.
<pre>let car; // Value is undefined, type is undefined</pre>
Any variable can be emptied, by setting the value to undefined. The type will also be undefined.
<pre>car = undefined; // Value is undefined, type is undefined</pre>
<h1>Empty</h1>
An empty value has nothing to do with undefined.
<br>
An empty string has both a legal value and a type.
<pre>let car = "";    // The value is "", the typeof is "string"</pre>
<h1>Null</h1>
In JavaScript null is "nothing". It is supposed to be something that doesn't exist.
<br>
Unfortunately, in JavaScript, the data type of null is an object.
<br>
You can empty an object by setting it to null:
<pre>
let person = {firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"};
person = null; // Now value is null, but type is still an object
</pre>
You can also empty an object by setting it to undefined:
<pre>
let person = {firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"};
person = undefined; // Now both value and type is undefined
</pre>
<h1>Difference Between Undefined and Null</h1>
undefined and null are equal in value but different in type:
<pre>
typeof undefined // undefined
typeof null // object
null === undefined // false
null == undefined // true
</pre>
