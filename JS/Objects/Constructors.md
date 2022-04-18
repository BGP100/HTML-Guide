<a href="/JS/Objects/Accessors.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Objects/Prototypes.md">Next &gt;</a>
<hr>
<pre>
function Person(first, last, age, eye) {
  this.firstName = first;
  this.lastName = last;
  this.age = age;
  this.eyeColor = eye;
}
</pre>
<h1>Object Types (Blueprints) (Classes)</h1>
The examples from the previous chapters are limited. They only create single objects.
<br>
Sometimes we need a "blueprint" for creating many objects of the same "type".
<br>
The way to create an "object type", is to use an object constructor function.
<br>
In the example above, function Person() is an object constructor function.
<br>
Objects of the same type are created by calling the constructor function with the new keyword:
<pre>
const myFather = new Person("John", "Doe", 50, "blue");
const myMother = new Person("Sally", "Rally", 48, "green");
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
<h1>Adding New Properties</h1>
You can add new properties to an existing object by simply giving it a value.
<br>
Assume that the person object already exists - you can then give it new properties:
<pre>person.nationality = "English";</pre>
<h1>Adding a Method to an Object</h1>
Adding a new method to an object is easy:
<pre>
person.name = function () {
  return this.firstName + " " + this.lastName;
};
</pre>
<h1>Adding a Property to a Constructor</h1>
You cannot add a new property to an object constructor the same way you add a new property to an existing object:
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
This way object properties can have default values.
<h1>Adding a Method to a Constructor</h1>
Your constructor function can also define methods:
<pre>
function Person(first, last, age, eyecolor) {
  this.firstName = first;
  this.lastName = last;
  this.age = age;
  this.eyeColor = eyecolor;
  this.name = function() {
    return this.firstName + " " + this.lastName;
  };
}
</pre>
You cannot add a new method to an object constructor the same way you add a new method to an existing object.
<br>
Adding methods to an object constructor must be done inside the constructor function:
<pre>
function Person(firstName, lastName, age, eyeColor) {
  this.firstName = firstName; 
  this.lastName = lastName;
  this.age = age;
  this.eyeColor = eyeColor;
  this.changeName = function (name) {
    this.lastName = name;
  };
}
</pre>
The changeName() function assigns the value of name to the person's lastName property.
<br>
Now You Can Try:
<pre>myMother.changeName("Doe");</pre>
<h1>Did You Know?</h1>
As you can see above, JavaScript has object versions of the primitive data types String, Number, and Boolean. But there is no reason to create complex objects. Primitive values are much faster:
<ul>
  <li>Use string literals <b>""</b> instead of <b>new String()</b>.</li>
  <li>Use number literals <b>50</b> instead of <b>new Number()</b>.</li>
  <li>Use boolean literals <b>true / false</b> instead of <b>new Boolean()</b>.</li>
  <li>Use object literals <b>{}</b> instead of <b>new Object()</b>.</li>
  <li>Use array literals <b>[]</b> instead of <b>new Array()</b>.</li>
  <li>Use pattern literals <b>/()/</b> instead of <b>new RegExp()</b>.</li>
  <li>Use function expressions <b>() {}</b> instead of <b>new Function()</b>.</li>
</ul>
<h1>String Objects</h1>
Normally, strings are created as primitives: firstName = "John"
<br>
But strings can also be created as objects using the new keyword:
<pre>firstName = new String("John")</pre>
<br>
Learn why strings should not be created as object in the chapter <a href="/JS/Strings/Main.md">JS Strings</a>.
<h1>Number Objects</h1>
Normally, numbers are created as primitives: x = 30
<br>
But numbers can also be created as objects using the new keyword:
<pre>x = new Number(30)</pre>
<br>
Learn why numbers should not be created as object in the chapter <a href="/JS/Numbers/Main.md">JS Numbers</a>.
<h1>Boolean Objects</h1>
Normally, booleans are created as primitives: x = false
<br>
But booleans can also be created as objects using the new keyword:
<pre>x = new Boolean(false)</pre>
<br>
Learn why booleans should not be created as object in the chapter <a href="/JS/Math/Booleans.md">JS Booleans</a>.
