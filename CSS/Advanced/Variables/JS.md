<a href="/CSS/Advanced/Variables/Overriding.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/Advanced/Variables/MediaQueries.md">Next &gt;</a>
<hr>
Here is an example of how you can create a script to display and change the --blue variable from the example used in the previous pages. For now, do not worry if you are not familiar with JavaScript:
<pre>
// Get the root element
var r = document.querySelector(':root');
// Create a function for getting a variable value
function myFunction_get() {
  // Get the styles (properties and values) for the root
  var rs = getComputedStyle(r);
  // Alert the value of the --blue variable
  alert("The value of --blue is: " + rs.getPropertyValue('--blue'));
}
// Create a function for setting a variable value
function myFunction_set() {
  // Set the value of variable --blue to another value (in this case "lightblue")
  r.style.setProperty('--blue', 'lightblue');
}
</pre>
<h1>Browser Support</h1>
The numbers in the table specify the first browser version that fully supports the <b>var()</b> function.
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
    <td>Version</td>
    <td>49.0</td>
    <td>15.0</td>
    <td>31.0</td>
    <td>9.1</td>
    <td>36.0</td>
  </tr>
</table>
<h1>Short Description</h1>
Inserts the value of a CSS variable.
