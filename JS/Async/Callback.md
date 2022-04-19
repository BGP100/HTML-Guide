<a href="/JS/Classes/Static.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Async/Asynchronous.md">Next &gt;</a>
<hr>
A callback is a function passed as an argument to another function.
<br>
This technique allows a function to call another function.
<br>
A callback function can run after another function has finished.
<h1>Sequence</h1>
JavaScript functions are executed in the sequence they are called. Not in the sequence they are defined.
<br>
This example will end up displaying "Goodbye":
<pre>
function myFirst() {
  myDisplayer("Hello");
}
function mySecond() {
  myDisplayer("Goodbye");
}
myFirst();
mySecond();
</pre>
This example will end up displaying "Hello":
<pre>
function myFirst() {
  myDisplayer("Hello");
}
function mySecond() {
  myDisplayer("Goodbye");
}
mySecond();
myFirst();
</pre>
<h1>Sequence Control</h1>
Sometimes you would like to have better control over when to execute a function.
<br>
Suppose you want to do a calculation, and then display the result.
<br>
You could call a calculator function (myCalculator), save the result, and then call another function (myDisplayer) to display the result:
<pre>
function myDisplayer(some) {
  document.getElementById("demo").innerHTML = some;
}
function myCalculator(num1, num2) {
  let sum = num1 + num2;
  return sum;
}
let result = myCalculator(5, 5);
myDisplayer(result);
</pre>
Or, you could call a calculator function (myCalculator), and let the calculator function call the display function (myDisplayer):
<pre>
function myDisplayer(some) {
  document.getElementById("demo").innerHTML = some;
}
function myCalculator(num1, num2) {
  let sum = num1 + num2;
  myDisplayer(sum);
}
myCalculator(5, 5);
</pre>
The problem with the first example above, is that you have to call two functions to display the result.
<br>
The problem with the second example, is that you cannot prevent the calculator function from displaying the result.
<br>
Now it is time to bring in a callback.
<h1>Callbacks</h1>
A callback is a function passed as an argument to another function.
<br>
Using a callback, you could call the calculator function (myCalculator) with a callback, and let the calculator function run the callback after the calculation is finished:
<pre>
function myDisplayer(some) {
  document.getElementById("demo").innerHTML = some;
}
function myCalculator(num1, num2, myCallback) {
  let sum = num1 + num2;
  myCallback(sum);
}
myCalculator(5, 5, myDisplayer);
</pre>
In the example above, <b>myDisplayer</b> is the name of a function.
<br>
It is passed to <b>myCalculator()</b> as an argument.
<h1>When to Use a Callback?</h1>
The examples above are not very exciting.
<br>
They are simplified to teach you the callback syntax.
<br>
Where callbacks really shine are in asynchronous functions, where one function has to wait for another function (like waiting for a file to load).
<br>
Asynchronous functions are covered in the next chapter.
