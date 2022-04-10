In this chapter you will learn about the following multi-column properties:
<ul>
  <li><b>column-count</b></li>
  <li><b>column-gap</b></li>
  <li><b>column-rule-style</b></li>
  <li><b>column-rule-width</b></li>
  <li><b>column-rule-color</b></li>
  <li><b>column-rule</b></li>
  <li><b>column-span</b></li>
  <li><b>column-width</b></li>
</ul>
<h1>Browser Support</h1>
<table class="browserref notranslate">
  <tr>
    <th>Property</th>
    <th>Chrome</th>
    <th>Edge</th>
    <th>Firefox</th>
    <th>Safari</th>
    <th>Opera</th>                
  </tr>
  <tr>
    <td>column-count</td>
    <td>50.0</td>
    <td>10.0</td>
    <td>52.0</td>
    <td>9.0</td>
    <td>37.0</td>
  </tr>
  <tr>
    <td>column-gap</td>
    <td>50.0</td>
    <td>10.0</td>
    <td>52.0</td>
    <td>9.0</td>
    <td>37.0</td>
  </tr>
  <tr>
    <td>column-rule</td>
    <td>50.0</td>
    <td>10.0</td>
    <td>52.0</td>
    <td>9.0</td>
    <td>37.0</td>
  </tr>
  <tr>
    <td>column-rule-color</td>
    <td>50.0</td>
    <td>10.0</td>
    <td>52.0</td>
    <td>9.0</td>
    <td>37.0</td>
  </tr>
  <tr>
    <td>column-rule-style</td>
    <td>50.0</td>
    <td>10.0</td>
    <td>52.0</td>
    <td>9.0</td>
    <td>37.0</td>
  </tr>
  <tr>
    <td>column-rule-width</td>
    <td>50.0</td>
    <td>10.0</td>
    <td>52.0</td>
    <td>9.0</td>
    <td>37.0</td>
  </tr>
  <tr>
    <td>column-span</td>
    <td>50.0</td>
    <td>10.0</td>
    <td>71.0</td>
    <td>9.0</td>
    <td>37.0</td>
  </tr>
  <tr>
    <td>column-width</td>
    <td>50.0</td>
    <td>10.0</td>
    <td>52.0</td>
    <td>9.0</td>
    <td>37.0</td>
  </tr>
</table>
<h1>Creating them</h1>
The <b>column-count</b> property specifies the number of columns an element should be divided into.
<br>
The following example will divide the text in the <b>&lt;div&gt;</b> element into 3 columns:
<pre>
div {
  column-count: 3;
}
</pre>
<h1>Gap Between Columns</h1>
The <b>column-gap</b> property specifies the gap between the columns.
<br>
The following example specifies a 40 pixels gap between the columns:
<pre>
div {
  column-gap: 40px;
}
</pre>
<h1>Column Rules</h1>
The <b>column-rule-style</b> property specifies the style of the rule between columns:
<pre>
div {
  column-rule-style: solid;
}
</pre>
The <b>column-rule-width</b> property specifies the width of the rule between columns:
<pre>
div {
  column-rule-width: 1px;
}
</pre>
The <b>column-rule-color</b> property specifies the color of the rule between columns:
<pre>
div {
  column-rule-color: lightblue;
}
</pre>
The column-rule property is a shorthand property for setting all the column-rule-* properties above.
<br>
The following example sets the width, style, and color of the rule between columns:
<pre>
div {
  column-rule: 1px solid lightblue;
}
</pre>
<h1>Specify How Many Columns</h1>
The <b>column-span</b> property specifies how many columns an element should span across.
<br>
The following example specifies that the <b>&lt;h2&gt;</b> element should span across all columns:
<pre>
h2 {
  column-span: all;
}
</pre>
<h1>Width</h1>
The <b>column-width</b> property specifies a suggested, optimal width for the columns.
<br>
The following example specifies that the suggested, optimal width for the columns should be 100px:
<pre>
div {
  column-width: 100px;
}
</pre>
