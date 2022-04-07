<h1>forEach()</h1>
The <b>forEach()</b> method calls a function (a callback function) once for each array element.
<pre>
const numbers = [45, 4, 9, 16, 25];
let txt = "";
numbers.forEach(myFunction);
function myFunction(value, index, array) {
  txt += value + "&lt;br&gt;";
}
</pre>
<h1>map()</h1>
The <b>map()</b> method creates a new array by performing a function on each array element.
<br>
The <b>map()</b> method does not execute the function for array elements without values.
<br>
The <b>map()</b> method does not change the original array.
<br>
This example multiplies each array value by 2:
<pre>
const numbers1 = [45, 4, 9, 16, 25];
const numbers2 = numbers1.map(myFunction);
function myFunction(value, index, array) {
  return value * 2;
}
</pre>
<h1>filter()</h1>
The <b>filter()</b> method creates a new array with array elements that passes a test.
<br>
This example creates a new array from elements with a value larger than 18:
<pre>
const numbers = [45, 4, 9, 16, 25];
const over18 = numbers.filter(myFunction);
function myFunction(value, index, array) {
  return value &gt; 18;
}
</pre>
<h1>reduce()</h1>
The <b>reduce()</b> method runs a function on each array element to produce (reduce it to) a single value.
<br>
The <b>reduce()</b> method works from left-to-right in the array. See also reduceRight().
<br>
The <b>reduce()</b> method does not reduce the original array.
<br>
<b>Note:</b>  This example finds the sum of all numbers in an array:
<pre>
const numbers = [45, 4, 9, 16, 25];
let sum = numbers.reduce(myFunction);
function myFunction(total, value, index, array) {
  return total + value;
}
</pre>
<h1>reduceRight()</h1>
The <b>reduceRight()</b> method runs a function on each array element to produce (reduce it to) a single value.
<br>
The <b>reduceRight()</b> works from right-to-left in the array. See also reduce().
<br>
<b>Note:</b> The <b>reduceRight()</b> method does not reduce the original array.
<br>
This example finds the sum of all numbers in an array:
<pre>
const numbers = [45, 4, 9, 16, 25];
let sum = numbers.reduceRight(myFunction);
function myFunction(total, value, index, array) {
  return total + value;
}
</pre>
<h1>every()</h1>
The <b>every()</b> method check if all array values pass a test.
<br>
This example check if all array values are larger than 18:
<pre>
const numbers = [45, 4, 9, 16, 25];
let allOver18 = numbers.every(myFunction);
function myFunction(value, index, array) {
  return value &gt; 18;
}
</pre>
<h1>some()</h1>
The <b>some()</b> method check if some array values pass a test.
<br>
This example check if some array values are larger than 18:
<pre>
const numbers = [45, 4, 9, 16, 25];
let someOver18 = numbers.some(myFunction);
function myFunction(value, index, array) {
  return value &gt; 18;
}
</pre>
<h1>find()</h1>
The <b>find()</b> method returns the value of the first array element that passes a test function.
<br>
This example finds (returns the value of) the first element that is larger than 18:
<pre>
const numbers = [4, 9, 16, 25, 29];
let first = numbers.find(myFunction);
function myFunction(value, index, array) {
  return value &gt; 18;
}
</pre>
<h1findIndex()
The <b>findIndex()</b> method returns the index of the first array element that passes a test function.
<br>
This example finds the index of the first element that is larger than 18:
<pre>
const numbers = [4, 9, 16, 25, 29];
let first = numbers.findIndex(myFunction);
function myFunction(value, index, array) {
  return value &gt; 18;
}
</pre>
<h1>Array.from()</h1>
The <b>Array.from()</b> method returns an Array object from any object with a length property or any iterable object.
<pre>Array.from("ABCDEFG");</pre>
<h1>Keys()</h1>
The Array.keys() method returns an Array Iterator object with the keys of an array.
<pre>
const fruits = ["Banana", "Orange", "Apple", "Mango"];
const keys = fruits.keys();
for (let x of keys) {
  text += x + "&lt;br&gt;";
}
</pre>
<h1>entries()</h1>
Create an Array Iterator, and then iterate over the key/value pairs:
<pre>
const fruits = ["Banana", "Orange", "Apple", "Mango"];
const f = fruits.entries();
for (let x of f) {
  document.getElementById("demo").innerHTML += x;
}
</pre>
