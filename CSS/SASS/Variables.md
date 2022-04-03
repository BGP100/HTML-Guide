Variables are a way to store information that you can re-use later.
<br>
With Sass, you can store information in variables, like:
</ul>
  <li><b>strings</b></li>
  <li><b>numbers</b></li>
  <li><b>colors</b></li>
  <li><b>booleans</b></li>
  <li><b>lists</b></li>
  <li><b>nulls</b></li>
</ul>
Sass uses the <code>$</code> symbol, followed by a name, to declare variables:
<pre>$<i>variablename</i>: <i>value</i>;</pre>
The following example declares 4 variables named myFont, myColor, myFontSize, and myWidth. After the variables are declared, you can use the variables wherever you want:
<pre>
$myFont: Helvetica, sans-serif;
$myColor: red;
$myFontSize: 18px;
$myWidth: 680px;
body {
  font-family: $myFont;
  font-size: $myFontSize;
  color: $myColor;
}
#container {
  width: $myWidth;
}
</pre>
So, when the Sass file is transpiled, it takes the variables (myFont, myColor, etc.) and outputs normal CSS with the variable values placed in the CSS, like this:
<pre>
body {
  font-family: Helvetica, sans-serif;
  font-size: 18px;
  color: red;
}
#container {
  width: 680px;
}
</pre>
<h1>Variable Scope</h1>
Sass variables are only available at the level of nesting where they are defined.
<br>
Look at the following example:
<pre>
$myColor: red;
h1 {
  $myColor: green;
  color: $myColor;
}
p {
  color: $myColor;
}
</pre>
Will the color of the text inside a <b>&lt;p&gt;</b> tag be red or green? It will be red!
<br>
The other definition, $myColor: green; is inside the <b>&lt;h1&gt;</b> rule, and will only be available there!
<br>
So, the CSS output will be:
<pre>
h1 {
  color: green;
}
p {
  color: red;
}
</pre>
<h1>!global</h1>
The default behavior for variable scope can be overridden by using the <b>!global</b> switch.
<br>
<b>!global</b> indicates that a variable is global, which means that it is accessible on all levels.
<br>
Look at the following example (same as above; but with <b>!global</b> added):
<pre>
$myColor: red;
h1 {
  $myColor: green !global;
  color: $myColor;
}
p {
  color: $myColor;
}
</pre>
Now the color of the text inside a <b>&lt;p&gt;</b> tag will be green!
<br>
So, the CSS output will be:
<pre>
h1 {
  color: green;
}
p {
  color: green;
}
</pre>
