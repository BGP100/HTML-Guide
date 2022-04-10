<a href="/CSS/Advanced/Variables/MediaQueries.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/Advanced/MediaQueries.md">Next &gt;</a>
<hr>
The CSS box-sizing property allows us to include the padding and border in an element's total width and height.
<h1>WITHOUT the Property</h1>
By default, the width and height of an element is calculated like this:
<br>
width + padding + border = actual width of an element
height + padding + border = actual height of an element
<br>
This means: When you set the width/height of an element, the element often appears bigger than you have set (because the element's border and padding are added to the element's specified width/height).
<br>
The following illustration shows two <b>&lt;div&gt;</b> elements with the same specified width and height:
<br>
<img src="https://i.imgur.com/dJ6GfdT.png">
<br>
<img src="https://i.imgur.com/1QfTz8S.png">
<br>
The two <b>&lt;div&gt;</b> elements above end up with different sizes in the result (because div2 has a padding specified):
<pre>
.div1 {
  width: 300px;
  height: 100px;
  border: 1px solid blue;
}
.div2 {
  width: 300px;
  height: 100px;
  padding: 50px;
  border: 1px solid red;
}
</pre>
The <b>box-sizing</b> property solves this problem.
<h1>WITH the Property</h1>
The <b>box-sizing</b> property allows us to include the padding and border in an element's total width and height.
<br>
If you set <b>box-sizing: border-box;</b> on an element, padding and border are included in the width and height:
<br>
<img src="https://i.imgur.com/grwNv0l.png">
<br>
<img src="https://i.imgur.com/0u36924.png">
<br>
Here is the same example as above, with <b>box-sizing:</b> border-box; added to both <b>&lt;div&gt;</b> elements:
<pre>
.div1 {
  width: 300px;
  height: 100px;
  border: 1px solid blue;
  box-sizing: border-box;
}
.div2 {
  width: 300px;
  height: 100px;
  padding: 50px;
  border: 1px solid red;
  box-sizing: border-box;
}
</pre>
Since the result of using the <b>box-sizing: border-box;</b> is so much better, many developers want all elements on their pages to work this way.
<br>
The code below ensures that all elements are sized in this more intuitive way. Many browsers already use <b>box-sizing: border-box;</b> for many form elements (but not all - which is why inputs and text areas look different at width: 100%;).
<br>
Applying this to all elements is safe and wise:
<pre>
* {
  box-sizing: border-box;
}
</pre>
