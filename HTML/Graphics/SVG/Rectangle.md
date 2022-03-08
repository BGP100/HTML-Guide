SVG has some predefined shape elements that can be used by developers:
<ul>
  <li>Rectangle &lt;rect&gt;</li>
  <li>Circle &lt;circle&gt;</li>
  <li>Ellipse &lt;ellipse&gt;</li>
  <li>Line &lt;line&gt;</li>
  <li>Polyline &lt;polyline&gt;</li>
  <li>Polygon &lt;polygon&gt;</li>
  <li>Path &lt;path&gt;</li>
</ul>
The following chapters will explain each element, starting with the rect element.
<h1>Example 1</h1>
<img src="https://i.imgur.com/6MgnOgh.png" width="300" height="100">
<pre>&lt;svg width="400" height="110"&gt;&lt;rect width="300" height="100" style="fill:rgb(0,0,255);stroke-width:3;stroke:rgb(0,0,0)" /&gt;&lt;/svg&gt;</pre>
<b>Explanation:</b>
<ul>
  <li>The width and height attributes of the <b>&lt;rect&gt;</b> element define the height and the width of the rectangle</li>
  <li>The style attribute is used to define CSS properties for the rectangle</li>
  <li>The CSS fill property defines the fill color of the rectangle</li>
  <li>The CSS stroke-width property defines the width of the border of the rectangle</li>
  <li>The CSS stroke property defines the color of the border of the rectangle</li>
</ul>
<h1>Example 2</h1>
<img src="https://i.imgur.com/ibxzJa6.png" width="150" height="150">
<pre>&lt;svg width="400" height="180"&gt;&lt;rect x="50" y="20" width="150" height="150" style="fill:blue;stroke:pink;stroke-width:5;fill-opacity:0.1;stroke-opacity:0.9" /&gt;&lt;/svg&gt;</pre>
<b>Explanation:</b>
<ul>
  <li>The x attribute defines the left position of the rectangle (e.g. x="50" places the rectangle 50 px from the left margin)</li>
  <li>The y attribute defines the top position of the rectangle (e.g. y="20" places the rectangle 20 px from the top margin)</li>
  <li>The CSS fill-opacity property defines the opacity of the fill color (legal range: 0 to 1)</li>
  <li>The CSS stroke-opacity property defines the opacity of the stroke color (legal range: 0 to 1)</li>
</ul>
<h1>Example 3</h1>
<img src="https://i.imgur.com/72gSNMX.png" width="150" height="150">
<pre>&lt;svg width="400" height="180"&gt;&lt;rect x="50" y="20" width="150" height="150" style="fill:blue;stroke:pink;stroke-width:5;opacity:0.5" /&gt;&lt;/svg&gt;</pre>
<b>Explanation:</b>
<ul>
  <li>The CSS opacity property defines the opacity value for the whole element (legal range: 0 to 1)</li>
</ul>
<h1>Example 3</h1>
<img src="https://i.imgur.com/0xms2Lc.png" width="150" height="150">
<pre>&lt;svg width="400" height="180"&gt;&lt;rect x="50" y="20" rx="20" ry="20" width="150" height="150" style="fill:red;stroke:black;stroke-width:5;opacity:0.5" /&gt;&lt;/svg&gt;</pre>
<b>Explanation:</b>
<ul>
  <li>The rx and the ry attributes rounds the corners of the rectangle</li>
</ul>
