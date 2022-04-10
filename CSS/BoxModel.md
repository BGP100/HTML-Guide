<a href="/CSS/HeightAndWidth.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/Outline/Main.md">Next &gt;</a>
<hr>
In CSS, the term "box model" is used when talking about design and layout.
<br>
The CSS box model is essentially a box that wraps around every HTML element. It consists of: margins, borders, padding, and the actual content. The image below illustrates the box model:
<br>
<img src="https://i.imgur.com/sDri3Pg.png">
<br>
Explanation of the different parts:
<ul>
  <li>Content - The content of the box, where text and images appear</li>
  <li>Padding - Clears an area around the content. The padding is transparent</li>
  <li>Border - A border that goes around the padding and content</li>
  <li>Margin - Clears an area outside the border. The margin is transparent</li>
</ul>
The box model allows us to add a border around elements, and to define space between elements.
<pre>
div {
  width: 300px;
  border: 15px solid green;
  padding: 50px;
  margin: 20px;
}
</pre>
<h1>Width and Height</h1>
In order to set the width and height of an element correctly in all browsers, you need to know how the box model works.
<pre>
div {
  width: 320px;
  padding: 10px;
  border: 5px solid gray;
  margin: 0;
}
</pre>
Here is the calculation:
<br>
<kbd>320px (width) + 20px (left + right padding) + 10px (left + right border) + 0px (left + right margin) = <b>350px</b></kbd>
<p></p>
The total width of an element should be calculated like this:
<br>
Total element width = width + left padding + right padding + left border + right border + left margin + right margin
<br>
The total height of an element should be calculated like this:
<br>
Total element height = height + top padding + bottom padding + top border + bottom border + top margin + bottom margin
