<a href="/JS/Objects/Definition.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Objects/Methods.md">Next &gt;</a>
<hr>
Properties are the most important part of any JavaScript object.
<hr>
Properties are the values associated with a JavaScript object.
<br>
A JavaScript object is a collection of unordered properties.
<br>
Properties can usually be changed, added, and deleted, but some are read only.
<h1>Accessing Them</h1>
The syntax for accessing the property of an object is:
<pre>objectName.property // person.age</pre>
or
<pre>objectName["property"] // person["age"]</pre>
or
<pre>objectName[expression] // x = "age"; person[x]</pre>
Examples:
<pre>person.firstname + " is " + person.age + " years old.";</pre>
<pre>person["firstname"] + " is " + person["age"] + " years old.";</pre>
<h1>for...in</h1>
The JavaScript for...in statement loops through the properties of an object.
<br>
<b>Syntax:</b>
<pre>
for (let variable in object) {
  // code to be executed
}
</pre>
The block of code inside of the for...in loop will be executed once for each property.
<br>
Looping through the properties of an object:
<pre>
const person = {
  fname:" John",
  lname:" Doe",
  age: 25
};

for (let x in person) {
  txt += person[x];
}
</pre>
<h1>Adding New Properties</h1>
You can add new properties to an existing object by simply giving it a value.
<br>
Assume that the person object already exists - you can then give it new properties:
<pre>person.nationality = "English";</pre>
<h1>Deleting Properties</h1>
The <b>delete</b> keyword deletes a property from an object:
<pre>
const person = {
  firstName: "John",
  lastName: "Doe",
  age: 50,
  eyeColor: "blue"
};
delete person.age;
</pre>
or delete person["age"];
<pre>
const person = {
  firstName: "John",
  lastName: "Doe",
  age: 50,
  eyeColor: "blue"
};
delete person["age"];
</pre>
The <b>delete</b> keyword deletes both the value of the property and the property itself.
<br>
After deletion, the property cannot be used before it is added back again.
<br>
The <b>delete</b> operator is designed to be used on object properties. It has no effect on variables or functions.
<br>
The <b>delete</b> operator should not be used on predefined JavaScript object properties. It can crash your application.
<h1>Nested Objects</h1>
Values in an object can be another object:
<pre>
myObj = {
  name:"John",
  age:30,
  cars: {
    car1:"Ford",
    car2:"BMW",
    car3:"Fiat"
  }
}
</pre>
You can access nested objects using the dot notation or the bracket notation:
<pre>myObj.cars.car2;</pre>
or:
<pre>myObj.cars["car2"];</pre>
or:
<pre>myObj["cars"]["car2"];</pre>
or:
<pre>
let p1 = "cars";
let p2 = "car2";
myObj[p1][p2];
</pre>
<h1>Property Attributes</h1>
All properties have a name. In addition they also have a value.
<br>
The value is one of the property's attributes.
<br>
Other attributes are: enumerable, configurable, and writable.
<br>
These attributes define how the property can be accessed (is it readable?, is it writable?)
<br>
In JavaScript, all attributes can be read, but only the value attribute can be changed (and only if the property is writable).
<br>
(ECMAScript 5 has methods for both getting and setting all property attributes)
<h1>Prototype Properties</h1>
JavaScript objects inherit the properties of their prototype.
<br>
The <b>delete</b> keyword does not delete inherited properties, but if you delete a prototype property, it will affect all objects inherited from the prototype.
