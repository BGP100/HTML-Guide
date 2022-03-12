Margins are used to create space around elements, outside of any defined borders.
<br>
<img src="https://i.imgur.com/ki6HmRJ.png">
<br>
The CSS <b>margin</b> properties are used to create space around elements, outside of any defined borders.
<br>
With CSS, you have full control over the margins. There are properties for setting the margin for each side of an element (top, right, bottom, and left).
<br>
CSS has properties for specifying the margin for each side of an element:
<ul>
  <li><b>margin-top</b></li>
  <li><b>margin-right</b></li>
  <li><b>margin-bottom</b></li>
  <li><b>margin-left</b></li>
</ul>
All the margin properties can have the following values:
<ul>
  <li>auto - the browser calculates the margin</li>
  <li>length - specifies a margin in px, pt, cm, etc.</li>
  <li>% - specifies a margin in % of the width of the containing element</li>
  <li>inherit - specifies that the margin should be inherited from the parent element</li>
</ul>
<b>Tip:</b> Negative values are allowed.
<pre>
p {
  margin-top: 100px;
  margin-bottom: 100px;
  margin-right: 150px;
  margin-left: 80px;
}
</pre>
To shorten the code, it is possible to specify all the margin properties in one property.
<br>
The margin property is a shorthand property for the following individual margin properties:
<ul>
  <li><b>margin-top</b></li>
  <li><b>margin-right</b></li>
  <li><b>margin-bottom</b></li>
  <li><b>margin-left</b></li>
</ul>
So, here is how it works:
<br>
If the margin property has four values:
<br>
<b>margin: 25px 50px 75px 100px;</b>
<ul>
  <li>top margin is 25px</li>
  <li>right margin is 50px</li>
  <li>bottom margin is 75px</li>
  <li>left margin is 100px</li>
</ul>
<pre>
p {
  margin: 25px 50px 75px 100px;
}
</pre>
If the <b>margin</b> property has three values:
<b></b>
<ul>
  <li>top margin is 25px</li>
  <li>right and left margins are 50px</li>
  <li>bottom margin is 75px</li>
</ul>
<pre>
p {
  margin: 25px 50px 75px;
}
</pre>
If the margin property has two values:
<br>
<b>margin: 25px 50px;</b>
<ul>
  <li>top and bottom margins are 25px</li>
  <li>right and left margins are 50px</li>
</ul>
<pre>
p {
  margin: 25px 50px;
}
</pre>
If the margin property has one value:
<br>
<b>margin: 25px;</b>
<ul>
  <li>all four margins are 25px</li>
</ul>
<pre>
p {
  margin: 25px;
}
</pre>
<h1>auto</h1>
You can set the margin property to auto to horizontally center the element within its container.
<br>
The element will then take up the specified width, and the remaining space will be split equally between the left and right margins.
<pre>
div {
  width: 300px;
  margin: auto;
  border: 1px solid red;
}
</pre>
<h1>inherit</h1>
This example lets the left margin of the <b>&lt;p class="ex1"&gt;</b> element be inherited from the parent element (<b>&lt;div&gt;</b>):
<pre>
div {
  border: 1px solid red;
  margin-left: 100px;
}
p.ex1 {
  margin-left: inherit;
}
</pre>
<h1>Collapsed</h1>
Sometimes two margins collapse into a single margin.
<hr>
Top and bottom margins of elements are sometimes collapsed into a single margin that is equal to the largest of the two margins.
<br>
This does not happen on left and right margins! Only top and bottom margins!
<br>
Look at the following example:
<pre>
h1 {
  margin: 0 0 50px 0;
}
h2 {
  margin: 20px 0 0 0;
}
</pre>
In the example above, the <b>&lt;h1&gt;</b> element has a bottom margin of 50px and the <b>&lt;h2&gt;</b> element has a top margin set to 20px.
<br>
Common sense would seem to suggest that the vertical margin between the <b>&lt;h1&gt;</b> and the <b>&lt;h2&gt;</b> would be a total of 70px (50px + 20px). But due to margin collapse, the actual margin ends up being 50px.
