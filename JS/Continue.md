<a href="/JS/Break.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Labels.md">Next &gt;</a>
<hr>
The <b>continue</b> statement "jumps over" one iteration in the loop.
<hr>
The <b>continue</b> statement breaks one iteration (in the loop), if a specified condition occurs, and continues with the next iteration in the loop.
<br>
This example skips the value of 3:
<pre>
for (let i = 0; i < 10; i++) {
  if (i === 3) { continue; }
  text += "The number is " + i + "<br>";
}
</pre>
