<a href="/JS/Async/Promises.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/APIs/Introduction.md">Next &gt;</a>
<hr>
<b>async</b> makes a function return a Promise.
<br>
<b>await</b> makes a function wait for a Promise.
<h1>Syntax</h1>
<h2>Async</h2>
The keyword <b>async</b> before a function makes the function return a promise:
<pre>
async function myFunction() {
  return "Hello";
}
</pre>
<pre>
function myFunction() {
  return Promise.resolve("Hello");
}
</pre>
Here is how to use the Promise:
<pre>
myFunction().then(
  function(value) { /* code if successful */ },
  function(error) { /* code if some error */ }
);
</pre>
Examples:
<pre>
async function myFunction() {
  return "Hello";
}
myFunction().then(
  function(value) {myDisplayer(value);},
  function(error) {myDisplayer(error);}
);
</pre>
Or simpler, since you expect a normal value (a normal response, not an error):
<pre>
async function myFunction() {
  return "Hello";
}
myFunction().then(
  function(value) {myDisplayer(value);}
);
</pre>
<h2>Await</h2>
The keyword <b>await</b> before a function makes the function wait for a promise:
<pre>let value = await promise;</pre>
The <b>await</b> keyword can only be used inside an async function.
<h1>Examples</h1>
Let's go slowly and learn how to use it.
<pre>
async function myDisplay() {
  let myPromise = new Promise(function(resolve, reject) {
    resolve("I love You !!");
  });
  document.getElementById("demo").innerHTML = await myPromise;
}
myDisplay();
</pre>
The two arguments (resolve and reject) are pre-defined by JavaScript.
<br>
We will not create them, but call one of them when the executor function is ready.
<br>
Very often we will not need a reject function.
<pre>
async function myDisplay() {
  let myPromise = new Promise(function(resolve) {
    resolve("I love You !!");
  });
  document.getElementById("demo").innerHTML = await myPromise;
}
myDisplay();
</pre>
<pre>
async function myDisplay() {
  let myPromise = new Promise(function(resolve) {
    setTimeout(function() {resolve("I love You !!");}, 3000);
  });
  document.getElementById("demo").innerHTML = await myPromise;
}
myDisplay();
</pre>
<pre>
async function getFile() {
  let myPromise = new Promise(function(resolve) {
    let req = new XMLHttpRequest();
    req.open('GET', "mycar.html");
    req.onload = function() {
      if (req.status == 200) {
        resolve(req.response);
      } else {
        resolve("File not Found");
      }
    };
    req.send();
  });
  document.getElementById("demo").innerHTML = await myPromise;
}
getFile();
</pre>
<h1>Browser Support</h1>
ECMAScript 2017 introduced the JavaScript keywords <b>async</b> and <b>await</b>.
<br>
The following table defines the first browser version with full support for both:
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
    <td>55.0</td>
    <td>15.0</td>
    <td>52.0</td>
    <td>11.0</td>
    <td>42.0</td>
  </tr>
</table>
