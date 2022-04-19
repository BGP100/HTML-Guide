<a href="/JS/Classes/Introduction.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Classes/Static.md">Next &gt;</a>
<hr>
To create a class inheritance, use the extends keyword.
<br>
A class created with a class inheritance inherits all the methods from another class:
<pre>
class Car {
  constructor(brand) {
    this.carname = brand;
  }
  present() {
    return "I have a " + this.carname;
  }
}
class Model extends Car {
  constructor(brand, mod) {
    super(brand);
    this.model = mod;
  }
  show() {
    return this.present() + ", it is a " + this.model;
  }
}
let myCar = new Model("Ford", "Mustang");
document.getElementById("demo").innerHTML = myCar.show();
</pre>
The <b>super()</b> method refers to the parent class.
<br>
By calling the <b>super()</b> method in the constructor method, we call the parent's constructor method and gets access to the parent's properties and methods.
<br>
<b>Note:</b> Inheritance is useful for code reusability: reuse properties and methods of an existing class when you create a new class.
<h1>Getters and Setters</h1>
Classes also allows you to use getters and setters.
<br>
It can be smart to use getters and setters for your properties, especially if you want to do something special with the value before returning them, or before you set them.
<br>
To add getters and setters in the class, use the <b>get</b> and <b>set</b> keywords.
<pre>
class Car {
  constructor(brand) {
    this.carname = brand;
  }
  get cnam() {
    return this.carname;
  }
  set cnam(x) {
    this.carname = x;
  }
}
let myCar = new Car("Ford");
document.getElementById("demo").innerHTML = myCar.cnam;
</pre>
The name of the getter/setter method cannot be the same as the name of the property, in this case carname.
<br>
Many programmers use an underscore character <code>_</code> before the property name to separate the getter/setter from the actual property:
<pre>
class Car {
  constructor(brand) {
    this._carname = brand;
  }
  get carname() {
    return this._carname;
  }
  set carname(x) {
    this._carname = x;
  }
}
let myCar = new Car("Ford");
document.getElementById("demo").innerHTML = myCar.carname;
</pre>
To use a setter, use the same syntax as when you set a property value, without parentheses:
<pre>
class Car {
  constructor(brand) {
    this._carname = brand;
  }
  get carname() {
    return this._carname;
  }
  set carname(x) {
    this._carname = x;
  }
}
let myCar = new Car("Ford");
myCar.carname = "Volvo";
document.getElementById("demo").innerHTML = myCar.carname;
</pre>
<h1>Hoisting</h1>
Unlike functions, and other JavaScript declarations, class declarations are not hoisted.
<br>
That means that you must declare a class before you can use it:
<pre>
// You cannot use the class yet.
// myCar = new Car("Ford")
// This would raise an error.
class Car {
  constructor(brand) {
    this.carname = brand;
  }
}
// Now you can use the class:
let myCar = new Car("Ford")
</pre>
<b>Note:</b> For other declarations, like functions, you will NOT get an error when you try to use it before it is declared, because the default behavior of JavaScript declarations are hoisting (moving the declaration to the top).
