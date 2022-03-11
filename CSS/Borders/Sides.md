From the examples on the previous pages, you have seen that it is possible to specify a different border for each side.
<br>
In CSS, there are also properties for specifying each of the borders (top, right, bottom, and left):
<pre>
p {
  border-top-style: dotted;
  border-right-style: solid;
  border-bottom-style: dotted;
  border-left-style: solid;
}
</pre>
<img src="https://i.imgur.com/zz0Y1an.png">
<br>
The example above gives the same result as this:
<pre>
p {
  border-style: dotted solid;
}
</pre>
So, here is how it works:
<br>
If the <b>border-style</b> property has four values:
<br>
<b> - border-style: dotted solid double dashed;</b>
<ul>
  <li>top border is dotted</li>
  <li>right border is solid</li>
  <li>bottom border is double</li>
  <li>left border is dashed</li>
</ul>
<b> - border-style: dotted solid double;</b>
<ul>
  <li>top border is dotted</li>
  <li>right and left borders are solid</li>
  <li>bottom border is double</li>
</ul>
<b> - border-style: dotted solid</b>
<ul>
  <li>top and bottom borders are dotted</li>
  <li>right and left borders are solid</li>
</ul>
<b> - border-style: dotted;</b>
<ul>
  <li>all four borders are dotted</li>
</ul>
<pre>
/* Four values */
p {
  border-style: dotted solid double dashed;
}
/* Three values */
p {
  border-style: dotted solid double;
}
/* Two values */
p {
  border-style: dotted solid;
}
/* One value */
p {
  border-style: dotted;
}
</pre>
