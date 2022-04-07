The JavaScript method <b>toString()</b> converts an array to a string of (comma separated) array values.
<pre>
const fruits = ["Banana", " Orange", " Apple", " Mango"];
document.getElementById("demo").innerHTML = fruits.toString();
</pre>
<b>Result:</b> <code>Banana, Orange, Apple, Mango</code>
<br>
The <b>join()</b> method also joins all array elements into a string.
<br>
It behaves just like <b>toString()</b>, but in addition you can specify the separator:
<pre>
const fruits = ["Banana", "Orange", "Apple", "Mango"];
document.getElementById("demo").innerHTML = fruits.join(" * ");
</pre>
<b>Result:</b> <code>Banana * Orange * Apple * Mango</code>
<h1>pop()</h1>
The <b>pop()</b> method removes the last element from an array:
<pre>
const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.pop();
</pre>
The <b>pop()</b> method returns the value that was "popped out":
<pre>
const fruits = ["Banana", "Orange", "Apple", "Mango"];
let fruit = fruits.pop();
</pre>
<h1>push()</h1>
The <b>push()</b> method adds a new element to an array (at the end):
<pre>
const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.push("Kiwi");
</pre>
The <b>push()</b> method returns the new array length:
<pre>
const fruits = ["Banana", "Orange", "Apple", "Mango"];
let length = fruits.push("Kiwi");
</pre>
<h1>shift()</h1>
The <b>shift()</b> method removes the first array element and "shifts" all other elements to a lower index.
<pre>
const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.shift();
</pre>
The <b>shift()</b> method returns the value that was "shifted out":
<pre>
const fruits = ["Banana", "Orange", "Apple", "Mango"];
let fruit = fruits.shift();
</pre>
<h1>unshift()</h1>
The <b>unshift()</b> method adds a new element to an array (at the beginning), and "unshifts" older elements:
<pre>
const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.unshift("Lemon");
</pre>
The <b>unshift()</b> method returns the new array length.
<pre>
const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.unshift("Lemon");
</pre>
<h1>delete()</h1>
WARNING!!!
Array elements can be deleted using the JavaScript operator delete.
<br>
Using delete leaves undefined holes in the array.
<br>
Use <b>pop()</b> or <b>shift()</b> instead.
<pre>
const fruits = ["Banana", "Orange", "Apple", "Mango"];
delete fruits[0];
</pre>
<h1>slice()</h1>
The <b>slice()</b> method slices out a piece of an array into a new array.
<br>
This example slices out a part of an array starting from array element 1 ("Orange"):
<pre>
const fruits = ["Banana", "Orange", "Lemon", "Apple", "Mango"];
const citrus = fruits.slice(1);
</pre>
<h1>toString()</h1>
JavaScript automatically converts an array to a comma separated string when a primitive value is expected.
<br>
This is always the case when you try to output an array.
<br>
These two examples will produce the same result:
<pre>
const fruits = ["Banana", "Orange", "Apple", "Mango"];
document.getElementById("demo").innerHTML = fruits.toString();
</pre>
<pre>
const fruits = ["Banana", "Orange", "Apple", "Mango"];
document.getElementById("demo").innerHTML = fruits;
</pre>
