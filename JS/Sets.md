<a href="/JS/Iterables.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Maps.md">Next &gt;</a>
<hr>
A JavaScript Set is a collection of unique values.
<br>
Each value can only occur once in a Set.
<h1>How To Create One</h1>
You can create a JavaScript Set by:
<ul>
  <li>Passing an Array to new <b>Set()</b></li>
  <li>Create a new Set and use <b>add()</b> to add values</li>
  <li>Create a new Set and use <b>add()</b> to add variables</li>
</ul>
<h1>Some Set Methods & Properties</h1>
<table class="ws-table-all notranslate">
  <tr>
    <th>Method</th>
    <th>Description</th>
  </tr>
  <tr>
    <td><a href="#new-Set">new Set()</a></td>
    <td>Creates a new Set</td>
  </tr>
  <tr>
    <td><a href="#new-Map">new Map()</a></td>
    <td>Creates a new Map</td>
  </tr>
  <tr>
    <td><a href="Maps.md#get">get()</a></td>
    <td>Gets the value for a key in a Map</td>
  </tr>
  <tr>
    <td><a href="Maps.md#set">set()</a></td>
    <td>Sets the value for a key in a Map</td>
  </tr>
  <tr>
    <td><a href="#add">add()</a></td>
    <td>Adds a new element to the Set</td>
  </tr>
  <tr>
    <td><a href="Maps.md#delete">delete()</a></td>
    <td>Removes an element from a Set</td>
  </tr>
  <tr>
    <td><a href="Maps.md#has">has()</a></td>
    <td>Returns true if a value exists in the Set</td>
  </tr>
  <tr>
    <td><a href="#forEach">forEach()</a></td>
    <td>Invokes a callback for each element in the Set</td>
  </tr>
  <tr>
    <td><a href="#values">values()</a></td>
    <td>Returns an iterator with all the values in a Set</td>
  </tr>
  <tr>
    <td><a href="Maps.md#entries">entries()</a></td>
    <td>Returns an iterator with the <code>[key, value]</code> pairs in a Map</td>
  </tr>
</table>
<table class="ws-table-all notranslate">
  <tr>
    <th>Property</th>
    <th>Description</th>
  </tr>
  <tr>
    <td><a href="/JS/Maps.md#size">size</a></td>
    <td>Returns the number of elements in a Set</td>
  </tr>
</table>
<h1>new Set()</h1>
Pass an Array to the new Set() constructor:
<pre>
// Create a Set
const letters = new Set(["a","b","c"]);
Create a Set and add values:
</pre>
<pre>
// Create a Set
const letters = new Set();
// Add Values to the Set
letters.add("a");
letters.add("b");
letters.add("c");
Create a Set and add variables:
</pre>
<pre>
// Create a Set
const letters = new Set();
// Create Variables
const a = "a";
const b = "b";
const c = "c";
// Add Variables to the Set
letters.add(a);
letters.add(b);
letters.add(c);
</pre>
<h1>add()</h1>
<pre>
letters.add("d");
letters.add("e");
</pre>
If you add equal elements, only the first will be saved:
<pre>
letters.add("a");
letters.add("b");
letters.add("c");
letters.add("c");
letters.add("c");
letters.add("c");
letters.add("c");
letters.add("c");
</pre>
<h1>forEach()</h1>
The <b>forEach()</b> method invokes (calls) a function for each Set element:
<pre>
// Create a Set
const letters = new Set(["a","b","c"]);
// List all Elements
let text = "";
letters.forEach (function(value) {
  text += value;
});
</pre>
<h1>values()</h1>
The values() method returns a new iterator object containing all the values in a Set:
<pre>letters.values(); // Returns [object Set Iterator]</pre>
Now you can use the Iterator object to access the elements:
<pre>
// List all Elements
let text = "";
for (const x of letters.values()) {
  text += x;
}
</pre>
