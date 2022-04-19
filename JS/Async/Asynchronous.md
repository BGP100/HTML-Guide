<a href="/JS/Async/Callback.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Async/Promises.md">Next &gt;</a>
<hr>
Functions running in parallel with other functions are called asynchronous.
<br>
A good example is JavaScript <b>setTimeout()</b>.
<hr>
The examples used in the previous chapter, was very simplified.
<br>
The purpose of the examples was to demonstrate the syntax of callback functions:
<pre>
function myDisplayer(something) {
  document.getElementById("demo").innerHTML = something;
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
<h1>Waiting for a Timeout</h1>
When using the JavaScript function setTimeout(), you can specify a callback function to be executed on time-out:
<pre>
setTimeout(myFunction, 3000);
function myFunction() {
  document.getElementById("demo").innerHTML = "I love You !!";
}
</pre>
In the example above, myFunction is used as a callback.
<br>
myFunction is passed to <b>setTimeout()</b> as an argument.
<br>
3000 is the number of milliseconds before time-out, so <b>myFunction()</b> will be called after 3 seconds.
Instead of passing the name of a function as an argument to another function, you can always pass a whole function instead:
<pre>
setTimeout(function() { myFunction("I love You !!!"); }, 3000);
function myFunction(value) {
  document.getElementById("demo").innerHTML = value;
}
</pre>
In the example above, <code>function(){ myFunction("I love You !!!"); }</code> is used as a callback. It is a complete function. The complete function is passed to setTimeout() as an argument.
<br>
3000 is the number of milliseconds before time-out, so myFunction() will be called after 3 seconds.
<h1>Waiting for Intervals</h1>
When using the JavaScript function setInterval(), you can specify a callback function to be executed for each interval:
<pre>
setInterval(myFunction, 1000);
function myFunction() {
  let d = new Date();
  document.getElementById("demo").innerHTML=
  d.getHours() + ":" +
  d.getMinutes() + ":" +
  d.getSeconds();
}
</pre>
In the example above, myFunction is used as a callback.
<br>
<b>myFunction</b> is passed to <b>setInterval()</b> as an argument.
<br>
1000 is the number of milliseconds between intervals, so myFunction() will be called every second.
<h1>Waiting for Files</h1>
If you create a function to load an external resource (like a script or a file), you cannot use the content before it is fully loaded.
<br>
This is the perfect time to use a callback.
<br>
This example loads an HTML file (mycar.html), and displays the HTML file in a web page, after the file is fully loaded:
<pre>
function myDisplayer(some) {
  document.getElementById("demo").innerHTML = some;
}
function getFile(myCallback) {
  let req = new XMLHttpRequest();
  req.open('GET', "mycar.html");
  req.onload = function() {
    if (req.status == 200) {
      myCallback(this.responseText);
    } else {
      myCallback("Error: " + req.status);
    }
  }
  req.send();
}
getFile(myDisplayer);
</pre>
In the example above, myDisplayer is used as a callback.
<br>
<b>myDisplayer</b> is passed to <b>getFile()</b> as an argument.
<br>
Below is a copy of mycar.html:
<br>
<code>mycar.html</code>:
<pre>
&lt;img src="img_car.jpg" alt="Nice car" style="width:100%;height:auto;"&gt;
&lt;p&gt;A car is a wheeled, self-powered motor vehicle used for transportation.
&lt;br&gt;
Most definitions of the term specify that cars are designed to run primarily on roads, to have seating for one to eight people, to typically have four wheels.&lt;/p&gt;
&lt;p&gt;(Wikipedia)&lt;/p&gt;
</pre>
