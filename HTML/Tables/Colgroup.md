The <b>&lt;colgroup&gt;</b> element is used to style specific columns of a table.
<br>
<img src="https://i.imgur.com/7JxbkoB.png">
<br>
The <colgroup> element should be used as a container for the column specifications.
<br>
Each group are specified with a <b>&lt;col&lt;</b> element.
<br>
The span attribute specifies how many columns that gets the style.
<br>
The style attribute specifies the style to give the columns.
<pre>
&lt;table style="width:60%;"&gt;
&lt;colgroup&gt;
    &lt;col span="2" style="background-color:rgba(150, 212, 212,0.4)"&gt;
  &lt;/colgroup&gt;
  &lt;tr&gt;
    &lt;th&gt;MON&lt;/th&gt;
    &lt;th&gt;TUE&lt;/th&gt;
    &lt;th&gt;WED&lt;/th&gt;
    &lt;th&gt;THU&lt;/th&gt;
    &lt;th&gt;FRI&lt;/th&gt;
    &lt;th&gt;SAT&lt;/th&gt;
    &lt;th&gt;SUN&lt;/th&gt;
  &lt;/tr&gt;
  &lt;tr&gt;
    &lt;td&gt;1&lt;/td&gt;
    &lt;td&gt;2&lt;/td&gt;
    &lt;td&gt;3&lt;/td&gt;
    &lt;td&gt;4&lt;/td&gt;
    &lt;td&gt;5&lt;/td&gt;
    &lt;td&gt;6&lt;/td&gt;
    &lt;td&gt;7&lt;/td&gt;
  &lt;/tr&gt;
  &lt;tr&gt;
    &lt;td&gt;8&lt;/td&gt;
    &lt;td&gt;9&lt;/td&gt;
    &lt;td&gt;10&lt;/td&gt;
    &lt;td&gt;11&lt;/td&gt;
    &lt;td&gt;12&lt;/td&gt;
    &lt;td&gt;13&lt;/td&gt;
    &lt;td&gt;14&lt;/td&gt;
  &lt;/tr&gt;
  &lt;tr&gt;
    &lt;td&gt;15&lt;/td&gt;
    &lt;td&gt;16&lt;/td&gt;
    &lt;td&gt;17&lt;/td&gt;
    &lt;td&gt;18&lt;/td&gt;
    &lt;td&gt;19&lt;/td&gt;
    &lt;td&gt;20&lt;/td&gt;
    &lt;td&gt;21&lt;/td&gt;
  &lt;/tr&gt;
  &lt;tr&gt;
    &lt;td&gt;22&lt;/td&gt;
    &lt;td&gt;23&lt;/td&gt;
    &lt;td&gt;24&lt;/td&gt;
    &lt;td&gt;25&lt;/td&gt;
    &lt;td&gt;26&lt;/td&gt;
    &lt;td&gt;27&lt;/td&gt;
    &lt;td&gt;28&lt;/td&gt;
  &lt;/tr&gt;
&lt;/table&gt;
</pre>
<h1>Selected Properties</h1>
There are only a very limited selection of CSS properties that are allowed to be used in the colgroup:
<ul>
  <li>width property</li>
  <li>visibility property</li>
  <li>background properties</li>
  <li>border properties</li>
</ul>
All other CSS properties will have no effect on your tables.
<h1>Multiple Col</h1>
If you want to style more columns with different styles, use more <b>&lt;col&lt;</b> elements inside the <b>&lt;colgroup&lt;</b>:
<pre>
&lt;table style="width:60%;"&gt;
&lt;colgroup&gt;
    &lt;col span="2" style="background-color: #D6EEEE"&gt;
    &lt;col span="3" style="background-color: pink"&gt;
  &lt;/colgroup&gt;
  &lt;tr&gt;
    &lt;th&gt;MON&lt;/th&gt;
    &lt;th&gt;TUE&lt;/th&gt;
    &lt;th&gt;WED&lt;/th&gt;
    &lt;th&gt;THU&lt;/th&gt;
    &lt;th&gt;FRI&lt;/th&gt;
    &lt;th&gt;SAT&lt;/th&gt;
    &lt;th&gt;SUN&lt;/th&gt;
  &lt;/tr&gt;
  &lt;tr&gt;
    &lt;td&gt;1&lt;/td&gt;
    &lt;td&gt;2&lt;/td&gt;
    &lt;td&gt;3&lt;/td&gt;
    &lt;td&gt;4&lt;/td&gt;
    &lt;td&gt;5&lt;/td&gt;
    &lt;td&gt;6&lt;/td&gt;
    &lt;td&gt;7&lt;/td&gt;
  &lt;/tr&gt;
  &lt;tr&gt;
    &lt;td&gt;8&lt;/td&gt;
    &lt;td&gt;9&lt;/td&gt;
    &lt;td&gt;10&lt;/td&gt;
    &lt;td&gt;11&lt;/td&gt;
    &lt;td&gt;12&lt;/td&gt;
    &lt;td&gt;13&lt;/td&gt;
    &lt;td&gt;14&lt;/td&gt;
  &lt;/tr&gt;
  &lt;tr&gt;
    &lt;td&gt;15&lt;/td&gt;
    &lt;td&gt;16&lt;/td&gt;
    &lt;td&gt;17&lt;/td&gt;
    &lt;td&gt;18&lt;/td&gt;
    &lt;td&gt;19&lt;/td&gt;
    &lt;td&gt;20&lt;/td&gt;
    &lt;td&gt;21&lt;/td&gt;
  &lt;/tr&gt;
  &lt;tr&gt;
    &lt;td&gt;22&lt;/td&gt;
    &lt;td&gt;23&lt;/td&gt;
    &lt;td&gt;24&lt;/td&gt;
    &lt;td&gt;25&lt;/td&gt;
    &lt;td&gt;26&lt;/td&gt;
    &lt;td&gt;27&lt;/td&gt;
    &lt;td&gt;28&lt;/td&gt;
  &lt;/tr&gt;
