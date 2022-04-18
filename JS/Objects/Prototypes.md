All JavaScript objects inherit properties and methods from a prototype.
<br>
In the previous chapter we learned how to use an object constructor:
<pre>
function Person(first, last, age, eyecolor) {
  this.firstName = first;
  this.lastName = last;
  this.age = age;
  this.eyeColor = eyecolor;
}
const myFather = new Person("John", "Doe", 50, "blue");
const myMother = new Person("Sally", "Rally", 48, "green");
</pre>
We also learned that you can not add a new property to an existing object constructor:
<pre>Person.nationality = "English";</pre>
To add a new property to a constructor, you must add it to the constructor function:
<pre>
function Person(first, last, age, eyecolor) {
  this.firstName = first;
  this.lastName = last;
  this.age = age;
  this.eyeColor = eyecolor;
  this.nationality = "English";
}
</pre>
<h1>Prototype Inheritance</h1>
All JavaScript objects inherit properties and methods from a prototype:
<ul>
  <li>Date objects inherit from Date.prototype</li>
  <li>Array objects inherit from Array.prototype</li>
  <li>Person objects inherit from Person.prototype</li>
</ul>
The Object.prototype is on the top of the prototype inheritance chain:
<br>
Date objects, Array objects, and Person objects inherit from Object.prototype.
<h1>Adding Properties and Methods to Objects</h1>
Sometimes you want to add new properties (or methods) to all existing objects of a given type.
<br>
Sometimes you want to add new properties (or methods) to an object constructor.
<h1>prototype</h1>
The JavaScript prototype property allows you to add new properties to object constructors:
<pre>
function Person(first, last, age, eyecolor) {
  this.firstName = first;
  this.lastName = last;
  this.age = age;
  this.eyeColor = eyecolor;
}
Person.prototype.nationality = "English";
</pre>
The JavaScript prototype property also allows you to add new methods to objects constructors:
<pre>
function Person(first, last, age, eyecolor) {
  this.firstName = first;
  this.lastName = last;
  this.age = age;
  this.eyeColor = eyecolor;
}
Person.prototype.name = function() {
  return this.firstName + " " + this.lastName;
};
</pre>
