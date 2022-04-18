<a href="/JS/Objects/Properties.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Objects/Display.md">Next &gt;</a>
<hr>
Methods are actions that can be performed on objects.
<br>
Object properties can be both primitive values, other objects, and functions.
<br>
An object method is an object property containing a function definition.
<pre>
const person = {
  firstName: "John",
  lastName: "Doe",
  id: 5566,
  fullName: function() {
    return this.firstName + " " + this.lastName;
  }
};
</pre>
<h1>this</h1>
In JavaScript, the <b>this</b> keyword refers to an object.
<br>
Which object depends on how <b>this</b> is being invoked (used or called).
<br>
The <b>this</b> keyword refers to different objects depending on how it is used:
<ul>
  <li>In an object method, <b>this</b> refers to the object.</li>
  <li>Alone, <b>this</b> refers to the global object.</li>
  <li>In a function, <b>this</b> refers to the global object.</li>
  <li>In a function, in strict mode, <b>this</b> is undefined.</li>
  <li>In an event, <b>this</b> refers to the element that received the event.</li>
  <li>Methods like <b>call()</b>, <b>apply()</b>, and <b>bind()</b> can refer <b>this</b> to any object.</li>
</ul>
<h1>Methods</h1>
JavaScript methods are actions that can be performed on objects.
<br>
A JavaScript method is a property containing a function definition.
<h1>Accessing Them</h1>
You access an object method with the following syntax:
<pre>objectName.methodName()</pre>
You will typically describe fullName() as a method of the person object, and fullName as a property.
<br>
The fullName property will execute (as a function) when it is invoked with ().
<br>
This example accesses the fullName() method of a person object:
<br>
Examples:
<pre>name = person.fullName();</pre>
If you access the fullName property, without (), it will return the function definition:
<pre>name = person.fullName;</pre>
<h1>Adding a Method to an Object</h1>
Adding a new method to an object is easy:
<pre>
person.name = function () {
  return this.firstName + " " + this.lastName;
};
</pre>
<h1>Using Built-In Methods</h1>
This example uses the toUpperCase() method of the String object, to convert a text to uppercase:
<pre>
let message = "Hello world!";
let x = message.toUpperCase();
</pre>
The value of x, after execution of the code above will be:
<pre>
person.name = function () {
  return (this.firstName + " " + this.lastName).toUpperCase();
};
</pre>
