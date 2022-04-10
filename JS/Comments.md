<a href="/JS/Syntax.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Variables.md">Next &gt;</a>
<hr>
JavaScript comments can be used to explain JavaScript code, and to make it more readable.
<br>
JavaScript comments can also be used to prevent execution, when testing alternative code.
<h1>Single Line Comments</h1>
Single line comments start with <code>//</code>.
<br>
Any text between <code>//</code> and the end of the line will be ignored by JavaScript (will not be executed).
<br>
This example uses a single-line comment before each code line:
<pre>
// Change heading:
document.getElementById("myH").innerHTML = "My First Page";
// Change paragraph:
document.getElementById("myP").innerHTML = "My first paragraph.";
</pre>
This example uses a single line comment at the end of each line to explain the code:
<pre>
let x = 5; // Declare x, give it the value of 5
let y = x + 2; // Declare y, give it the value of x + 2
</pre>
<h1>Multiple Line Comments</h1>
Multi-line comments start with <code>/*</code> and end with <code>*/</code>.
<br>
Any text between <code>/*</code> and <code>*/</code> will be ignored by JavaScript.
<br>
This example uses a multi-line comment (a comment block) to explain the code:
<pre>
/*
The code below will change
the heading with id = "myH"
and the paragraph with id = "myP"
in my web page:
*/
document.getElementById("myH").innerHTML = "My First Page";
document.getElementById("myP").innerHTML = "My first paragraph.";
</pre>
<h1>Using Comments to Prevent Executing</h1>
Using comments to prevent execution of code is suitable for code testing.
<br>
Adding <code>//</code> in front of a code line changes the code lines from an executable line to a comment.
<br>
This example uses <code>//</code> to prevent execution of one of the code lines:
<pre>
//document.getElementById("myH").innerHTML = "My First Page";
document.getElementById("myP").innerHTML = "My first paragraph.";
</pre>
This example uses a comment block to prevent execution of multiple lines:
<pre>
/*
document.getElementById("myH").innerHTML = "My First Page";
document.getElementById("myP").innerHTML = "My first paragraph.";
*/
</pre>
