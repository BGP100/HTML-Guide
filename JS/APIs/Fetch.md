<a href="/JS/APIs/WebWorkers.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/APIs/Geolocation.md">Next &gt;</a>
<hr>
The Fetch API interface allows web browser to make HTTP requests to web servers.
<br>
😃 No need for XMLHttpRequest anymore.
<h1>Browser Support</h1>
The numbers in the table specify the first browser versions that fully support Fetch API:
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
    <td>42.0</td>
    <td>14.0</td>
    <td>40.0</td>
    <td>10.1</td>
    <td>29.0</td>
  </tr>
</table>
<h1>Examples</h1>
The example below fetches a file and displays the content:
<pre>
fetch(file)
.then(x => x.text())
.then(y => myDisplay(y));
</pre>
Since Fetch is based on async and await, the example above might be easier to understand like this:
<pre>
async function getText(file) {
  let x = await fetch(file);
  let y = await x.text();
  myDisplay(y);
}
</pre>
Or even bettter: Use understandable names instead of x and y:
<pre>
async function getText(file) {
  let myObject = await fetch(file);
  let myText = await myObject.text();
  myDisplay(myText);
}
</pre>
