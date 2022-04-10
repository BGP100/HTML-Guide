<a href="/CSS/Advanced/Fonts.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/Advanced/3D-Transforms.md">Next &gt;</a>
<hr>
CSS transforms allow you to move, rotate, scale, and skew elements.
<br>
Mouse over the element below to see a 2D transformation:
<br>
<img src="https://i.imgur.com/OXizM9q.gif" width="20%">
<h1>Browser Support</h1>
The numbers in the table specify the first browser version that fully supports the property.
<table class="ws-table-all notranslate">
  <tr>
    <th>Browser</th>
    <th>Chrome</th>
    <th>Edge</th>
    <th>Firefox</th>
    <th>Safari</th>
    <th>Opera</th>
  </tr>
  <tr>
    <td>Version</td>
    <td>36.0</td>
    <td>10.0</td>
    <td>16.0</td>
    <td>9.0</td>
    <td>23.0</td>
  </tr>
</table>
<h1>All Methods</h1>
With the CSS transform property you can use the following 2D transformation methods:
<ul>
  <li><a href="#translate">translate()</a></li>
  <li><a href="#rotate">rotate()</a></li>
  <li><a href="#scaleX">scaleX()</a></li>
  <li><a href="#scaleY">scaleY()</a></li>
  <li><a href="#scale">scale()</a></li>
  <li><a href="#skewX">skewX()</a></li>
  <li><a href="#skewY">skewY()</a></li>
  <li><a href="#skew">skew()</a></li>
  <li><a href="#matrix">matrix()</a></li>
</ul>
<h1>translate()</h1>
<img src="https://i.imgur.com/vFgkTxZ.jpg">
<br>
The <b>translate()</b> method moves an element from its current position (according to the parameters given for the X-axis and the Y-axis).
<br>
The following example moves the <b>&lt;div&gt;</b> element 50 pixels to the right, and 100 pixels down from its current position:
<pre>
div {
  transform: translate(50px, 100px);
}
</pre>
<h1>rotate()</h1>
<img src="https://i.imgur.com/ivZxqEX.jpg">
<br>
The <b>rotate()</b> method rotates an element clockwise or counter-clockwise according to a given degree.
<br>
The following example rotates the <b>&lt;div&gt;</b> element clockwise with 20 degrees:
<pre>
div {
  transform: rotate(20deg);
}
</pre>
Using negative values will rotate the element counter-clockwise.
<br>
The following example rotates the <b>&lt;div&gt;</b> element counter-clockwise with 20 degrees:
<pre>
div {
  transform: rotate(-20deg);
}
</pre>
<h1>scale()</h1>
<img src="https://i.imgur.com/Mypsdgx.jpg">
<br>
The <b>scale()</b> method increases or decreases the size of an element (according to the parameters given for the width and height).
<br>
The following example increases the <b>&lt;div&gt;</b> element to be two times of its original width, and three times of its original height:
<pre>
div {
  transform: scale(2, 3);
}
</pre>
The following example decreases the <b>&lt;div&gt;</b> element to be half of its original width and height:
<pre>
div {
  transform: scale(0.5, 0.5);
}
</pre>
<h1>scaleX</h1>
The <b>scaleX()</b> method increases or decreases the width of an element.
<br>
The following example increases the <b>&lt;div&gt;</b> element to be two times of its original width:
<pre>
div {
  transform: scaleX(2);
}
</pre>
The following example decreases the <b>&lt;div&gt;</b> element to be half of its original width:
<pre>
div {
  transform: scaleX(0.5);
}
</pre>
<h1>scaleY()</h1>
The <b>scaleY()</b> method increases or decreases the height of an element.
<br>
The following example increases the <b>&lt;div&gt;</b> element to be three times of its original height:
<pre>
div {
  transform: scaleY(3);
}
</pre>
The following example decreases the <b>&lt;div&gt;</b> element to be half of its original height:
<pre>
div {
  transform: scaleY(0.5);
}
</pre>
<h1>skew()</h1>
The <b>skew()</b> method skews an element along the X and Y-axis by the given angles.
<br>
The following example skews the <b>&lt;div&gt;</b> element 20 degrees along the X-axis, and 10 degrees along the Y-axis:
<pre>
div {
  transform: skew(20deg, 10deg);
}
</pre>
If the second parameter is not specified, it has a zero value. So, the following example skews the <b>&lt;div&gt;</b> element 20 degrees along the X-axis:
<pre>
div {
  transform: skew(20deg);
}
</pre>
<h1>skewX()</h1>
The <b>skewX()</b> method skews an element along the X-axis by the given angle.
<br>
The following example skews the <b>&lt;div&gt;</b> element 20 degrees along the X-axis:
<pre>
div {
  transform: skewX(20deg);
}
</pre>
<h1>skewY()</h1>
The <b>skewY()</b> method skews an element along the Y-axis by the given angle.
<br>
The following example skews the <b>&lt;div&gt;</b> element 20 degrees along the Y-axis:
<pre>
div {
  transform: skewY(20deg);
}
</pre>
<h1>matrix()</h1>
The <b>matrix()</b> method combines all the 2D transform methods into one.
<br>
The <b>matrix()</b> method take six parameters, containing mathematic functions, which allows you to rotate, scale, move (translate), and skew elements.
<br>
The parameters are as follow: matrix(scaleX(),skewY(),skewX(),scaleY(),translateX(),translateY())
<pre>
div {
  transform: matrix(1, -0.3, 0, 1, 0, 0);
}
</pre>
