The var() function is used to insert the value of a CSS variable.
<br>
CSS variables have access to the DOM, which means that you can create variables with local or global scope, change the variables with JavaScript, and change the variables based on media queries.
<br>
A good way to use CSS variables is when it comes to the colors of your design. Instead of copy and paste the same colors over and over again, you can place them in variables.
<h1>The Traditional Way</h1>
The following example shows the traditional way of defining some colors in a style sheet (by defining the colors to use, for each specific element):
<pre>
body {
  background-color: #1e90ff;
}
h2 {
  border-bottom: 2px solid #1e90ff;
}
.container {
  color: #1e90ff;
  background-color: #ffffff;
  padding: 15px;
}
button {
  background-color: #ffffff;
  color: #1e90ff;
  border: 1px solid #1e90ff;
  padding: 5px;
}
</pre>
<h1>Syntax</h1>
The var() function is used to insert the value of a CSS variable.
<br>
The syntax of the var() function is as follows:
<pre>var(<i>--name, value</i>)</pre>
<table class="ws-table-all notranslate">
  <tr>
    <th>Value</th>
    <th>Description</th>
  </tr>  
  <tr>
    <td><i>name</i></td>
    <td>Required. The variable name (must start with two 
    dashes)</td>
  </tr>
  <tr>
    <td><i>value</i></td>
    <td>Optional. The fallback value (used if the variable is not found)</td>
  </tr>
</table>
<b>Note:</b> The variable name must begin with two dashes (--) and it is case sensitive!
<h1>How it Works</h1>
First of all: CSS variables can have a global or local scope.
<br>
Global variables can be accessed/used through the entire document, while local variables can be used only inside the selector where it is declared.
<br>
To create a variable with global scope, declare it inside the <b>:root</b> selector. The <b>:root</b> selector matches the document's root element.
<br>
To create a variable with local scope, declare it inside the selector that is going to use it.
<br>
The following example is equal to the example above, but here we use the <b>var()</b> function.
<br>
First, we declare two global variables (--blue and --white). Then, we use the <b>var()</b> function to insert the value of the variables later in the style sheet:
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
Advantages of using var() are:
<ul>
  <li>makes the code easier to read (more understandable)</li>
  <li>makes it much easier to change the color values</li>
</ul>
To change the blue and white color to a softer blue and white, you just need to change the two variable values:
<pre>
:root {
  --blue: #6495ed;
  --white: #faf0e6;
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
<h1>Browser Support</h1>
The numbers in the table specify the first browser version that fully supports the var() function.
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
