<a href="/JS/Objects/Main.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Objects/Properties.md">Next &gt;</a>
<hr>
In JavaScript, almost "everything" is an object.
<ul>
  <li>Booleans can be objects (if defined with the <b>new</b> keyword)</li>
  <li>Numbers can be objects (if defined with the <b>new</b> keyword)</li>
  <li>Strings can be objects (if defined with the <b>new</b> keyword)</li>
  <li>Dates are always objects</li>
  <li>Maths are always objects</li>
  <li>Regular expressions are always objects</li>
  <li>Arrays are always objects</li>
  <li>Functions are always objects</li>
  <li>Objects are always objects</li>
</ul>
All JavaScript values, except primitives, are objects.
<h1>Primitives</h1>
A primitive value is a value that has no properties or methods.
<br>
3.14 is a primitive value
<br>
A primitive data type is data that has a primitive value.
<br>
JavaScript defines 7 types of primitive data types:
<ul>
  <li>string</li>
  <li>number</li>
  <li>boolean</li>
  <li>null</li>
  <li>undefined</li>
  <li>symbol</li>
  <li>bigint</li>
</ul>
<h1>Objects are Variables</h1>
JavaScript variables can contain single values:
<pre>let person = "John Doe";</pre>
JavaScript variables can also contain many values.
<br>
Objects are variables too. But objects can contain many values.
<br>
Object values are written as name : value pairs (name and value separated by a colon).
<pre>let person = {firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"};</pre>
It is a common practice to declare objects with the <b>const</b> keyword.
<pre>const person = {firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"};</pre>
<h1>Properties</h1>
The named values, in JavaScript objects, are called properties.
<br>
Objects written as name value pairs are similar to:
<ul>
  <li>Associative arrays in PHP</li>
  <li>Dictionaries in Python</li>
  <li>Hash tables in C</li>
  <li>Hash maps in Java</li>
  <li>Hashes in Ruby and Perl</li>
</ul>
<h1>Methods</h1>
Methods are actions that can be performed on objects.
<br>
Object properties can be both primitive values, other objects, and functions.
<br>
An object method is an object property containing a function definition.
<br>
You will learn more about methods in the next chapters.
<h1>Creating an Object</h1>
With JavaScript, you can define and create your own objects.
<br>
There are different ways to create new objects:
<ul>
  <li>Create a single object, using an object literal.</li>
  <li>Create a single object, with the keyword <b>new</b>.</li>
  <li>Define an object constructor, and then create objects of the constructed type.</li>
  <li>Create an object using <b>Object.create()</b>.</li>
</ul>
<h1>Using an Object Literal</h1>
This is the easiest way to create a JavaScript Object.
<br>
Using an object literal, you both define and create an object in one statement.
<br>
An object literal is a list of name:value pairs (like age:50) inside curly braces { }.
<br>
The following example creates a new JavaScript object with four properties:
<pre>const person = {firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"};</pre>
Spaces and line breaks are not important. An object definition can span multiple lines:
<pre>
const person = {
  firstName: "John",
  lastName: "Doe",
  age: 50,
  eyeColor: "blue"
};
</pre>
This example creates an empty JavaScript object, and then adds 4 properties:
<pre>
const person = {};
person.firstName = "John";
person.lastName = "Doe";
person.age = 50;
person.eyeColor = "blue";
</pre>
<h1>new Object()</h1>
The following example create a new JavaScript object using <b>new Object()</b>, and then adds 4 properties:
<pre>
const person = new Object();
person.firstName = "John";
person.lastName = "Doe";
person.age = 50;
person.eyeColor = "blue";
</pre>
<h1>Objects are Mutable</h1>
Objects are mutable: They are addressed by reference, not by value.
<br>
If person is an object, the following statement will not create a copy of person:
<pre>const x = person; // Will not create a copy of person</pre>
The object x is not a copy of person. It is person. Both x and person are the same object.
<br>
Any changes to x will also change person, because x and person are the same object.
<pre>
const person = {
  firstName:"John",
  lastName:"Doe",
  age:50, eyeColor:"blue"
}
const x = person;
x.age = 10; // Will change both x.age and person.age
</pre>
