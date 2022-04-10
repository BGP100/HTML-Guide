<a href="/CSS/Text/Spacing.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/Fonts/Family.md">Next &gt;</a>
<hr>
The <b>text-shadow</b> property adds shadow to text.
<br>
In its simplest use, you only specify the horizontal shadow (2px) and the vertical shadow (2px):
<br>
<img src="https://i.imgur.com/Llk3XwQ.png">
<pre>
exampleA {
  text-shadow: 2px 2px;
  background-color: lightblue;
}
</pre>
Next, add a color red to the shadow:
<br>
<img src="https://i.imgur.com/zi3SFYX.png">
<pre>
exampleB {
  text-shadow: 2px 2px red;
}
</pre>
Then, add a blur effect 5px to the shadow:
<br>
<img src="https://i.imgur.com/PfDEwX6.png">
<pre>
exampleC {
  text-shadow: 2px 2px 5px red;
}
</pre>
<h1>Some More Examples</h1>
<h2>Example 1</h2>
Black shadow on white text:
<pre>
example1 {
  color: white;
  text-shadow: 2px 2px 4px #000000;
}
</pre>
<h2>Example 2</h2>
Neon glow:
<pre>
example2 {
  text-shadow: 0 0 3px #ff0000;
}
</pre>
<h2>Example 3</h2>
Red and blue glow
<pre>
example3 {
  text-shadow: 0 0 3px #ff0000, 0 0 5px #0000ff;
}
</pre>
<h2>Example 4</h2>
Blue glow on white text:
<pre>
example4 {
  color: white;
  text-shadow: 1px 1px 2px black, 0 0 25px blue, 0 0 5px darkblue;
}
</pre>
