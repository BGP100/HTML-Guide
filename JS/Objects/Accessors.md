<a href="/JS/Objects/Display.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Objects/Constructors.md">Next &gt;</a>
<hr>
<h1>Accessors (Getters and Setters)</h1>
ECMAScript 5 (ES5 2009) introduced Getter and Setters.
<br>
Getters and setters allow you to define Object Accessors (Computed Properties).
<h1>Getter (The get Keyword)</h1>
This example uses a lang property to get the value of the language property.
<pre>
// Create an object:
const person = {
  firstName: "John",
  lastName: "Doe",
  language: "en",
  get lang() {
    return this.language;
  }
};
// Display data from the object using a getter:
document.getElementById("demo").innerHTML = person.lang;
</pre>
<h1>Setter (The set Keyword)</h1>
This example uses a lang property to set the value of the language property.
<pre>
const person = {
  firstName: "John",
  lastName: "Doe",
  language: "",
  set lang(lang) {
    this.language = lang;
  }
};
// Set an object property using a setter:
person.lang = "en";
// Display data from the object:
document.getElementById("demo").innerHTML = person.language;
</pre>
<h1>Function or Getter?</h1>
What is the differences between these two examples?
<pre>
const person = {
  firstName: "John",
  lastName: "Doe",
  fullName: function() {
    return this.firstName + " " + this.lastName;
  }
};
// Display data from the object using a method:
document.getElementById("demo").innerHTML = person.fullName();
</pre>
<pre>
const person = {
  firstName: "John",
  lastName: "Doe",
  get fullName() {
    return this.firstName + " " + this.lastName;
  }
};
// Display data from the object using a getter:
document.getElementById("demo").innerHTML = person.fullName;
</pre>
Example 1 access fullName as a function: person.fullName().
<br>
Example 2 access fullName as a property: person.fullName.
<br>
The second example provides a simpler syntax.
<h1>Data Quality</h1>
JavaScript can secure better data quality when using getters and setters.
<br>
Using the lang property, in this example, returns the value of the language property in upper case:
<pre>
// Create an object:
const person = {
  firstName: "John",
  lastName: "Doe",
  language: "en",
  get lang() {
    return this.language.toUpperCase();
  }
};
// Display data from the object using a getter:
document.getElementById("demo").innerHTML = person.lang;
</pre>
Using the lang property, in this example, stores an upper case value in the language property:
<pre>
const person = {
  firstName: "John",
  lastName: "Doe",
  language: "",
  set lang(lang) {
    this.language = lang.toUpperCase();
  }
};
// Set an object property using a setter:
person.lang = "en";
// Display data from the object:
document.getElementById("demo").innerHTML = person.language;
</pre>
<h1>Why Using Getters and Setters?</h1>
<ul>
  <li>It gives simpler syntax.</li>
  <li>It allows equal syntax for properties and methods.</li>
  <li>It can secure better data quality.</li>
  <li>It is useful for doing things behind-the-scenes.</li>
</ul>
<h1>Object.defineProperty()</h1>
The Object.defineProperty() method can also be used to add Getters and Setters:
<pre>
// Define object
const obj = {counter : 0};
// Define setters
Object.defineProperty(obj, "reset", {
  get : function () {this.counter = 0;}
});
Object.defineProperty(obj, "increment", {
  get : function () {this.counter++;}
});
Object.defineProperty(obj, "decrement", {
  get : function () {this.counter--;}
});
Object.defineProperty(obj, "add", {
  set : function (value) {this.counter += value;}
});
Object.defineProperty(obj, "subtract", {
  set : function (value) {this.counter -= value;}
});
// Play with the counter:
obj.reset;
obj.add = 5;
obj.subtract = 1;
obj.increment;
obj.decrement;
</pre>
