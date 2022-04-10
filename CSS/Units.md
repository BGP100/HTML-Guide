<a href="/CSS/Layout.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/Specificity.md">Next &gt;</a>
<hr>
<h1>Units</h1>
CSS has several different units for expressing a length.
<br>
Many CSS properties take "length" values, such as <b>width</b>, <b>margin</b>, <b>padding</b>, <b>font-size</b>, etc.
<br>
<b>Length</b> is a number followed by a length unit, such as <b>10px</b>, <b>2em</b>, etc.
<pre>
h1 {
  font-size: 60px;
}
p {
  font-size: 25px;
  line-height: 50px;
}
</pre>
<b>Note:</b> A whitespace cannot appear between the number and the unit. However, if the value is <b>0</b>, the unit can be omitted.
<br>
For some CSS properties, negative lengths are allowed.
<br>
There are two types of length units: <b>absolute</b> and <b>relative</b>.
<h2>Absolute</h2>
The absolute length units are fixed and a length expressed in any of these will appear as exactly that size.
<br>
Absolute length units are not recommended for use on screen, because screen sizes vary so much. However, they can be used if the output medium is known, such as for print layout.
<table class="ws-table-all notranslate">
  <tr>
    <th>Unit</th>
    <th>Meaning</th>
  </tr>
  <tr>
    <td>cm</td>
    <td>centimeters</td>
  </tr>
  <tr>
    <td>mm</td>
    <td>millimeters</td>
  </tr>
  <tr>
    <td>in</td>
    <td>inches (1in = 96px = 2.54cm)</td>
  </tr>
  <tr>
    <td>px <code>*</code></td>
    <td>pixels (1px = 1/96th of 1in)</td>
  </tr>
  <tr>
    <td>pt</td>
    <td>points (1pt = 1/72nd of 1in)</td>
  </tr>
  <tr>
    <td>pc</td>
    <td>picas (1pc = 12pt)</td>
  </tr>
</table>
<code>*</code> Pixels (px) are relative to the viewing device. For low-dpi devices, 1px is one device pixel (dot) of the display. For printers and high resolution screens 1px implies multiple device pixels.
<h2>Relative</h2>
Relative length units specify a length relative to another length property. Relative length units scales better between different rendering mediums.
<table class="ws-table-all notranslate">
  <tr>
    <th>Unit</th>
    <th>Meaning</th>
  </tr>
  <tr>
    <td>em</td>
    <td>Relative to the font-size of the element (2em means 2 times the size of the current font)</td>
  </tr>
  <tr>
    <td>ex</td>
    <td>Relative to the x-height of the current font (rarely used)</td>
  </tr>
  <tr>
    <td>ch</td>
    <td>Relative to width of the "0" (zero)</td>
  </tr>
  <tr>
    <td>rem</td>
    <td>Relative to font-size of the root element</td>
  </tr>
  <tr>
    <td>vw</td>
    <td>Relative to 1% of the width of the viewport <code>*</code></td>
  </tr>
  <tr>
    <td>vh</td>
    <td>Relative to 1% of the height of the viewport <code>*</code></td>
  </tr>
  <tr>
    <td>vmin</td>
    <td>Relative to 1% of viewport's <code>*</code> smaller dimension</td>
  </tr>
  <tr>
    <td>vmax</td>
    <td>Relative to 1% of viewport's <code>*</code> larger dimension</td>
  </tr>
  <tr>
    <td>%</td>
    <td>Percentage of the screen/element is on.</td>
  </tr>
</table>
<code>*</code> Viewport = the browser window size. If the viewport is 50cm wide, 1vw = 0.5cm.
<h1>Browser Support</h1>
The numbers in the table specify the first browser version that fully supports the length unit.
<table class="ws-table-all notranslate">
  <tr>
    <th>Unit</th>
    <th>Chrome</th>
    <th>Edge</th>
    <th>Firefox</th>
    <th>Safari</th>
    <th>Opera</th>
  </tr>
  <tr>
    <td>em, ex, %, px, cm, mm, in, pt, pc</td>
    <td>1.0</td>
    <td>3.0</td>
    <td>1.0</td>
    <td>1.0</td>
    <td>3.5</td>
  </tr>
  <tr>
    <td>ch</td>
    <td>27.0</td>
    <td>9.0</td>
    <td>1.0</td>
    <td>7.0</td>
    <td>20.0</td>
  </tr>
  <tr>
    <td>rem</td>
    <td>4.0</td>
    <td>9.0</td>
    <td>3.6</td>
    <td>4.1</td>
    <td>11.6</td>
  </tr>
  <tr>
    <td>vh, vw</td>
    <td>20.0</td>
    <td>9.0</td>
    <td>19.0</td>
    <td>6.0</td>
    <td>20.0</td>
  </tr>
  <tr>
    <td>vmin</td>
    <td>20.0</td>
    <td>12.0</td>
    <td>19.0</td>
    <td>6.0</td>
    <td>20.0</td>
  </tr>
  <tr>
    <td>vmax</td>
    <td>26.0</td>
    <td>16.0</td>
    <td>19.0</td>
    <td>6.0</td>
    <td>20.0</td>
  </tr>
</table>
