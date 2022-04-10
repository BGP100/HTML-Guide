<a href="/JS/Arrays/Methods.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Arrays/Iteration.md">Next &gt;</a>
<hr>
The <b>sort()</b> method sorts an array alphabetically:
<pre>
const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.sort();
</pre>
<h1>Reversing an Array</h1>
The <b>reverse()</b> method reverses the elements in an array.
<br>
You can use it to sort an array in descending order:
<pre>
const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.sort();
fruits.reverse();
</pre>
<h1>Numeric Sort</h1>
By default, the <b>sort()</b> function sorts values as strings.
<br>
This works well for strings ("Apple" comes before "Banana").
<br>
However, if numbers are sorted as strings, "25" is bigger than "100", because "2" is bigger than "1".
<br>
Because of this, the <b>sort()</b> method will produce incorrect result when sorting numbers.
<br>
You can fix this by providing a compare function:
<pre>
const points = [40, 100, 1, 5, 25, 10];
points.sort(function(a, b){return a - b});
</pre>
<h1>The Compare Function</h1>
The purpose of the compare function is to define an alternative sort order.
<br>
The compare function should return a negative, zero, or positive value, depending on the arguments:
<pre>function(a, b){return a - b}</pre>
When the <b>sort()</b> function compares two values, it sends the values to the compare function, and sorts the values according to the returned (negative, zero, positive) value.
<br>
If the result is negative a is sorted before b.
<br>
If the result is positive b is sorted before a.
<br>
If the result is 0 no changes are done with the sort order of the two values.
<br>
<b>Example:</b>
<br>
The compare function compares all the values in the array, two values at a time (a, b).
<br>
When comparing 40 and 100, the sort() method calls the compare function(40, 100).
<br>
The function calculates 40 - 100 (a - b), and since the result is negative (-60),  the sort function will sort 40 as a value lower than 100.
<br>
You can use this code snippet to experiment with numerically and alphabetically sorting:
<pre>
&lt;button onclick="myFunction1()"&gt;Sort Alphabetically&lt;/button&gt;
&lt;button onclick="myFunction2()"&gt;Sort Numerically&lt;/button&gt;
&lt;p id="demo"&gt;&lt;/p&gt;
&lt;script>
const points = [40, 100, 1, 5, 25, 10];
document.getElementById("demo").innerHTML = points;
function myFunction1() {
  points.sort();
  document.getElementById("demo").innerHTML = points;
}
function myFunction2() {
  points.sort(function(a, b){return a - b});
  document.getElementById("demo").innerHTML = points;
}
&lt;/script&gt;
</pre>
<h1>Find the Highest (or Lowest) Array Value</h1>
There are no built-in functions for finding the max or min value in an array.
<br>
However, after you have sorted an array, you can use the index to obtain the highest and lowest values.
<br>
Sorting ascending:
<pre>
const points = [40, 100, 1, 5, 25, 10];
points.sort(function(a, b){return a - b});
// now points[0] contains the lowest value
// and points[points.length-1] contains the highest value
</pre>
Sorting descending:
<pre>
const points = [40, 100, 1, 5, 25, 10];
points.sort(function(a, b){return b - a});
// now points[0] contains the highest value
// and points[points.length-1] contains the lowest value
</pre>
<h1>Sorting Object Arrays</h1>
JavaScript arrays often contain objects:
<pre>
const cars = [
  {type:"Volvo", year:2016},
  {type:"Saab", year:2001},
  {type:"BMW", year:2010}
];
</pre>
Even if objects have properties of different data types, the sort() method can be used to sort the array.
<br>
The solution is to write a compare function to compare the property values:
<pre>cars.sort(function(a, b){return a.year - b.year});</pre>
Comparing string properties is a little more complex:
<pre>
cars.sort(function(a, b){
  let x = a.type.toLowerCase();
  let y = b.type.toLowerCase();
  if (x &lt; y) {return -1;}
  if (x &gt; y) {return 1;}
  return 0;
});
</pre>
