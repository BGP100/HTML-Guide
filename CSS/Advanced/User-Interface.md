In this chapter you will learn about the following CSS user interface properties:
<ul>
  <li><b>resize</b></li>
  <li><b>outline-offset</b></li>
</ul>
<h1>Browser Support</h1>
The numbers in the table specify the first browser version that fully supports the property.
<table class="ws-table-all notranslate">
  <tr>
    <th>Property</th>
    <th>Chrome</th>
    <th>Edge</th>
    <th>Firefox</th>
    <th>Safari</th>
    <th>Opera</th>
  </tr>
  <tr>
    <td>resize</td>
    <td>4.0</td>
    <td>79.0</td>
    <td>5.0</td>
    <td>4.0</td>
    <td>15.0</td>
  </tr>
  <tr>
    <td>outline-offset</td>
    <td>4.0</td>
    <td>15.0</td>
    <td>5.0</td>
    <td>4.0</td>
    <td>9.5</td>
  </tr>
</table>
<h1>resize</h1>
The resize property specifies if (and how) an element should be resizable by the user.
<br>
The following example lets the user resize only the width of a <b>&lt;div&gt;</b> element:
<pre>
div {
  resize: horizontal;
  overflow: auto;
}
</pre>
The following example lets the user resize only the height of a <b>&lt;div&gt;</b> element:
<pre>
div {
  resize: vertical;
  overflow: auto;
}
</pre>
The following example lets the user resize both the height and width of a <b>&lt;div&gt;</b> element:
<pre>
div {
  resize: both;
  overflow: auto;
}
</pre>
In many browsers, <b>&lt;textarea&gt;</b> is resizable by default. Here, we have used the resize property to disable the resizability:
<pre>
textarea {
  resize: none;
}
</pre>
<h1>outline-offset</h1>
The <b>outline-offset</b> property adds space between an outline and the edge or border of an element.
<br>
<b>Note:</b> Outline differs from borders! Unlike border, the outline is drawn outside the element's border, and may overlap other content. Also, the outline is NOT a part of the element's dimensions; the element's total width and height is not affected by the width of the outline.
<br>
The following example uses the <b>outline-offset</b> property to add space between the border and the outline:
<pre>
div {
  margin: 20px;
  border: 1px solid black;
  outline: 4px solid red;
  outline-offset: 15px;
} 
</pre>
<pre>
div {
  margin: 10px;
  border: 1px solid black;
  outline: 5px dashed blue;
  outline-offset: 5px;
}
</pre>
