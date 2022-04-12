<a href="/JS/Labels.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Sets.md">Next &gt;</a>
<hr>
Iterables are iterable objects (like Arrays).
<br>
Iterables can be accessed with simple and efficient code.
<br>
Iterables can be iterated over with <b>for..of</b> loops.
<hr>
Iterating is easy to understand.
<br>
It simply means looping over a sequence of elements.
<br>
Here are some easy examples:
<ul>
  <li>Iterating over a String</li>
  <li>Iterating over an Array</li>
</ul>
<h1>Examples</h1>
The JavaScript <b>for..of</b> statement loops through the elements of an iterable object.
<pre>
for (variable of iterable) {
  // code block to be executed
}
</pre>
<hr>
You can use a <b>for..of</b> loop to iterate over the elements of a string:
<pre>
const name = "BledyGames";

for (const x of name) {
  // code block to be executed
}
</pre>
<hr>
You can use a <b>for..of</b> loop to iterate over the elements of an Array:
<pre>
const letters = ["a","b","c"];
for (const x of letters) {
  // code block to be executed
}
</pre>
<hr>
You can use a <b>for..of</b> loop to iterate over the elements of a Map:
<pre>
const fruits = new Map([
  ["apples", 500],
  ["bananas", 300],
  ["oranges", 200]
]);
for (const x of fruits) {
  // code block to be executed
}
</pre>
