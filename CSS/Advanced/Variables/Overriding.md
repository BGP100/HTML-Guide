From the previous page we have learned that global variables can be accessed/used through the entire document, while local variables can be used only inside the selector where it is declared.
<br>
Look at the example from the previous page:
<pre>
:root {
  --blue: #1e90ff;
  --white: #ffffff;
}
body {
  background-color: var(--blue);
}
h2 {
  border-bottom: 2px solid var(--blue);
}
.container {
  color: var(--blue);
  background-color: var(--white);
  padding: 15px;
}
button {
  background-color: var(--white);
  color: var(--blue);
  border: 1px solid var(--blue);
  padding: 5px;
}
</pre>
Sometimes we want the variables to change only in a specific section of the page.
<br>
Assume we want a different color of blue for button elements. Then, we can re-declare the --blue variable inside the button selector. When we use var(--blue) inside this selector, it will use the local --blue variable value declared here.
<br>
We see that the local --blue variable will override the global --blue variable for the button elements:
<pre>
:root {
  --blue: #1e90ff;
  --white: #ffffff;
}
body {
  background-color: var(--blue);
}
h2 {
  border-bottom: 2px solid var(--blue);
}
.container {
  color: var(--blue);
  background-color: var(--white);
  padding: 15px;
}
button {
  --blue: #0000ff; /* local variable will override global */
  background-color: var(--white);
  color: var(--blue);
  border: 1px solid var(--blue);
  padding: 5px;
}
</pre>
<h1>Add Local Variables</h1>
If a variable is to be used at only one single place, we could also have declared a new local variable, like this:
<pre>
:root {
  --blue: #1e90ff;
  --white: #ffffff;
}
body {
  background-color: var(--blue);
}
h2 {
  border-bottom: 2px solid var(--blue);
}
.container {
  color: var(--blue);
  background-color: var(--white);
  padding: 15px;
}
button {
  --button-blue: #0000ff; /* new local variable */
  background-color: var(--white);
  color: var(--button-blue);
  border: 1px solid var(--button-blue);
  padding: 5px;
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
