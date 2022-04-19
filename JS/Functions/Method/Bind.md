<a href="/JS/Functions/Method/Apply.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Functions/Closures.md">Next &gt;</a>
<hr>
With the <b>bind()</b> method, an object can borrow a method from another object.
<br>
The example below creates 2 objects (person and member).
<br>
The member object borrows the fullname method from the person object:
<pre>
const person = {
  firstName:"John",
  lastName: "Doe",
  fullName: function () {
    return this.firstName + " " + this.lastName;
  }
}
const member = {
  firstName:"Hege",
  lastName: "Nilsen",
}
let fullName = person.fullName.bind(member);
</pre>
<h1>Preserving the this Keyword</h1>
Sometimes the <b>bind()</b> method has to be used to prevent loosing this.
<br>
In the following example, the person object has a display method. In the display method, this refers to the person object:
<pre>
const person = {
  firstName:"John",
  lastName: "Doe",
  display: function () {
    let x = document.getElementById("demo");
    x.innerHTML = this.firstName + " " + this.lastName;
  }
}
person.display();
</pre>
When a function is used as a callback, this is lost.
<br>
This example will try to display the person name after 3 seconds, but it will display undefined instead:
<pre>
const person = {
  firstName:"John",
  lastName: "Doe",
  display: function () {
    let x = document.getElementById("demo");
    x.innerHTML = this.firstName + " " + this.lastName;
  }
}
setTimeout(person.display, 3000);
</pre>
The <b>bind()</b> method solves this problem.
<br>
In the following example, the bind() method is used to bind person.display to person.
<br>
This example will display the person name after 3 seconds:
<pre>
const person = {
  firstName:"John",
  lastName: "Doe",
  display: function () {
    let x = document.getElementById("demo");
    x.innerHTML = this.firstName + " " + this.lastName;
  }
}
let display = person.display.bind(person);
setTimeout(display, 3000);
</pre>
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
<b><i>Note:</i> this</b> is not a variable. It is a keyword. You cannot change the value of <b>this</b>.
<br>
Checkout <a href="/JS/This.md">the this keyword</a> chapter!
