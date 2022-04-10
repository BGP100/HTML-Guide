<a href="/JS/Math/Main.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Math/Booleans.md">Next &gt;</a>
<hr>
<b>Math.random()</b> returns a random number between 0 (inclusive),  and 1 (exclusive):
<pre>Math.random(); // Returns a random number:</pre>
<h1>Integers</h1>
<b>Math.random()</b> used with <b>Math.floor()</b> can be used to return random integers.
<pre>Math.floor(Math.random() * 10); // Returns a random integer from 0 to 9:</pre>
<pre>Math.floor(Math.random() * 11); // Returns a random integer from 0 to 10:</pre>
<pre>Math.floor(Math.random() * 100); // Returns a random integer from 0 to 99:</pre>
<pre>Math.floor(Math.random() * 101); // Returns a random integer from 0 to 100:</pre>
<pre>Math.floor(Math.random() * 10) + 1; // Returns a random integer from 1 to 10:</pre>
<pre>Math.floor(Math.random() * 100) + 1; // Returns a random integer from 1 to 100:</pre>
<h1>A Proper Random Function</h1>
As you can see from the examples above, it might be a good idea to create a proper random function to use for all random integer purposes.
<br>
This JavaScript function always returns a random number between min (included) and max (excluded):
<pre>
function getRndInteger(min, max) {
  return Math.floor(Math.random() * (max - min) ) + min;
}
</pre>
This JavaScript function always returns a random number between min and max (both included):
<pre>
function getRndInteger(min, max) {
  return Math.floor(Math.random() * (max - min + 1) ) + min;
}
</pre>
