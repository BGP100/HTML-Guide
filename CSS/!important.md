<a href="/CSS/Specificity.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/Math.md">Next &gt;</a>
<hr>
The <b>!important</b> rule in CSS is used to add more importance to a property/value than normal.
<br>
In fact, if you use the <b>!important</b> rule, it will override ALL previous styling rules for that specific property on that element!
<br>
Let us look at an example:
<pre>
#myid {
  background-color: blue;
}
.myclass {
  background-color: gray;
}
p {
  background-color: red <b>!important</b>;
}
</pre>
In the example above. all three paragraphs will get a red background color, even though the ID selector and the class selector has a higher specificity. The <b>!important</b> rule overrides the <b>background-color</b> property in both cases.
<h1>Importancy About it</h1>
The only way to override an <b>!important</b> rule is to include another <b>!important</b> rule on a declaration with the same (or higher) specificity in the source code - and here the problem starts! This makes the CSS code confusing and the debugging will be hard, especially if you have a large style sheet!
<br>
Here we have created a simple example. It is not very clear, when you look at the CSS source code, which color is considered most important:
<pre>
#myid {
  background-color: blue !important;
}
.myclass {
  background-color: gray !important;
}
p {
  background-color: red !important;
}
</pre>
<b><i>Tip:</i></b> It is good to know about the <b>!important</b> rule, you might see it in some CSS source code. However, do not use it unless you absolutely have to.
<h1>Some Fair Uses</h1>
One way to use <b>!important</b> is if you have to override a style that cannot be overridden in any other way. This could be if you are working on a Content Management System (CMS) and cannot edit the CSS code. Then you can set some custom styles to override some of the CMS styles.
<br>
Another way to use <b>!important</b> is: Assume you want a special look for all buttons on a page. Here, buttons are styled with a gray background color, white text, and some padding and border:
<pre>
.button {
  background-color: #8c8c8c; 
  color: white;
  padding: 5px;
  border: 1px solid black; 
}
</pre>
The look of a button can sometimes change if we put it inside another element with higher specificity, and the properties get in conflict. Here is an example of this:
<pre>
.button {
  background-color: #8c8c8c; 
  color: white;
  padding: 5px;
  border: 1px solid black; 
}
#myDiv a {
  color: red;
  background-color: yellow; 
}
</pre>
To "force" all buttons to have the same look, no matter what, we can add the <b>!important</b> rule to the properties of the button, like this:
<pre>
.button {
  background-color: #8c8c8c !important; 
  color: white !important;
  padding: 5px !important;
  border: 1px solid black !important; 
}
#myDiv a {
  color: red;
  background-color: yellow; 
}
</pre>
