<a href="/JS/Functions/Method/Call.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Functions/Method/Bind.md">Next &gt;</a>
<hr>
<h1>Method Reuse</h1>
With the <b>apply()</b> method, you can write a method that can be used on different objects.
<h1>apply()</h1>
The apply() method is similar to the call() method (previous chapter).
<br>
In this example the fullName method of person is applied on person1:
<pre>
const person = {
  fullName: function() {
    return this.firstName + " " + this.lastName;
  }
}
const person1 = {
  firstName: "Mary",
  lastName: "Doe"
}
// This will return "Mary Doe":
person.fullName.apply(person1);
</pre>
<h2>Difference Between call() and apply()</h2>
The difference is:
<br>
The <b>call()</b> method takes arguments separately.
<br>
The <b>apply()</b> method takes arguments as an array.
<h1>apply() with Arguments</h1>
The <b>apply()</b> method accepts arguments in an array:
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
person.fullName.apply(person1, ["Oslo", "Norway"]);
</pre>
Compared with the <b>call()</b> method:
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
<h1>Simulate a Max Method on Arrays</h1>
You can find the largest number (in a list of numbers) using the Math.max() method:
<pre>Math.max(1,2,3); // Will return 3</pre>
Since JavaScript arrays do not have a max() method, you can apply the Math.max() method instead.
<pre>Math.max.apply(null, [1,2,3]); // Will also return 3</pre>
The first argument (null) does not matter. It is not used in this example.
<br>
These examples will give the same result:
<pre>Math.max.apply(Math, [1,2,3]); // Will also return 3</pre>
<pre>Math.max.apply(" ", [1,2,3]); // Will also return 3</pre>
<pre>Math.max.apply(0, [1,2,3]); // Will also return 3</pre>
<h1>Strict Mode</h1>
In JavaScript strict mode, if the first argument of the <b>apply()</b> method is not an object, it becomes the owner (object) of the invoked function. In "non-strict" mode, it becomes the global object.
