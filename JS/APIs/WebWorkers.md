<a href="/JS/APIs/WebStorage.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/APIs/Fetch.md">Next &gt;</a>
<hr>
When executing scripts in an HTML page, the page becomes unresponsive until the script is finished.
<br>
A web worker is a JavaScript that runs in the background, independently of other scripts, without affecting the performance of the page. You can continue to do whatever you want: clicking, selecting things, etc., while the web worker runs in the background.
<h1>Browser Support</h1>
The numbers in the table specify the first browser version that fully support Web Workers.
<table class="ws-table-all notranslate">
  <tr>
    <th>Browser</th>
    <td>Chrome</td>
    <td>Edge</td>
    <td>Firefox</td>
    <td>Safari</td>
    <td>Opera</td>
  </tr>
  <tr>
    <th>Version</th>
    <td>4.0</td>
    <td>10.0</td>
    <td>3.5</td>
    <td>4.0</td>
    <td>11.5</td>
  </tr>
</table>
<h1>Check the WW Support</h1>
Before creating a web worker, check whether the user's browser supports it:
<pre>
if (typeof(Worker) !== "undefined") {
  // Yes! Web worker support!
  // Some code.....
} else {
  // Sorry! No Web Worker support..
};
</pre>
<h1>Create WW File</h1>
Now, let's create our web worker in an external JavaScript.
<br>
Here, we create a script that counts. The script is stored in the "demo_workers.js" file:
<pre>
var i = 0;
function timedCount() {
  i = i + 1;
  postMessage(i);
  setTimeout("timedCount()",500);
}
timedCount();
</pre>
The important part of the code above is the <b>postMessage()</b> method - which is used to post a message back to the HTML page.
<br>
<b>Note:</b> Normally web workers are not used for such simple scripts, but for more CPU intensive tasks.
<h1>Create an WW Object</h1>
Now that we have the web worker file, we need to call it from an HTML page.
<br>
The following lines checks if the worker already exists, if not - it creates a new web worker object and runs the code in "demo_workers.js":
<pre>
if (typeof(w) == "undefined") {
  w = new Worker("demo_workers.js");
}
</pre>
Then we can send and receive messages from the web worker.
<br>
Add an "onmessage" event listener to the web worker.
<pre>
w.onmessage = function(event){
  document.getElementById("result").innerHTML = event.data;
};
</pre>
When the web worker posts a message, the code within the event listener is executed. The data from the web worker is stored in event.data.
<h1>Terminate a WW</h1>
When a web worker object is created, it will continue to listen for messages (even after the external script is finished) until it is terminated.
<br>
To terminate a web worker, and free browser/computer resources, use the <b>terminate()</b> method:
<pre>w.terminate();</pre>
<h1>Reuse a WW</h1>
If you set the worker variable to undefined, after it has been terminated, you can reuse the code:
<h1>Full WW Example</h1>
<b>JS:</b>
<pre>
var w;
function startWorker() {
  if (typeof(Worker) !== "undefined") {
    if (typeof(w) == "undefined") {
      w = new Worker("demo_workers.js");
    }
    w.onmessage = function(event) {
      document.getElementById("result").innerHTML = event.data;
    };
  } else {
    document.getElementById("result").innerHTML = "Sorry! No Web Worker support.";
  }
}
function stopWorker() { 
  w.terminate();
  w = undefined;
}
</pre>
<b>HTML:</b>
<pre>
Count numbers: &lt;output id="result"&gt;&lt;/output&gt;
&lt;button onclick="startWorker()"&gt;Start Worker&lt;/button&gt;
&lt;button onclick="stopWorker()"&gt;Stop Worker&lt;/button&gt;
</pre>
<h1>WW and DOM</h1>
Since web workers are in external files, they do not have access to the following JavaScript objects:
<ul>
  <li>The window object.</li>
  <li>The document object.</li>
  <li>The parent object.</li>
</ul>
