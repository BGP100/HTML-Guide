<a href="/JS/Arrows.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Modules.md">Next &gt;</a>
<hr>
ECMAScript 2015, also known as ES6, introduced JavaScript Classes.
<br>
JavaScript Classes are templates for JavaScript Objects.
<h1>Syntax</h1>
Use the keyword <b>class</b> to create a class.
<br>
Always add a method named <b>constructor()</b>:
<pre>
class ClassName {
  constructor() { ... }
}
</pre>
<pre>
class Car {
  constructor(name, year) {
    this.name = name;
    this.year = year;
  }
}
</pre>
The example above creates a class named "Car".
<br>
The class has two initial properties: "name" and "year".
<h1>Using a Class</h1>
When you have a class, you can use the class to create objects:
<pre>
let myCar1 = new Car("Ford", 2014);
let myCar2 = new Car("Audi", 2019);
</pre>
The example above uses the Car class to create two Car objects.
<h1>constructor()</h1>
The constructor method is a special method:
<ul>
  <li>It has to have the exact name "constructor".</li>
  <li>It is executed automatically when a new object is created.</li>
  <li>It is used to initialize object properties.</li>
</ul>
If you do not define a constructor method, JavaScript will add an empty constructor method..
<h1>Methods</h1>
Class methods are created with the same syntax as object methods.
<br>
Use the keyword <b>class</b> to create a class.
<br>
Always add a <b>constructor()</b> method.
<br>
Then add any number of methods.
<pre>
class ClassName {
  constructor() { ... }
  method_1() { ... }
  method_2() { ... }
  method_3() { ... }
}
</pre>
Create a Class method named "age", that returns the Car age:
<pre>
class Car {
  constructor(name, year) {
    this.name = name;
    this.year = year;
  }
  age() {
    let date = new Date();
    return date.getFullYear() - this.year;
  }
}
let myCar = new Car("Ford", 2014);
document.getElementById("demo").innerHTML = "My car is " + myCar.age() + " years old.";
</pre>
You can send parameters to Class methods:
<pre>
class Car {
  constructor(name, year) {
    this.name = name;
    this.year = year;
  }
  age(x) {
    return x - this.year;
  }
}
let date = new Date();
let year = date.getFullYear();
let myCar = new Car("Ford", 2014);
document.getElementById("demo").innerHTML="My car is "+myCar.age(year)+" years old.";
</pre>
<h1>Browser Support</h1>
The following table defines the first browser version with full support for Classes in JavaScript:
<table class="ws-table-all notranslate">
  <tr>
    <th>Browser</th>
    <th>Chrome</th>
    <th>Edge</th>
    <th>Firefox</th>
    <th>Safari</th>
    <th>Opera</th>
  </tr>
  <tr>
    <td>Version</td>
    <td>49.0</td>
    <td>12.0</td>
    <td>45.0</td>
    <td>9.0</td>
    <td>36.0</td>
  </tr>
</table>
