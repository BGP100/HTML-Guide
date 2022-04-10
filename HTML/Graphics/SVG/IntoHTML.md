<a href="/HTML/Graphics/SVG/Main.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/HTML/Graphics/SVG/Rectangle.md">Next &gt;</a>
<hr>
You can embed SVG elements directly into your HTML pages.
<hr>
Here is an example of a simple SVG graphic:
<br>
<img src="https://i.imgur.com/oVlYcHQ.jpg" width="100" height="100">
<br>
and here is the HTML code:
<pre>&lt;svg width="100" height="100"&gt;&lt;circle cx="50" cy="50" r="40" stroke="green" stroke-width="4" fill="yellow" /&gt;&lt;/svg&gt;</pre>
SVG Code explanation:
<ul>
  <li>An SVG image begins with an &lt;svg&gt; element</li>
  <li>The width and height attributes of the &lt;svg&gt; element define the width and height of the SVG image</li>
  <li>The &lt;circle&gt; element is used to draw a circle</li>
  <li>The cx and cy attributes define the x and y coordinates of the center of the circle. If cx and cy are not set, the circle's center is set to (0, 0)</li>
  <li>The r attribute defines the radius of the circle</li>
  <li>The stroke and stroke-width attributes control how the outline of a shape appears. We set the outline of the circle to a 4px green "border"</li>
  <li>The fill attribute refers to the color inside the circle. We set the fill color to yellow</li>
  <li>The closing &lt;/svg&gt; tag closes the SVG image</li>
</ul>
<b>Note:</b> Since SVG is written in XML, all elements must be properly closed!
