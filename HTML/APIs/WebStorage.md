HTML web storage; better than cookies.
<hr>
With web storage, web applications can store data locally within the user's browser.
<br>
Before HTML5, application data had to be stored in cookies, included in every server request. Web storage is more secure, and large amounts of data can be stored locally, without affecting website performance.
<br>
Unlike cookies, the storage limit is far larger (at least 5MB) and information is never transferred to the server.
<br>
Web storage is per origin (per domain and protocol). All pages, from one origin, can store and access the same data.
<h1>Browser Support</h1>
The numbers in the table specify the first browser version that fully supports Web Storage.
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
    <td>8.0</td>
    <td>3.5</td>
    <td>4.0</td>
    <td>11.5</td>
  </tr>
</table>
<h1>Web Storage Objects</h1>
HTML web storage provides two objects for storing data on the client:
<ul>
  <li>window.localStorage - stores data with no expiration date.</li>
  <li>window.sessionStorage - stores data for one session (data is lost when the browser tab is closed).</li>
</ul>
Before using web storage, check browser support for localStorage and sessionStorage:
<pre>
if (typeof(Storage) !== "undefined") {
  // Code for localStorage/sessionStorage.
} else {
  // Sorry! No Web Storage support..
}
<pre>
<h1>localStorage Object</h1>
The localStorage object stores the data with no expiration date. The data will not be deleted when the browser is closed, and will be available the next day, week, or year.
<pre>
// Store
localStorage.setItem("lastname", "Smith");
// Retrieve
document.getElementById("result").innerHTML = localStorage.getItem("lastname");
</pre>
Example explained:
<ul>
  <li>Create a localStorage name/value pair with name="lastname" and value="Smith"</li>
  <li>Retrieve the value of "lastname" and insert it into the element with id="result"</li>
</ul>
The example above could also be written like this:
<pre>
// Store
localStorage.lastname = "Smith";
// Retrieve
document.getElementById("result").innerHTML = localStorage.lastname;
</pre>
The syntax for removing the "lastname" localStorage item is as follows:
<pre>localStorage.removeItem("lastname");</pre>
<b>Note:</b> Name/value pairs are always stored as strings. Remember to convert them to another format when needed!
<br>
The following example counts the number of times a user has clicked a button. In this code the value string is converted to a number to be able to increase the counter:
<pre>
if (localStorage.clickcount) {
  localStorage.clickcount = Number(localStorage.clickcount) + 1;
} else {
  localStorage.clickcount = 1;
}
document.getElementById("result").innerHTML = "You have clicked the button " +
localStorage.clickcount + " time(s).";
</pre>
<h1>sessionStorage Object</h1>
The sessionStorage object is equal to the localStorage object, except that it stores the data for only one session. The data is deleted when the user closes the specific browser tab.
<br>
The following example counts the number of times a user has clicked a button, in the current session:
<pre>
if (sessionStorage.clickcount) {
  sessionStorage.clickcount = Number(sessionStorage.clickcount) + 1;
} else {
  sessionStorage.clickcount = 1;
}
document.getElementById("result").innerHTML = "You have clicked the button " +
sessionStorage.clickcount + " time(s) in this session.";
</pre>
