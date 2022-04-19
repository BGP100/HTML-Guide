<a href="/JS/Async/Asynchronous.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Async/AsyncAndAwake.md">Next &gt;</a>
<hr>
"Producing code" is code that can take some time
<br>
"Consuming code" is code that must wait for the result
<br>
A Promise is a JavaScript object that links producing code and consuming code
<h1>Object</h1>
A JavaScript Promise object contains both the producing code and calls to the consuming code:
<br>
<b>Syntax:</b>
<pre>
let myPromise = new Promise(function(myResolve, myReject) {
// "Producing Code" (May take some time)

  myResolve(); // when successful
  myReject();  // when error
});

// "Consuming Code" (Must wait for a fulfilled Promise)
myPromise.then(
  function(value) { /* code if successful */ },
  function(error) { /* code if some error */ }
);
</pre>
<h1>Object Properties</h1>
A JavaScript Promise object can be:
<ul>
  <li>Pending</li>
  <li>Fulfilled</li>
  <li>Rejected</li>
</ul>
The Promise object supports two properties: state and result.
<br>
While a Promise object is "pending" (working), the result is undefined.
<br>
When a Promise object is "fulfilled", the result is a value.
<br>
When a Promise object is "rejected", the result is an error object.
<h1>How To</h1>
Here is how to use a Promise:
<pre>
myPromise.then(
  function(value) { /* code if successful */ },
  function(error) { /* code if some error */ }
);
</pre>
<b>Promise.then()</b> takes two arguments, a callback for success and another for failure.
<br>
Both are optional, so you can add a callback for success or failure only.
<pre>
function myDisplayer(some) {
  document.getElementById("demo").innerHTML = some;
}
let myPromise = new Promise(function(myResolve, myReject) {
  let x = 0;
// The producing code (this may take some time)
  if (x == 0) {
    myResolve("OK");
  } else {
    myReject("Error");
  }
});
myPromise.then(
  function(value) {myDisplayer(value);},
  function(error) {myDisplayer(error);}
);
</pre>
<h1>Examples</h1>
To demonstrate the use of promises, we will use the callback examples from the previous chapter:
<pre>
setTimeout(function() { myFunction("I love You !!!"); }, 3000);
function myFunction(value) {
  document.getElementById("demo").innerHTML = value;
}
</pre>
<pre>
let myPromise = new Promise(function(myResolve, myReject) {
  setTimeout(function() { myResolve("I love You !!"); }, 3000);
});
myPromise.then(function(value) {
  document.getElementById("demo").innerHTML = value;
});
</pre>
<pre>
function getFile(myCallback) {
  let req = new XMLHttpRequest();
  req.open('GET', "mycar.html");
  req.onload = function() {
    if (req.status == 200) {
      myCallback(req.responseText);
    } else {
      myCallback("Error: " + req.status);
    }
  }
  req.send();
}
getFile(myDisplayer);
</pre>
<pre>
let myPromise = new Promise(function(myResolve, myReject) {
  let req = new XMLHttpRequest();
  req.open('GET', "mycar.htm");
  req.onload = function() {
    if (req.status == 200) {
      myResolve(req.response);
    } else {
      myReject("File not Found");
    }
  };
  req.send();
});
myPromise.then(
  function(value) {myDisplayer(value);},
  function(error) {myDisplayer(error);}
);
</pre>
<h1>Browser Support</h1>
ECMAScript 2015, also known as ES6, introduced the JavaScript Promise object.
<br>
The following table defines the first browser version with full support for Promise objects:
<table class="ws-table-all notranslate">
  <tr>
    <th>Browser</th>
    <th>Chrome</th>
    <th>Edge</th>
    <th>Firefox</th>
    <th>Safari</th>
    <th>Opera</th>
  </tr>
  <tr>
    <td>Verison</td>
    <td>33.0</td>
    <td>12.0</td>
    <td>29.0</td>
    <td>7.1</td>
    <td>20.0</td>
  </tr>
</table>
