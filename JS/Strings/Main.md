<a href="/JS/Events.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Strings/Methods.md">Next &gt;</a>
<hr>
A JavaScript string is zero or more characters written inside quotes.
<pre>let text = "John Doe";</pre>
You can use single or double quotes:
<pre>
let carName1 = "Volvo XC60";  // Double quotes
let carName2 = 'Volvo XC60';  // Single quotes
</pre>
You can use quotes inside a string, as long as they don't match the quotes surrounding the string:
<pre>
let answer1 = "It's alright";
let answer2 = "He is called 'Johnny'";
let answer3 = 'He is called "Johnny"';
</pre>
<h1>Length</h1>
To find the length of a string, use the built-in <b>length</b> property:
<pre>
let text = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
let length = text.length;
</pre>
<h1>Escape Character</h1>
Because strings must be written within quotes, JavaScript will misunderstand this string:
<pre>let text = "We are the so-called "Vikings" from the north.";</pre>
The string will be chopped to "We are the so-called ".
<br>
The solution to avoid this problem, is to use the backslash escape character.
<br>
The backslash (<code>\</code>) escape character turns special characters into string characters:
<br>
<table class="ws-table-all notranslate">
  <tr>
    <th>Code</th>
    <th>Result</th>
    <th>Description</th>
  </tr>
  <tr>
    <td><code>/'</code></td>
    <td><code>'</code></td>
    <td>Single Quote</td>
  </tr>
  <tr>
    <td><code>/"</code></td>
    <td><code>"</code></td>
    <td>Doulbe Quote</td>
  </tr>
  <tr>
    <td><code>//</code></td>
    <td><code>/</code></td>
    <td>Backslash</td>
  </tr>
</table>
The sequence \"  inserts a double quote in a string:
<pre>let text = "We are the so-called \"Vikings\" from the north.";</pre>
The sequence \'  inserts a single quote in a string:
<pre>let text= 'It\'s alright.';</pre>
The sequence \\  inserts a backslash in a string:
<pre>let text = "The character \\ is called backslash.";</pre>
<h1>Strings as Objects</h1>
Normally, JavaScript strings are primitive values, created from literals:
<pre>let x = "John";</pre>
But strings can also be defined as objects with the keyword new:
<pre>let y = new String("John");</pre>
<pre>
let x = "John";
let y = new String("John");
</pre>
Do not create Strings objects.
<br>
The new keyword complicates the code and slows down execution speed.
<br>
String objects can produce unexpected results:
<br>
When using the <code>==</code> operator, <b>x</b> and <b>y</b> are equal:
<pre>
let x = "John";
let y = new String("John");
</pre>
When using the <code>===</code> operator, <b>x</b> and <b>y</b> are not equal:
<pre>
let x = "John";
let y = new String("John");
</pre>
<code>(x == y)</code> true or false?
<pre>
let x = new String("John");
let y = new String("John");
</pre>
<code>(x === y)</code> true or false?
<pre>
let x = new String("John");
let y = new String("John");
</pre>
