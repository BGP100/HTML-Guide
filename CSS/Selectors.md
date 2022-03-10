A CSS selector selects the HTML element(s) you want to style.
<hr>
CSS selectors are used to "find" (or select) the HTML elements you want to style.
<br>
We can divide CSS selectors into five categories:
<ul>
  <li>Simple selectors (select elements based on name, id, class)</li>
  <li>Combinator selectors (select elements based on a specific relationship between them)</li>
  <li>Pseudo-class selectors (select elements based on a certain state)</li>
  <li>Pseudo-elements selectors (select and style a part of an element)</li>
  <li>Attribute selectors (select elements based on an attribute or attribute value)</li>
  <li>This page will explain the most basic CSS selectors.</li>
</ul>
<h1>Elements</h1>
The element selector selects HTML elements based on the element name.
<pre>
p {
  text-align: center;
  color: red;
}
</pre>
Here, all <b>&lt;p&gt;</b> elements on the page will be center-aligned, with a red text color.
<h1>id</h1>
The id selector uses the id attribute of an HTML element to select a specific element.
<br>
The id of an element is unique within a page, so the id selector is used to select one unique element!
<br>
To select an element with a specific id, write a hash (#) character, followed by the id of the element.
<pre>
#para1 {
  text-align: center;
  color: red;
}
</pre>
The CSS rule below will be applied to the HTML element with <b>id="para1"</b>.
<h1>class</h1>
The class selector selects HTML elements with a specific class attribute.
<br>
To select elements with a specific class, write a period (.) character, followed by the class name.
<pre>
.center {
  text-align: center;
  color: red;
}
</pre>
In this example all HTML elements with <b>class="center"</b> will be red and center-aligned
<p></p>
You can also specify that only specific HTML elements should be affected by a class.
<pre>
p.center {
  text-align: center;
  color: red;
}
</pre>
In this example only <b>&lt;p&gt;</b> elements with class="center" will be red and center-aligned
<p></p>
HTML elements can also refer to more than one class.
<pre>&lt;p class="center large"&gt;This paragraph refers to two classes.&lt;/p&gt;</pre>
<h1>Universal</h1>
The universal selector (<code>*</code>) selects all HTML elements on the page.
<pre>
* {
  text-align: center;
  color: blue;
}
</pre>
The CSS rule below will affect every HTML element on the page.
<h1>Grouping</h1>
The grouping selector selects all the HTML elements with the same style definitions.
<br>
Look at the following CSS code (the h1, h2, and p elements have the same style definitions):
<pre>
h1 {
  text-align: center;
  color: red;
}
h2 {
  text-align: center;
  color: red;
}
p {
  text-align: center;
  color: red;
}
</pre>
It will be better to group the selectors, to minimize the code.
<br>
To group selectors, separate each selector with a comma.
<pre>
h1, h2, p {
  text-align: center;
  color: red;
}
</pre>
