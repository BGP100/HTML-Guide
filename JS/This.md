<a href="/JS/UseStrict.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Arrow.md">Next &gt;</a>
<hr>
In JavaScript, the this keyword refers to an object.
<br>
Which object depends on how this is being invoked (used or called).
<br>
The this keyword refers to different objects depending on how it is used:
<ul>
  <li>In an object method, this refers to the object.</li>
  <li>Alone, this refers to the global object.</li>
  <li>In a function, this refers to the global object.</li>
  <li>In a function, in strict mode, this is undefined.</li>
  <li>In an event, this refers to the element that received the event.</li>
  <li>Methods like call(), apply(), and bind() can refer this to any object.</li>
</ul>
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
<h1>In a Method</h1>
When used in an object method, this refers to the object.
<br>
In the example on top of this page, this refers to the person object.
<br>
Because the fullName method is a method of the person object.
<pre>
fullName : function() {
  return this.firstName + " " + this.lastName;
}
</pre>
<h1>Alone</h1>
When used alone, this refers to the global object.
<br>
Because this is running in the global scope.
<br>
In a browser window the global object is <code>[object Window]</code>:
<pre>
let x = this;
 In strict mode, when used alone, this also refers to the global object:
</pre>
<pre>
"use strict";
let x = this;
</pre>
<h1>In a Function (Default)</h1>
In a function, the global object is the default binding for this.
<br>
In a browser window the global object is [object Window]:
<pre>
function myFunction() {
  return this;
}
</pre>
<h1>n a Function (Strict)</h1>
JavaScript strict mode does not allow default binding.
<br>
So, when used in a function, in strict mode, this is undefined.
<pre>
"use strict";
function myFunction() {
  return this;
}
</pre>
<h1>Object Method Binding</h1>
In these examples, this is the person object:
<pre>
const person = {
  firstName  : "John",
  lastName   : "Doe",
  id         : 5566,
  myFunction : function() {
    return this;
  }
};
</pre>
<pre>
const person = {
  firstName: "John",
  lastName : "Doe",
  id       : 5566,
  fullName : function() {
    return this.firstName + " " + this.lastName;
  }
};
</pre>
<h1>Explicit Function Binding</h1>
The <b>call()</b> and <b>apply()</b> methods are predefined JavaScript methods.
<br>
They can both be used to call an object method with another object as argument.
<br>
The example below calls person1.fullName with person2 as an argument, this refers to person2, even if fullName is a method of person1:
<pre>
const person1 = {
  fullName: function() {
    return this.firstName + " " + this.lastName;
  }
}
const person2 = {
  firstName: "John",
  lastName: "Doe",
}
person1.fullName.call(person2); // Return "John Doe"
</pre>
<h1>Function Borrowing</h1>
With the bind() method, an object can borrow a method from another object.
<br>
This example creates 2 objects (person and member).
<br>
The member object borrows the fullname method from the person object:
<pre>
const person = {
  firstName: "John",
  lastName: "Doe",
  fullName: function () {
    return this.firstName + " " + this.lastName;
  }
}
const member = {
  firstName: "Hege",
  lastName: "Nilsen",
}
let fullName = person.fullName.bind(member);
</pre>
