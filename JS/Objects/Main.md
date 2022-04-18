<a href="/JS/Versions/History.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Objects/Definition.md">Next &gt;</a>
<hr>
You have already learned that JavaScript variables are containers for data values.
<br>
This code assigns a simple value (Fiat) to a variable named car:
<pre>let car = "Fiat";</pre>
Objects are variables too. But objects can contain many values.
<br>
This code assigns many values (Fiat, 500, white) to a variable named car:
<pre>const car = {type:"Fiat", model:"500", color:"white"};</pre>
The values are written as name:value pairs (name and value separated by a colon).
<h1>Properties</h1>
The <b>name:values</b> pairs in JavaScript objects are called properties:
<table class="ws-table-all notranslate">
  <tr>
    <th>Property</th>
    <th>Value</th>
  </tr>
  <tr>
    <td>firstName</td>
    <td>John</td>
  </tr>
  <tr>
    <td>lastName</td>
    <td>Doe</td>
  </tr>
  <tr>
    <td>age</td>
    <td>50</td>
  </tr>
  <tr>
    <td>eyeColor</td>
    <td>blue</td>
  </tr>
</table>
<h2>Accessing Them</h2>
You can access object properties in two ways:
<pre>objectName.propertyName</pre>
or
<pre>objectName["propertyName"]</pre>
<pre>person.lastName;</pre>
<pre>person["lastName"];</pre>
<h1>Methods</h1>
Objects can also have methods.
<br>
Methods are actions that can be performed on objects.
<br>
Methods are stored in properties as function definitions.
<table class="ws-table-all notranslate">
  <tr>
    <th>Property</th>
    <th>Value</th>
  </tr>
  <tr>
    <td>firstName</td>
    <td>John</td>
  </tr>
  <tr>
    <td>lastName</td>
    <td>Doe</td>
  </tr>
  <tr>
    <td>age</td>
    <td>50</td>
  </tr>
  <tr>
    <td>eyeColor</td>
    <td>blue</td>
  </tr>
  <tr>
    <td>fullName</td>
    <td><code>function() {return this.firstName + " " + this.lastName;}</code></td>
  </tr>
</table>
<b>Note:</b> A method is a function stored as a property.
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
In the example above, this refers to the person object.
<br>
I.E. <code>this.firstName</code> means the firstName property of this.
<br>
I.E. <code>this.firstName</code> means the firstName property of person.
<h1>What is the 'this' Keyword?</h1>
In JavaScript, the <b>this</b> keyword refers to an object.
<br>
Which object depends on how <b>this</b> is being invoked (used or called).
<br>
The <b>this</b> keyword refers to different objects depending on how it is used:
<ul>
  <li>In an object method, <b>this</b> refers to the object.</li>
  <li>Alone, <b>this</b> refers to the global object.</li>
  <li>In a function, <b>this</b> refers to the global object.</li>
  <li>In a function, in strict mode, <b>this</b> is <b>undefined</b>.</li>
  <li>In an event, <b>this</b> refers to the element that received the event.</li>
  <li>Methods like <b>call()</b>, <b>apply()</b>, and <b>bind()</b> can refer <b>this</b> to any object.</li>
</ul>
<b>Note: this</b> is not a variable. It is a keyword. You cannot change the value of <b>this</b>.
<br>
In a function definition, <b>this</b> refers to the "owner" of the function.
<br>
In the example above, <b>this</b> is the person object that "owns" the <b>fullName</b> function.
<br>
In other words, <b>this.firstName</b> means the <b>firstName</b> property of this object.
<h1>Accessing Methods</h1>
You access an object method with the following syntax:
<pre>objectName.methodName()</pre>
<pre>name = person.fullName();</pre>
If you access a method without the () parentheses, it will return the function definition:
<pre>name = person.fullName;</pre>
<h1>DO NOT Declare Strings, Numbers, and Booleans as Objects!</h1>
When a JavaScript variable is declared with the keyword "new", the variable is created as an object:
<pre>
x = new String(); // Declares x as a String object
y = new Number(); // Declares y as a Number object
z = new Boolean(); // Declares z as a Boolean object
</pre>
Avoid <b>String</b>, <b>Number</b>, and <b>Boolean</b> objects. They complicate your code and slow down execution speed.
