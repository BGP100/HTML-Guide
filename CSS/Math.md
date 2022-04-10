<a href="/CSS/!important.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="https://bledy-guides.repl.co">Next &gt;</a>
<hr>
The CSS math functions allow mathematical expressions to be used as property values. Here, we will explain the calc(), max() and min() functions.
<h1>calc()</h1>
The <b>calc()</b> function performs a calculation to be used as the property value.
<pre>calc(<i>expression</i>)</pre>
<i>expression</i>: Required. A mathematical expression. The result will be used as the value.
<br>
The following operators can be used: <code>+ - * /</code>
<br>
Let's look at an example:
<pre>
#div1 {
  position: absolute;
  left: 50px;
  width: calc(100% - 100px);
  border: 1px solid black;
  background-color: yellow;
  padding: 5px;
}
</pre>
Use <b>calc()</b> to calculate the width of a <b>&lt;div&gt;</b> element.
<h1>max()</h1>
The <b>max()</b> function uses the largest value, from a comma-separated list of values, as the property value.
<pre>max(<i>value1, value2, ...</i>)</pre>
<i>value1, value2, ...</i>: Required. A list of comma-separated values - where the largest value is chosen
<br>
Let's look at an example:
<pre>
#div1 {
  background-color: yellow;
  height: 100px;
  width: max(50%, 300px);
}
</pre>
Use <b>max()</b> to set the width of <b>#div1</b> to whichever value is largest, 50% or 300px.
<h1>min()</h1>
The <b>min()</b> function uses the smallest value, from a comma-separated list of values, as the property value.
<pre>min(<i>value1, value2, ...</i>)</pre>
<i>value1, value2, ...</i>: Required. A list of comma-separated values - where the smallest value is chosen
<br>
Let's look at an example:
<pre>
#div1 {
  background-color: yellow;
  height: 100px;
  width: min(50%, 300px);
}
</pre>
Use <b>min()</b> to set the width of <b>#div1</b> to whichever value is smallest, 50% or 300px.
