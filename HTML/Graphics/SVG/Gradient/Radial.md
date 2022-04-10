<a href="/HTML/Gradient/SVG/Linear.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/HTML/Gradient/GoogleMaps/Main.md">Next &gt;</a>
<hr>
A gradient is a smooth transition from one color to another. In addition, several color transitions can be applied to the same element.
<br>
There are two main types of gradients in SVG:
<ul>
  <li><a href="Linear.md">Linear</a></li>
  <li><b>Radial</b></li>
</ul>
<h1>Example 1</h1>
<img src="https://i.imgur.com/6xxriPw.jpg" width="30%" height="auto">
<pre>&lt;svg height="150" width="500"&gt;&lt;defs&gt;&lt;radialGradient id="grad1" cx="50%" cy="50%" r="50%" fx="50%" fy="50%"&gt;&lt;stop offset="0%" style="stop-color:rgb(255,255,255);stop-opacity:0" /&gt;&lt;stop offset="100%" style="stop-color:rgb(0,0,255);stop-opacity:1" /&gt;&lt;/radialGradient&gt;&lt;/defs&gt;&lt;ellipse cx="200" cy="70" rx="85" ry="55" fill="url(#grad1)" /&gt;&lt;/svg&gt;</pre>
<b>Explanation:</b>
<ul>
  <li>The id attribute of the <b>&lt;radialGradient&gt;</b> tag defines a unique name for the gradient.</li>
  <li>The <i>cx</i>, <i>cy</i> and <i>r</i> attributes define the outermost circle and the <i>fx</i> and <i>fy</i> define the innermost circle.</li>
  <li>The color range for a gradient can be composed of two or more colors. Each color is specified with a <b>&lt;stop&gt;</b> tag. The offset attribute is used to define where the gradient color begin and end.</li>
  <li>The fill attribute links the ellipse element to the gradient.</li>
</ul>
<h1>Example 2</h1>
<img src="https://i.imgur.com/xPqVTkt.jpg" width="15%" height="auto">
<pre>&lt;svg height="150" width="500"&gt;&lt;defs&gt;&lt;radialGradient id="grad2" cx="20%" cy="30%" r="30%" fx="50%" fy="50%"&gt;&lt;stop offset="0%" style="stop-color:rgb(255,255,255);stop-opacity:0" /&gt;&lt;stop offset="100%" style="stop-color:rgb(0,0,255);stop-opacity:1" /&gt;&lt;/radialGradient&gt;&lt;/defs&gt;&lt;ellipse cx="200" cy="70" rx="85" ry="55" fill="url(#grad2)" /&gt;&lt;/svg&gt;</pre>
