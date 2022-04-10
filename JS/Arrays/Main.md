<a href="/JS/Numbers/Methods.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Arrays/Methods.md">Next &gt;</a>
<hr>
An array is a special variable, which can hold more than one value:
<pre>const cars = ["Saab", "Volvo", "BMW"];</pre>
<h1>Why Use Them?</h1>
If you have a list of items (a list of car names, for example), storing the cars in single variables could look like this:
<pre>
let car1 = "Saab";
let car2 = "Volvo";
let car3 = "BMW";
</pre>
However, what if you want to loop through the cars and find a specific one? And what if you had not 3 cars, but 300?
<br>
The solution is an array!
<br>
An array can hold many values under a single name, and you can access the values by referring to an index number.
<h1>Creating an Array</h1>
Using an array literal is the easiest way to create a JavaScript Array.
<br>
<b>Syntax:</b>
<pre>const array_name = [item1, item2, ...];</pre>
<pre>const cars = ["Saab", "Volvo", "BMW"];</pre>
Spaces and line breaks are not important. A declaration can span multiple lines:
<pre>
const cars = [
  "Saab",
  "Volvo",
  "BMW"
];
</pre>
You can also create an array, and then provide the elements:
<pre>
const cars = [];
cars[0] = "Saab";
cars[1] = "Volvo";
cars[2] = "BMW";
</pre>
<h1>new</h1>
The following example also creates an Array, and assigns values to it:
<pre>const cars = new Array("Saab", "Volvo", "BMW");</pre>
<h1>Arrays are Objects</h1>
Arrays are a special type of objects. The <b>typeof</b> operator in JavaScript returns "object" for arrays.
<br>
But, JavaScript arrays are best described as arrays.
<br>
Arrays use numbers to access its "elements". In this example, <code>person[0]</code> returns John:
<pre>const person = ["John", "Doe", 46];</pre>
Objects use names to access its "members". In this example, <code>person.firstName</code> returns John:
<pre>const person = {firstName:"John", lastName:"Doe", age:46};</pre>
<h1>Last Array Element</h1>
<pre>
const fruits = ["Banana", "Orange", "Apple", "Mango"];
let fruit = fruits[fruits.length - 1];
</pre>
<h1>Loops</h1>
One way to loop through an array, is using a for loop:
<pre>
const fruits = ["Banana", "Orange", "Apple", "Mango"];
let fLen = fruits.length;
let text = "&lt;ul&gt;";
for (let i = 0; i &lt; fLen; i++) {
  text += "&lt;li&gt;" + fruits[i] + "&lt;/li&gt;";
}
text += "&lt;/ul&gt;";
</pre>
You can also use the <b>Array.forEach()</b> function:
<pre>
const fruits = ["Banana", "Orange", "Apple", "Mango"];
let text = "&lt;ul&gt;";
fruits.forEach(myFunction);
text += "&lt;/ul&gt;";
function myFunction(value) {
  text += "&lt;li&gt;" + value + "&lt;/li&gt;";
}
</pre>
<h1>Associative Arrays</h1>
Many programming languages support arrays with named indexes.
<br>
Arrays with named indexes are called associative arrays (or hashes).
<br>
JavaScript does not support arrays with named indexes.
<br>
In JavaScript, arrays always use numbered indexes.  
<pre>
const person = [];
person[0] = "John";
person[1] = "Doe";
person[2] = 46;
person.length; // Will return 3
person[0]; // Will return "John"
</pre>
<h1>Difference Between Arrays and Objects</h1>
In JavaScript, arrays use numbered indexes.  
<br>
In JavaScript, objects use named indexes.
<br>
Arrays are a special kind of objects, with numbered indexes.
<h2>When to Use Them?</h2>
<ul>
  <li>JavaScript does not support associative arrays.</li>
  <li>You should use objects when you want the element names to be strings (text).</li>
  <li>You should use arrays when you want the element names to be numbers.</li>
</ul>
