<a href="/CSS/SASS/@/import.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/SASS/@/extend.md">Next &gt;</a>
<hr>
The <b>@mixin</b> directive lets you create CSS code that is to be reused throughout the website.
<br>
The <b>@include</b> directive is created to let you use (include) the mixin.
<h1>Defining a Mixin</h1>
A mixin is defined with the <b>@mixin</b> directive.
<pre>
@mixin name {
  property: value;
  property: value;
  ...
}
</pre>
The following example creates a mixin named "important-text":
<pre>
@mixin important-text {
  color: red;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid blue;
}
</pre>
<h1>Using a Mixin</h1>
The <b>@include</b> directive is used to include a mixin.
<pre>
selector {
  @include mixin-name;
}
</pre>
So, to include the important-text mixin created above:
<pre>
.danger {
  @include important-text;
  background-color: green;
}
</pre>
The SASS transpiler will convert the above to normal CSS:
<pre>
.danger {
  color: red;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid blue;
  background-color: green;
}
</pre>
A mixin can also include other mixins:
<pre>
@mixin special-text {
  @include important-text;
  @include link;
  @include special-border;
}
</pre>
<h1>Passing Variables to a Mixin</h1>
Mixins accept arguments. This way you can pass variables to a mixin.
<br>
Here is how to define a mixin with arguments:
<pre>
/* Define mixin with two arguments */
@mixin bordered($color, $width) {
  border: $width solid $color;
}
.myArticle {
  @include bordered(blue, 1px);  // Call mixin with two values
}
.myNotes {
  @include bordered(red, 2px); // Call mixin with two values
}
</pre>
Notice that the arguments are set as variables and then used as the values (color and width) of the border property.
<br>
After compilation, the CSS will look like this:
<pre>
.myArticle {
  border: 1px solid blue;
}
.myNotes {
  border: 2px solid red;
}
</pre>
<h1>Default Values</h1>
It is also possible to define default values for mixin variables:
<pre>
@mixin bordered($color: blue, $width: 1px) {
  border: $width solid $color;
}
</pre>
Then, you only need to specify the values that change when you include the mixin:
<pre>
.myTips {
  @include bordered($color: orange);
}
</pre>
<h1>Using a Mixin For Vendor Prefixes</h1>
Another good use of a mixin is for vendor prefixes.
<br>
Here is an example for transform:
<pre>
@mixin transform($property) {
  -webkit-transform: $property;
  -ms-transform: $property;
  transform: $property;
}
.myBox {
  @include transform(rotate(20deg));
}
</pre>
After compilation, the CSS will look like this:
<pre>
.myBox {
  -webkit-transform: rotate(20deg);
  -ms-transform: rotate(20deg);
  transform: rotate(20deg);
}
</pre>
