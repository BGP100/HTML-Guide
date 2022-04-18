<a href="/JS/Objects/Prototypes.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Objects/Sets.md">Next &gt;</a>
<hr>
Iterable objects are objects that can be iterated over with <b>for..of</b>.
<br>
Technically, iterables must implement the <b>Symbol.iterator</b> method.
<h1>Iterating Over a String</h1>
You can use a <b>for..of</b> loop to iterate over the elements of a string:
<pre>
for (const x of "BledyGames") {
  // code block to be executed
}
</pre>
<h1>Iterating Over an Array</h1>
You can use a for..of loop to iterate over the elements of an Array:
<pre>
for (const x of [1,2,3,4,5] {
  // code block to be executed
}
<h1>Iterators</h1>
The iterator protocol defines how to produce a sequence of values from an object.
<br>
An object becomes an iterator when it implements a <b>next()</b> method.
<br>
The <b>next()</b> method must return an object with two properties:
<ul>
  <li>value (the next value)</li>
  <li>done (true or false)</li>
</ul>
<h1>Home Made Iterable
This iterable returns never ending: 10,20,30,40,.... Everytime <b>next()</b> is called:
<pre>
// Home Made Iterable
function myNumbers() {
  let n = 0;
  return {
    next: function() {
      n += 10;
      return {value:n, done:false};
    }
  };
}
// Create Iterable
const n = myNumbers();
n.next(); // Returns 10
n.next(); // Returns 20
n.next(); // Returns 30
</pre>
A JavaScript iterable is an object that has a Symbol.iterator.
<br>
The <b>Symbol.iterator</b> is a function that returns a next() function.
<br>
An iterable can be iterated over with the code: for (const x of iterable) { }
<pre>
// Create an Object
myNumbers = {};
// Make it Iterable
myNumbers[Symbol.iterator] = function() {
  let n = 0;
  done = false;
  return {
    next() {
      n += 10;
      if (n == 100) {done = true}
      return {value:n, done:done};
    }
  };
}
</pre>
Now you can use <b>for..of</b>:
<pre>
for (const num of myNumbers) {
  // Any Code Here
}
</pre>
The <b>Symbol.iterator</b> method is called automatically by for..of.
<br>
But we can also do it "manually":
<pre>
let iterator = myNumbers[Symbol.iterator]();
while (true) {
  const result = iterator.next();
  if (result.done) break;
  // Any Code Here
}
</pre>
