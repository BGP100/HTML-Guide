<a href="/JS/jQuery/Effects/Callback.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/jQuery/Traversing/Main.md">Next &gt;</a>
<hr>
With jQuery, you can chain together actions/methods.
<br>
Chaining allows us to run multiple jQuery methods (on the same element) within a single statement.
<h1>Method Chaining</h1>
Until now we have been writing jQuery statements one at a time (one after the other).
<br>
However, there is a technique called chaining, that allows us to run multiple jQuery commands, one after the other, on the same element(s).
<br>
<b>Tip:</b> This way, browsers do not have to find the same element(s) more than once.
<br>
To chain an action, you simply append the action to the previous action.
<br>
The following example chains together the <b>css()</b>, <b>slideUp()</b>, and <b>slideDown()</b> methods. The "p1" element first changes to red, then it slides up, and then it slides down:
<pre>$("#p1").css("color","red").slideUp(2000).slideDown(2000);</pre>
I could also have added more method calls if needed.
<br>
<b>Tip:</b> When chaining, the line of code could become quite long. However, jQuery is not very strict on the syntax; you can format it like you want, including line breaks and indentations.
<br>
This also works just fine:
<pre>$("#p1").css("color","red")
  .slideUp(2000)
  .slideDown(2000);
</pre>
jQuery throws away extra whitespace and executes the lines above as one long line of code (just like every other programming language we've learned before).