&lt;/table&gt;
</pre>
<h1>Empty Colgroups</h1>
If you want to style columns in the middle of a table, insert a "empty" <b>&lt;col&lt;</b> element (with no styles) for the columns before:
<pre>
&lt;table style="width:60%;"&gt;
&lt;colgroup&gt;
    &lt;col span="2"&gt;
    &lt;col span="3" style="background-color: pink"&gt;
  &lt;/colgroup&gt;
  &lt;tr&gt;
    &lt;th&gt;MON&lt;/th&gt;
    &lt;th&gt;TUE&lt;/th&gt;
    &lt;th&gt;WED&lt;/th&gt;
    &lt;th&gt;THU&lt;/th&gt;
    &lt;th&gt;FRI&lt;/th&gt;
    &lt;th&gt;SAT&lt;/th&gt;
    &lt;th&gt;SUN&lt;/th&gt;
  &lt;/tr&gt;
  &lt;tr&gt;
    &lt;td&gt;1&lt;/td&gt;
    &lt;td&gt;2&lt;/td&gt;
    &lt;td&gt;3&lt;/td&gt;
    &lt;td&gt;4&lt;/td&gt;
    &lt;td&gt;5&lt;/td&gt;
    &lt;td&gt;6&lt;/td&gt;
    &lt;td&gt;7&lt;/td&gt;
  &lt;/tr&gt;
  &lt;tr&gt;
    &lt;td&gt;8&lt;/td&gt;
    &lt;td&gt;9&lt;/td&gt;
    &lt;td&gt;10&lt;/td&gt;
    &lt;td&gt;11&lt;/td&gt;
    &lt;td&gt;12&lt;/td&gt;
    &lt;td&gt;13&lt;/td&gt;
    &lt;td&gt;14&lt;/td&gt;
  &lt;/tr&gt;
  &lt;tr&gt;
    &lt;td&gt;15&lt;/td&gt;
    &lt;td&gt;16&lt;/td&gt;
    &lt;td&gt;17&lt;/td&gt;
    &lt;td&gt;18&lt;/td&gt;
    &lt;td&gt;19&lt;/td&gt;
    &lt;td&gt;20&lt;/td&gt;
    &lt;td&gt;21&lt;/td&gt;
  &lt;/tr&gt;
  &lt;tr&gt;
    &lt;td&gt;22&lt;/td&gt;
    &lt;td&gt;23&lt;/td&gt;
    &lt;td&gt;24&lt;/td&gt;
    &lt;td&gt;25&lt;/td&gt;
    &lt;td&gt;26&lt;/td&gt;
    &lt;td&gt;27&lt;/td&gt;
    &lt;td&gt;28&lt;/td&gt;
  &lt;/tr&gt;
&lt;/table&gt;
</pre>
<h1>Hide Columns</h1>
You can hide columns with the <b>visibility: collapse</b> property:
<pre>
&lt;table style="width:60%;"&gt;
&lt;colgroup&gt;
    &lt;col span="2"&gt;
    &lt;col span="3" style="visibility: collapse"&gt;
  &lt;/colgroup&gt;
  &lt;tr&gt;
    &lt;th&gt;MON&lt;/th&gt;
    &lt;th&gt;TUE&lt;/th&gt;
    &lt;th&gt;WED&lt;/th&gt;
    &lt;th&gt;THU&lt;/th&gt;
    &lt;th&gt;FRI&lt;/th&gt;
    &lt;th&gt;SAT&lt;/th&gt;
    &lt;th&gt;SUN&lt;/th&gt;
  &lt;/tr&gt;
  &lt;tr&gt;
    &lt;td&gt;1&lt;/td&gt;
    &lt;td&gt;2&lt;/td&gt;
    &lt;td&gt;3&lt;/td&gt;
    &lt;td&gt;4&lt;/td&gt;
    &lt;td&gt;5&lt;/td&gt;
    &lt;td&gt;6&lt;/td&gt;
    &lt;td&gt;7&lt;/td&gt;
  &lt;/tr&gt;
  &lt;tr&gt;
    &lt;td&gt;8&lt;/td&gt;
    &lt;td&gt;9&lt;/td&gt;
    &lt;td&gt;10&lt;/td&gt;
    &lt;td&gt;11&lt;/td&gt;
    &lt;td&gt;12&lt;/td&gt;
    &lt;td&gt;13&lt;/td&gt;
    &lt;td&gt;14&lt;/td&gt;
  &lt;/tr&gt;
  &lt;tr&gt;
    &lt;td&gt;15&lt;/td&gt;
    &lt;td&gt;16&lt;/td&gt;
    &lt;td&gt;17&lt;/td&gt;
    &lt;td&gt;18&lt;/td&gt;
    &lt;td&gt;19&lt;/td&gt;
    &lt;td&gt;20&lt;/td&gt;
    &lt;td&gt;21&lt;/td&gt;
  &lt;/tr&gt;
  &lt;tr&gt;
    &lt;td&gt;22&lt;/td&gt;
    &lt;td&gt;23&lt;/td&gt;
    &lt;td&gt;24&lt;/td&gt;
    &lt;td&gt;25&lt;/td&gt;
    &lt;td&gt;26&lt;/td&gt;
    &lt;td&gt;27&lt;/td&gt;
    &lt;td&gt;28&lt;/td&gt;
  &lt;/tr&gt;
&lt;/table&gt;
</pre>
