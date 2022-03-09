A gradient is a smooth transition from one color to another. In addition, several color transitions can be applied to the same element.
<br>
There are two main types of gradients in SVG:
<ul>
  <li><b>Linear</b></li>
  <li><a href="Radial.md">Radial</a></li>
</ul>
<h1>&lt;linarGradient&gt;</h1>
The <b>&lt;linarGradient&gt;</b> element is used to define a linear gradient.
<br>
The <b>&lt;linarGradient&gt;</b> element must be nested within a <b>&lt;defs&gt;</b> tag. The <b>&lt;defs&gt;</b> tag is short for definitions and contains definition of special elements (such as gradients).
<br>
Linear gradient can be defined as horizontal, vertical or angular gradients:
<ul>
  <li>Horizontal gradients are created when <i>y1</i> and <i>y2</i> are equal and <i>x1</i> and <i>x2</i> differ
  <li>Vertical gradients are created when <i>x1</i> and <i>x2</i> are equal and <i>y1</i> and <i>y2</i> differ
  <li>Angular gradients are created when <i>x1</i> and <i>x2</i> differ and <i>y1</i> and <i>y2</i> differ
</ul>
<h1>Example 1</h1>
<img src="https://i.imgur.com/uzd9lRl.jpg" height="auto" width="210">
<pre>&lt;svg height="150" width="400"&gt;&lt;defs&gt;&lt;linearGradient id="grad1" x1="0%" y1="0%" x2="100%" y2="0%"&gt;&lt;stop offset="0%" style="stop-color:rgb(255,255,0);stop-opacity:1" /&gt;&lt;stop offset="100%" style="stop-color:rgb(255,0,0);stop-opacity:1" /&gt;&lt;/linearGradient&gt;&lt;/defs&gt;&lt;ellipse cx="200" cy="70" rx="85" ry="55" fill="url(#grad1)" /&gt;&lt;/svg&gt;</pre>
<b>Eplanation:</b>
<ul>
  <li>The id attribute of the <b>&lt;linarGradient&gt;</b> tag defines a unique name for the gradient.</li>
  <li>The <i>x1</i>, <i>x2</i>, <i>y1</i>, <i>y2</i> attributes of the <b>&lt;linarGradient&gt;</b> tag define the start and end position of the gradient.</li>
  <li>The color range for a gradient can be composed of two or more colors. Each color is specified with a <b>&lt;stop&gt;</b> tag. The offset attribute is used to define where the gradient color begin and end.</li>
  <li>The fill attribute links the ellipse element to the gradient.</li>
</ul>
<h1>Example 2</h1>
<img src="https://i.imgur.com/QkxdmuI.jpg" height="auto" width="210">
<pre>&lt;svg height="150" width="400"&gt;&lt;defs&gt;&lt;linearGradient id="grad2" x1="0%" y1="0%" x2="0%" y2="100%"&gt;&lt;stop offset="0%" style="stop-color:rgb(255,0,0);stop-opacity:1" /&gt;&lt;stop offset="100%" style="stop-color:rgb(255,255,0);stop-opacity:1" /&gt;&lt;/linearGradient&gt;&lt;/defs&gt;&lt;ellipse cx="200" cy="70" rx="85" ry="55" fill="url(#grad2)" /&gt;&lt;/svg&gt;</pre>
<h1>Example 3</h1>
<img src="https://i.imgur.com/SJGqgfL.jpg" height="auto" width="210">
<pre>&lt;svg height="150" width="400"&gt;&lt;defs&gt;&lt;linearGradient id="grad3" x1="0%" y1="0%" x2="100%" y2="0%"&gt;&lt;stop offset="0%" style="stop-color:rgb(255,255,0);stop-opacity:1" /&gt;&lt;stop offset="100%" style="stop-color:rgb(255,0,0);stop-opacity:1" /&gt;&lt;/linearGradient&gt;&lt;/defs&gt;&lt;ellipse cx="200" cy="70" rx="85" ry="55" fill="url(#grad3)" /&gt;&lt;text fill="#ffffff" font-size="45" font-family="Verdana" x="150" y="86"&gt;SVG&lt;/text&gt;&lt;/svg&gt;</pre>
<b>Eplanation:</b>
<ul>
  <li>The <b>&lt;text&gt;</b> element is used to add a text</li>
</ul>
