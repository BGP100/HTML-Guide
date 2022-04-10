<a href="/CSS/SASS/@/mixin.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/SASS/Functions/String.md">Next &gt;</a>
<hr>
The <b>@extend</b> directive lets you share a set of CSS properties from one selector to another.
<br>
The <b>@extend</b> directive is useful if you have almost identically styled elements that only differ in some small details.
<br>
The following Sass example first creates a basic style for buttons (this style will be used for most buttons). Then, we create one style for a "Report" button and one style for a "Submit" button. Both "Report" and "Submit" button inherit all the CSS properties from the .button-basic class, through the <b>@extend</b> directive. In addition, they have their own colors defined:
<pre>
.button-basic  {
  border: none;
  padding: 15px 30px;
  text-align: center;
  font-size: 16px;
  cursor: pointer;
}
.button-report  {
  @extend .button-basic;
  background-color: red;
}
.button-submit  {
  @extend .button-basic;
  background-color: green;
  color: white;
}
</pre>
After compilation, the CSS will look like this:
<pre>
.button-basic, .button-report, .button-submit {
  border: none;
  padding: 15px 30px;
  text-align: center;
  font-size: 16px;
  cursor: pointer;
}
.button-report  {
  background-color: red;
}
.button-submit  {
  background-color: green;
  color: white;
}
</pre>
By using the <b>@extend</b> directive, you do not need to specify several classes for an element in your HTML code, like this: <code>&lt;button class="button-basic button-report"&gt;Report this&lt;/button&gt;</code>. You just need to specify .button-report to get both sets of styles.
<br>
The <b>@extend</b> directive helps keep your Sass code very DRY.=
