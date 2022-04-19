<a href="/JS/Classes/Inheritance.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Async/Callback.md">Next &gt;</a>
<hr>
Static class methods are defined on the class itself.
<br>
You cannot call a static method on an object, only on an object class.
<pre>
class Car {
  constructor(name) {
    this.name = name;
  }
  static hello() {
    return "Hello!!";
  }
}
let myCar = new Car("Ford");
// You can call 'hello()' on the Car Class:
document.getElementById("demo").innerHTML = Car.hello();
// But NOT on a Car Object:
// document.getElementById("demo").innerHTML = myCar.hello();
// this will raise an error.
</pre>
If you want to use the myCar object inside the static method, you can send it as a parameter:
<pre>
class Car {
  constructor(name) {
    this.name = name;
  }
  static hello(x) {
    return "Hello " + x.name;
  }
}
let myCar = new Car("Ford");
document.getElementById("demo").innerHTML = Car.hello(myCar);
</pre>
