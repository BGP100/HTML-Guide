Now we want to change a variable value inside a media query.
<br>
Here, we first declare a new local variable named --fontsize for the .container class. We set its value to 25 pixels. Then we use it in the .container class further down. Then, we create a @media rule that says "When the browser's width is 450px or wider, change the --fontsize variable value of the .container class to 50px."
<br>
Here is the complete example:
<pre>
/* Variable declarations */
:root {
  --blue: #1e90ff;
  --white: #ffffff;
}
.container {
  --fontsize: 25px;
}
/* Styles */
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
  font-size: var(--fontsize);
}
@media screen and (min-width: 450px) {
  .container {
    --fontsize: 50px;
  }
}
</pre>
Here is another example where we also change the value of the --blue variable in the @media rule:
<pre>
/* Variable declarations */
:root {
  --blue: #1e90ff;
  --white: #ffffff;
}
.container {
  --fontsize: 25px;
}
/* Styles */
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
  font-size: var(--fontsize);
}
@media screen and (min-width: 450px) {
  .container {
    --fontsize: 50px;
  }
   :root {
    --blue: lightblue;
  }
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
