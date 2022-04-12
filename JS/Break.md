The <b>break</b> statement "jumps out" of a loop.
<br>
The <b>continue</b> statement "jumps over" one iteration in the loop.
<h1>Break</h1>
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
<h1>Continue</h1>
The <b>continue</b> statement breaks one iteration (in the loop), if a specified condition occurs, and continues with the next iteration in the loop.
<br>
This example skips the value of 3:
<pre>
for (let i = 0; i < 10; i++) {
  if (i === 3) { continue; }
  text += "The number is " + i + "<br>";
}
</pre>
