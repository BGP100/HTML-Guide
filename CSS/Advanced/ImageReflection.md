The <b>box-reflect</b> property is used to create an image reflection.
<br>
The value of the <b>box-reflect</b> property can be: <b>below</b>, <b>above</b>, <b>left</b>, or <b>right</b>.
<h1>Browser Support</h1>
The numbers in the table specify the first browser version that fully supports the property.
<br>
Numbers followed by -webkit- specify the first version that worked with a prefix.
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
    <td>4.0</td>
    <td>79.0</td>
    <td>Not Supported</td>
    <td>4.0</td>
    <td>15.0</td>
  </tr>
</table>
<h1>Examples</h1>
<pre>
img {
  -webkit-box-reflect: below;
}
</pre>
<pre>
img {
  -webkit-box-reflect: right;
}
</pre>
<h1>Offset</h1>
To specify the gap between the image and the reflection, add the size of the gap to the box-reflect property.
<pre>
img {
  -webkit-box-reflect: below 20px;
}
</pre>
<h1>With Gradients</h1>
We can also create a fade-out effect on the reflection.
<pre>
img {
  -webkit-box-reflect: below 0px linear-gradient(to bottom, rgba(0,0,0,0.0), rgba(0,0,0,0.4));
}
</pre>
