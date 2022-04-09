A JavaScript Boolean represents one of two values: <b>true</b> or <b>false</b>.
<br>
Very often, in programming, you will need a data type that can only have one of two values, like
<ul>
  <li>YES / NO</li>
  <li>ON / OFF</li>
  <li>TRUE / FALSE</li>
</ul>
For this, JavaScript has a Boolean data type. It can only take the values <b>true</b> or <b>false</b>.
<h1>Boolean()</h1>
You can use the Boolean() function to find out if an expression (or a variable) is true:
<pre>Boolean(10 &gt; 9)</pre>
Or even easier:
<pre>10 &gt; 9</pre>
<h1>Everything With a "Value" is True</h1>
<pre>100</pre>
<pre>3.14</pre>
<pre>-15</pre>
<pre>"Hello"</pre>
<pre>"false"</pre>
<pre>7 + 1 + 3.14</pre>
<h1>Everything Without a "Value" is False</h1>
The Boolean value of 0 (zero) is false:
<pre>
let x = 0;
Boolean(x);
</pre>
The Boolean value of -0 (minus zero) is false:
<pre>
let x = -0;
Boolean(x);
</pre>
The Boolean value of "" (empty string) is false:
<pre>
let x = "";
Boolean(x);
</pre>
The Boolean value of undefined is false:
<pre>
let x;
Boolean(x);
</pre>
The Boolean value of null is false:
<pre>
let x = null;
Boolean(x);
</pre>
The Boolean value of false is (you guessed it) false:
<pre>
let x = false;
Boolean(x);
</pre>
The Boolean value of NaN is false:
<pre>
let x = 10 / "Hallo";
Boolean(x);
</pre>
<h1>Booleans as Objects</h1>
Normally JavaScript booleans are primitive values created from literals:
<pre>let x = false;</pre>
But booleans can also be defined as objects with the keyword <b>new</b>:
<pre>let y = new Boolean(false);</pre>
<pre>
let x = false;
let y = new Boolean(false);
// typeof x returns boolean
// typeof y returns object
</pre>
When using the <code>==</code> operator, x and y are equal:
<pre>
let x = false;
let y = new Boolean(false);
</pre>
When using the <code>===</code> operator, x and y are not equal:
<pre>
let x = false;
let y = new Boolean(false);
</pre>
