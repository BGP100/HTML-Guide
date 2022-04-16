<a href="/JS/Mistakes.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Reserved-Words.md">Next &gt;</a>
<hr>
How to speed up your JavaScript code.
<h1>Reduce Activity in Loops</h1>
Loops are often used in programming.
<br>
Each statement in a loop, including the for statement, is executed for each iteration of the loop.
<br>
Statements or assignments that can be placed outside the loop will make the loop run faster.
<br>
Bad:
<pre>for (let i = 0; i &lt; arr.length; i++) {</pre>
Better Code:
<pre>let l = arr.length;<br>for (let i = 0; i < l; i++) {</pre>
The bad code accesses the length property of an array each time the loop is iterated.
<br>
The better code accesses the length property outside the loop and makes the loop run faster.
<h1>Reduce DOM Access</h1>
Accessing the HTML DOM is very slow, compared to other JavaScript statements.
<br>
If you expect to access a DOM element several times, access it once, and use it as a local variable:
<pre>
const obj = document.getElementById("demo");
obj.innerHTML = "Hello";
</pre>
<h1>Reduce DOM Size</h1>
Keep the number of elements in the HTML DOM small.
<br>
This will always improve page loading, and speed up rendering (page display), especially on smaller devices.
<br>
Every attempt to search the DOM (like getElementsByTagName) will benefit from a smaller DOM.
<h1>Avoid Unnecessary Variables</h1>
Don't create new variables if you don't plan to save values.
<br>
Often you can replace code like this:
<pre>
let fullName = firstName + " " + lastName;
document.getElementById("demo").innerHTML = fullName;
</pre>
With this:
<pre>document.getElementById("demo").innerHTML=firstName+" "+lastName;</pre>
<h1>Delay JavaScript Loading</h1>
Putting your scripts at the bottom of the page body lets the browser load the page first.
<br>
While a script is downloading, the browser will not start any other downloads. In addition all parsing and rendering activity might be blocked.
<br>
<b>Note:</b> The HTTP specification defines that browsers should not download more than two components in parallel.
<br>
An alternative is to use <b>defer="true"</b> in the script tag. The defer attribute specifies that the script should be executed after the page has finished parsing, but it only works for external scripts.
<br>
If possible, you can add your script to the page by code, after the page has loaded:
<pre>
&lt;script&gt;
window.onload = function() {
  const element = document.createElement("script");
  element.src = "myScript.js";
  document.body.appendChild(element);
};
&lt;/script&gt;
</pre>
<h1>Avoid Using with</h1>
Avoid using the <b>with</b> keyword. It has a negative effect on speed. It also clutters up JavaScript scopes.
<br>
The <b>with</b> keyword is not allowed in strict mode.
