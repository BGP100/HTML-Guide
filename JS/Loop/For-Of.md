<a href="/JS/Loop/For-In.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Loop/While.md">Next &gt;</a>
<hr>
The JavaScript <b>for of</b> statement loops through the values of an iterable object.
<br>
It lets you loop over iterable data structures such as Arrays, Strings, Maps, NodeLists, and more:
<br>
<b>Syntax:</b>
<pre>
for (variable of iterable) {
  // code block to be executed
}
</pre>
<b>variable</b> - For every iteration the value of the next property is assigned to the variable. Variable can be declared with <b>const</b>, <b>let</b>, or <b>var</b>.
<br>
<b>iterable</b> - An object that has iterable properties.
<h1>Looping over an Array</h1>
<pre>
const cars = ["BMW", "Volvo", "Mini"];
let text = "";
for (let x of cars) {
  text += x;
}
</pre>
<h1>Looping over a String</h1>
<pre>
let language = "JavaScript";
let text = "";
for (let x of language) {
text += x;
}
</pre>
