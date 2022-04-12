<a href="/JS/Loop/While.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Continue.md">Next &gt;</a>
<hr>
The <b>break</b> statement "jumps out" of a loop.
<hr>
You have already seen the <b>break</b> statement used in an earlier chapter of this tutorial. It was used to "jump out" of a <b>switch()</b> statement.
<br>
The <b>break</b> statement can also be used to jump out of a loop:
<pre>
for (let i = 0; i &lt; 10; i++) {
  if (i === 3) { break; }
  text += "The number is " + i + "&lt;br&gt;";
}
</pre>
In the example above, the <b>break</b> statement ends the loop ("breaks" the loop) when the loop counter (i) is 3.
