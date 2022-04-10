<a href="/JS/Operators/Main.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Operators/Assignment.md">Next &gt;</a>
<hr>
<table class="ws-table-all notranslate">
  <tr>
    <th>Operator</th>
    <th>Description</th>
  </tr>
  <tr>
    <td><code>+</code></td>
    <td>Addition.</td>
  </tr>
  <tr>
    <td><code>-</code></td>
    <td>Subtraction.</td>
  </tr>
  <tr>
    <td><code>*</code></td>
    <td>Multiplication.</td>
  </tr>
  <tr>
    <td><code>**</code></td>
    <td>Exponentation (ES2016).</td>
  </tr>
  <tr>
    <td><code>/</code></td>
    <td>Division.</td>
  </tr>
  <tr>
    <td><code>%</code></td>
    <td>Modulus (Division Remainder).</td>
  </tr>
  <tr>
    <td><code>++</code></td>
    <td>Increment.</td>
  </tr>
  <tr>
    <td><code>--</code></td>
    <td>Decrement.</td>
  </tr>
</table>
A typical arithmetic operation operates on two numbers.
<br>
The two numbers can be literals:
<pre>let x = 100 + 50;</pre>
or variables:
<pre>
var a = 100;
var b = 50;
let x = a + b;
</pre>
or expressions:
<pre>
var a = 1;
let x = (100 + 50) * a;
</pre>
<h1>Adding</h1>
The addition operator (<code>+</code>) adds numbers:
<pre>
let x = 5;
let y = 2;
let z = x + y;
</pre>
<h1>Subtracting</h1>
The subtraction operator (<code>-</code>) subtracts numbers.
<pre>
let x = 5;
let y = 2;
let z = x - y;
</pre>
<h1>Multiplying</h1>
The multiplication operator (<code>*</code>) multiplies numbers.
<pre>
let x = 5;
let y = 2;
let z = x * y;
</pre>
<h1>Dividing</h1>
The division operator (<code>/</code>) divides numbers.
<pre>
let x = 5;
let y = 2;
let z = x / y;
</pre>
<h1>Remainder</h1>
The modulus operator (<code>%</code>) returns the division remainder.
<pre>
let x = 5;
let y = 2;
let z = x % y;
</pre>
<h1>Incrementing</h1>
The increment operator (<code>++</code>) increments numbers.
<pre>
let x = 5;
x++;
let z = x;
</pre>
<h1>Decrementing</h1>
The decrement operator (<code>--</code>) decrements numbers.
<pre>
let x = 5;
x--;
let z = x;
</pre>
<h1>Exponentiation</h1>
The exponentiation operator (<code>**</code>) raises the first operand to the power of the second operand.
<pre>
let x = 5;
let z = x ** 2; // result is 25
</pre>
<code>x ** y</code> produces the same result as Math.pow(x,y):
<pre>
let x = 5;
let z = Math.pow(x,2); // result is 25
</pre>
<h1>Operator Precedence</h1>
Operator precedence describes the order in which operations are performed in an arithmetic expression.
<pre>let x = 100 + 50 * 3;</pre>
Is the result of example above the same as <code>150 * 3</code>, or is it the same as <code>100 + 150</code>?
<br>
Is the addition or the multiplication done first?
<br>
As in traditional school mathematics, the multiplication is done first.
<br>
Multiplication (<code>*</code>) and division (<code>/</code>) have higher precedence than addition (<code>+</code>) and subtraction (<code>-</code>).
<br>
And (as in school mathematics) the precedence can be changed by using parentheses:
<pre>let x = (100 + 50) * 3;</pre>
When using parentheses, the operations inside the parentheses are computed first.
<br>
When many operations have the same precedence (like addition and subtraction), they are computed from left to right:
<pre>let x = 100 + 50 - 3;</pre>
