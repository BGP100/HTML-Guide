<a href="/JS/Continue.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Iterables.md">Next &gt;</a>
<hr>
To label JavaScript statements you precede the statements with a label name and a colon:
<pre>
label:
statements
</pre>
The break and the continue statements are the only JavaScript statements that can "jump out of" a code block.
<br>
<b>Syntax:</b>
<pre>
break labelname;
continue labelname;
</pre>
The continue statement (with or without a label reference) can only be used to skip one loop iteration.
<br>
The break statement, without a label reference, can only be used to jump out of a loop or a switch.
<br>
With a label reference, the break statement can be used to jump out of any code block:
<pre>
const cars = ["BMW", "Volvo", "Saab", "Ford"];
list: {
  text += cars[0] + "&lt;br&gt;";
  text += cars[1] + "&lt;br&gt;";
  break list;
  text += cars[2] + "&lt;br&gt;";
  text += cars[3] + "&lt;br&gt;";
}
</pre>
