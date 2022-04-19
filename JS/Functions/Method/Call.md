<a href="/JS/Functions/Invocation.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Functions/Method/Apply.md">Next &gt;</a>
<hr>
<h1>Method Reuse</h1>
With the <b>call()</b> method, you can write a method that can be used on different objects.
<h1>All Functions are Methods</h1>
In JavaScript all functions are object methods.
<br>
If a function is not a method of a JavaScript object, it is a function of the global object (see previous chapter).
<br>
The example below creates an object with 3 properties, firstName, lastName, fullName.
<pre>
const person = {
  firstName:"John",
  lastName: "Doe",
  fullName: function () {
    return this.firstName + " " + this.lastName;
  }
}
// This will return "John Doe":
person.fullName();
</pre>
In the example above, this refers to the person object.
<br>
<b>this.firstName</b> means the firstName property of this.
<br>
Same as:
<br>
<b>this.firstName</b> means the firstName property of person.
<h1>What is the this Keyword?</h1>
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
<h1>call()</h1>
The call() method is a predefined JavaScript method.
<br>
It can be used to invoke (call) a method with an owner object as an argument (parameter).
<br>
<b>Note:</b> With call(), an object can use a method belonging to another object.
<br>
This example calls the fullName method of person, using it on person1:
<pre>
const person = {
  fullName: function() {
    return this.firstName + " " + this.lastName;
  }
}
const person1 = {
  firstName:"John",
  lastName: "Doe"
}
const person2 = {
  firstName:"Mary",
  lastName: "Doe"
}
// This will return "John Doe":
person.fullName.call(person1);
</pre>
This example calls the fullName method of person, using it on person2:
<pre>
const person = {
  fullName: function() {
    return this.firstName + " " + this.lastName;
  }
}
const person1 = {
  firstName:"John",
  lastName: "Doe"
}
const person2 = {
  firstName:"Mary",
  lastName: "Doe"
}
// This will return "Mary Doe"
person.fullName.call(person2);
</pre>
<h1>call() with Arguments</h1>
The call() method can accept arguments:
<pre>
const person = {
  fullName: function(city, country) {
    return this.firstName + " " + this.lastName + "," + city + "," + country;
  }
}
const person1 = {
  firstName:"John",
  lastName: "Doe"
}
person.fullName.call(person1, "Oslo", "Norway");
</pre>
