<a href="/JS/Sets.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Typeof.md">Next &gt;</a>
<hr>
A Map holds key-value pairs where the keys can be any datatype.
<br>
A Map remembers the original insertion order of the keys.
<h1>Some Map Methods & Properties</h1>
<table class="ws-table-all notranslate">
  <tr>
    <th>Method</th>
    <th>Description</th>
  </tr>
  <tr>
    <td><a href="Sets.md#new-Set">new Set()</a></td>
    <td>Creates a new Set</td>
  </tr>
  <tr>
    <td><a href="Sets.md#add">add()</a></td>
    <td>Adds a new element to the Set</td>
  </tr>
  <tr>
    <td><a href="#delete">delete()</a></td>
    <td>Removes an element from a Set</td>
  </tr>
  <tr>
    <td><a href="#has">has()</a></td>
    <td>Returns true if a value exists in the Set</td>
  </tr>
  <tr>
    <td><a href="Sets.md#forEach">forEach()</a></td>
    <td>Invokes a callback for each element in the Set</td>
  </tr>
  <tr>
    <td><a href="Sets.md#values">values()</a></td>
    <td>Returns an iterator with all the values in a Set</td>
  </tr>
  <tr>
    <td><a href="#entries">entries()</a></td>
    <td>Returns an iterator with the <code>[key, value]</code> pairs in a Map</td>
  </tr>
</table>
<table class="ws-table-all notranslate">
  <tr>
    <th>Property</th>
    <th>Description</th>
  </tr>
  <tr>
    <td><a href="#size">size</a></td>
    <td>Returns the number of elements in a Set</td>
  </tr>
</table>
<h1>new Map()</h1>
You can create a Map by passing an Array to the <b>new Map()</b> constructor:
<pre>
// Create a Map
const fruits = new Map([
  ["apples", 500],
  ["bananas", 300],
  ["oranges", 200]
]);
</pre>
<h1>delete()</h1>
The delete() method removes a Map element:
<pre>fruits.delete("apples");</pre>
<h1>has()</h1>
The <b>has()</b> method returns true if a key exists in a Map:
<br>
<b>No:</b>
<pre>
fruits.has("apples");
</pre>
<b>Yes:</b>
<pre>
fruits.delete("apples");
fruits.has("apples");
</pre>
<h1>size()</h1>
The size property returns the number of elements in a Map:
<pre>fruits.size;</pre>
<h1>entries()</h1>
The <b>entries()</b> method returns an iterator object with the <code>[key, values]</code> in a Map:
<pre>
// List all entries
let text = "";
for (const x of fruits.entries()) {
  text += x;
}
</pre>
<h1>set()</h1>
You can add elements to a Map with the <b>set()</b> method:
<pre>
// Create a Map
const fruits = new Map();
// Set Map Values
fruits.set("apples", 500);
fruits.set("bananas", 300);
fruits.set("oranges", 200);
</pre>
The <b>set()</b> method can also be used to change existing Map values:
<pre>fruits.set("apples", 200);</pre>
<h1>get()</h1>
The <b>get()</b> method gets the value of a key in a Map:
<pre>fruits.get("apples"); // Returns 500</pre>
